# NetworkX: A Python library for visualizing complex relationships
[![Build Status](https://github.com/johnwmillr/LyricsGenius/actions/workflows/build.yml/badge.svg?branch=master)](https://github.com/johnwmillr/LyricsGenius/actions/workflows/build.yml)
[![Documentation Status](https://github.com/johnwmillr/LyricsGenius/actions/workflows/docs.yml/badge.svg?branch=master)](https://github.com/johnwmillr/LyricsGenius/actions/workflows/docs.yml)
[![PyPI version](https://badge.fury.io/py/lyricsgenius.svg)](https://pypi.org/project/lyricsgenius/)

`NetworkX` enables users to model and analyze complex structures and multi-layered networks

Official documentation for `NetworkX` is available online at [networkx.org](https://networkx.org/documentation/stable/reference/index.html)

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
| username | first_follower | days |
-----------|----------------|------|
| john_blackwell | rani_bannerjee | 29 |
| yang_jeongin | nancy_dorian | 143 |
| winter_maddox | mordecai_wells | 47 |
```
