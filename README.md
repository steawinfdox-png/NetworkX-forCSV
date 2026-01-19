# NetworkX for Dataframes
**Python package to create and study dynamics of complex networks sourced from CSV data and Excel files**
[![Build Status](https://github.com/johnwmillr/LyricsGenius/actions/workflows/build.yml/badge.svg?branch=master)](https://github.com/johnwmillr/LyricsGenius/actions/workflows/build.yml)
[![Documentation Status](https://github.com/johnwmillr/LyricsGenius/actions/workflows/docs.yml/badge.svg?branch=master)](https://github.com/johnwmillr/LyricsGenius/actions/workflows/docs.yml)
[![PyPI version](https://badge.fury.io/py/lyricsgenius.svg)](https://pypi.org/project/lyricsgenius/)

`NetworkX` enables users to model and analyze complex structures and multi-layered networks

Official documentation for `NetworkX` is available online at [networkx.org](https://networkx.org/documentation/stable/reference/index.html)

# Setup
To utilize the visualization capabilities of `NetworkX`, you will need to have `Matplotlib` installed and imported.

## Installation
`NetworkX` requires Python 3.11 or greater.

Install package:

```bash
pip install networkx
```
Import library:

```python
import networkx as nx
```

## Types of Visualizations

Graph: undirected graph with only one edge between nodes ([example](https://github.com/steawinfdox-png/Network-X/blob/main/assets/networkx-graph-types-cf81549883bb93cd4b558d22ceb8a27a.png)):
```python
graph = nx.Graph()
```

Multigraph: undirected graph with multiple edges between nodes ([example](https://github.com/steawinfdox-png/Network-X/blob/main/assets/multigraph.png)):
```python
multigraph = nx.Multigraph()
```

Digraph: directed graph with only one edge between nodes ([example](https://github.com/steawinfdox-png/Network-X/blob/main/assets/digraph.png)):
```python
digraph = nx.Digraph()
```

Multidigraph: directed graph with multiple edges between nodes([example](https://github.com/steawinfdox-png/Network-X/blob/main/assets/multidigraph.png)):
```python
multidigraph = nx.MultiDigraph()
```

## Using NetworkX for CSV dataframes
```python
df = pd.read_csv('social_network.csv')
df
```

```bash
# social_network.csv
| username | first_follower | days |
| john_blackwell | yang_jeongin | 29 |
| yang_jeongin | john_blackwell | 143 |
| winter_maddox | john_blackwell | 47 |
```

```python
# Initialize variable containing csv data
graph = nx.from_pandas_edgelist(df, source = 'username', target = 'first_follower', edge_attr = 'days')

# Retrieve all node names
graph.nodes()
```
RESULT:
> NodeView(("john_blackwell", "yang_jeongin", "winter_maddox"))

### Visualizing relationships in dataframes

Make relatedness of nodes more apparent:
```python
layout = nx.spring_layout(graph)
```

Visualize:
```python
nx.draw_networkx_nodes(graph, layout)
nx.draw_networkx_edges(graph, layout)
nx.draw_networkx_labels(graph, layout)
plt.show()
```

### Design options

Change node size:
```python
# Change `node_size` for increasing/decreasing size of nodes
nx.draw_networkx_nodes(graph, layout, node_size = 500)
```

Change node color:
```python
# Change `alpha` for color
nx.draw_networkx_edges(graph, layout, alpha = 0.5)
```

Change edge thickness:
```python
# Edge weight dependent on 'days' column data
weight = list(nx.get_edge_attributes(graph, 'days').values())

# Add weight to lines connecting nodes
nx.draw_networkx_edges(graph, layout, width = weight)
```

## Contact me!
Feel free to let me know of any errors or bugs you find! Also, if you need help for a specific project of yours using `NetworkX`, [open an issue](https://github.com/steawinfdox-png/Network-X/issues) or send me a pull request!

## Credits
- [JS_Data Talks](https://www.youtube.com/watch?v=k4tLpFEGeTo)
- [NetworkX.org](https://networkx.org/documentation/stable/reference/introduction.html#networkx-basics)
