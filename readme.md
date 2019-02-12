# Multilayer Networks of Movies

Here is the data corresponding to the Complex Networks 2018 paper *"Multilayer Networks of Movie Scripts"* by Youssef Mourchid, Benjamin Renoust, Hocine Cherifi, and Mohammed El Hassouni.

The data represents movie scripts under the form of temporal multilayer networks extracted from aligning scripts and subtitles. Please read the paper in `Paper/` for a full description.

## Model

Each movie proposes a list of CSV files as follows (the headers should be self explanatory).
#### Nodes and time information:

- `scene_timestamps.csv`: timestamps of detected scenes (contains ids, start and end times),
- `dialogue_timestamps.csv`: timestamps of detected dialogue pieces (contains ids, start and end times - dialogues are usually contained in scene),- `character_nodes.csv`: list of characters (contains ids, list of scenes and dialogues ids in which each character has been detected),- `keyword_nodes.csv`: list of keywords (contains ids, list of scenes and dialogues ids in which each keyword has been detected),- `location_nodes.csv`: list of locations (contains ids, list of scenes and dialogues ids in which each location has been detected).

#### Edges:
- `character_character_edges.csv`: list of edges connecting characters derived from dialogues (contains source node, target node, scene id - direction does not matter here), - `keyword_keyword_edges.csv`: list of edges connecting keywords derived from dialogue co-occurrence (contains source node, target node, scene id, dialogue id - direction does not matter here),- `location_location_edges.csv`: list of edges connecting locations derived from scene transition (contains source node, target node, source scene id, target scene - direction matters here),
- `character_keyword_edges.csv`: list of edges connecting keywords to characters derived from dialogue utterances,- `character_location_edges.csv`: list of edges connecting locations to characters derived from scene occurrences,
- `keyword_location_edges.csv`: list of edges connecting keywords to locations derived from dialogue utterances in scenes.



## Citation
If you use the data, please consider citing our paper as follows:

```
@inproceedings{mourchid_multilayer18,
  author = {Youssef Mourchid and Benjamin Renoust and Hocine Cherifi and Mohammed El Hassouni},
  title = {Multilayer Network Model of Movie Script},
  booktitle = {Complex Networks 2018, Cambridge, UK, 2018 Dec. 11-13},
  pages = {782--796},
  year = {2018},
  url = {https://doi.org/10.1007/978-3-030-05411-3\_62},
}
```