# Social Networks

## Basics

- Diameter of a graph is the largest distance between any two vertices.
- BFS is better to find the shortest distance in a social network between two nodes/vertices.
- There is a high probability to encounter a large community when:
  - average degree is 1.
  - edge probability is large enough.
- Adjacency-List is best for sparce graphs, and also easy to traverse the neighbors.

## NetworkX Library

- nx.Graph()
  - Creates a undirected graph.
- nx.DiGraph()
  - Creates a directed graph.
- nx.MultiGraph()
  - Creates a multigraph (a graph where two nodes can have multiple edges).

## Gephi

- Modularity is used to determine connectivity between communities.

## Page Rank Algorithm

- Pages that are linked to more often are more important.

### Link Prediction

- Predicting what will the current page will link to next.
- Link Prediction is done with Jaccard Similarity Index.

## Web Graph Model

- Nodes: Web Pages.
- Edges: Hyperlinks Between Pages.

## Closures

### Triad Closure

- When one person has two friends, it is highly likely that the other two become friends.

## Neighborhood Overlap

- Common neighbors that two nodes share.

## Bridge

- An edge connecting two components.

### Local Bridge

- Connects two nodes that have fewer or no connections between them or their neighbors.

### Structural Hole

- A gap between two components that aren't connected.
- Usually a BROKER helps in transfer of knowledge.

## Embeddedness

- If stranger meets, NO
- If stranger already knew some of our friends, YES
- The degree to which a relationship is supported by other relationships.
