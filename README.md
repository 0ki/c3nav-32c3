# c3nav

Indoor navigation for the **32nd Chaos Communication Congress** and future
events. See it live at https://c3nav.de.

There are still some features to come including selecting from map, Wi-Fi
positioning (as an Android App) and more POIs (assemblies etc.)

c3nav is written in python3 using flask, scipy, numpy and matplotlib.

Feel free to contact me if you have and questions/ideas or want to contribute.
My DECT number at 32c3 will be NMKT (6658).

## Running it yourself

* Clone the repository
* `pip install -r requirements.txt`
* `python3 main.py graph.32c3.json`
* navigate to http://localhost:5000/
* To activate debugging, add `debug` to the end of the command.

## Editing the graph

You can just edit minor stuff directly in the JSON file. You have to restart
the python script in order to reload the graph.

To edit the underlying graph, rooms, barriers and points of interest, run
`python3 configure.py graph.32c3.json` and navigate to http://localhost:5000/.

To add translations, use `python3 translate.py graph.32c3.json (en|de)`. Please
do not submit pull request for other languages for now.

## Setting up a new graph

Copy `graph.empty.json` and edit the basic meta data, add the level maps as
images, then build/edit the graph as described above.