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

## Usage
Import library:

```python
import networkx as nx
```

Undirected graph with only one edge between nodes:
```python
graph = nx.Graph()
```

Undirected graph with multiple edges between nodes:
```python
multigraph = nx.Multigraph()
```

Directed graph with only one edge between nodes:
```python
digraph = nx.Digraph()
```

Directed graph with multiple edges between nodes:
```python
multigraph = nx.MultiDigraph()
```
