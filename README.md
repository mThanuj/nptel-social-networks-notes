<script type="text/javascript" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

# Social Networks

## Basics

- Diameter of a graph is the largest distance between any two vertices.
- BFS is better to find the shortest distance in a social network between two nodes/vertices.
- There is a high probability to encounter a large community when:
  - average degree is 1.
  - edge probability is large enough.
- Adjacency-List is best for sparse graphs, and also easy to traverse the neighbors.

## NetworkX Library

- nx.Graph()
  - Creates a undirected graph.
- nx.DiGraph()
  - Creates a directed graph.
- nx.MultiGraph()
  - Creates a multigraph (a graph where two nodes can have multiple edges).

## Gephi

- Modularity is used to determine connectivity between communities.

## Algorithms and Models

### Page Rank Algorithm

- Pages that are linked to more often are more important.
- Degree Rank vs Page Rank:
  - Degree Rank: Number of links to a page.
  - Page Rank: Importance of the page based on the number of links to it and the importance of the pages linking to it.

#### Link Prediction

- Predicting what will the current page will link to next.
- Link Prediction is done with Jaccard Similarity Index.

### Web Graph Model

- Nodes: Web Pages.
- Edges: Hyperlinks Between Pages.
- Links, Keywords and Ratings.

#### Collecting Web Graphs

- Web Graphs are collected by crawling the web.
- Do a random walk on the web graph to collect data.

#### Find Most Important Pages

##### Equal Coin Distribution:

- All are given same number of coins first.
- When one page is linked to another, the coins are distributed equally.
- After a while, the coins will be distributed based on the number of links.
- The page which has the most coins is the most important page.

##### Random Walk Coin Distribution:

- Start with a random page.
- Randomly walk to the next page based on the links and give it a coin.
- Repeat this process for a large number of steps.
- The page which has the most coins is the most important page.
- The distribution shown here is Power Law Distribution.
- Emergence of Inequality in Distribution of Coins over time.
- If we reach a dangling node, we will not be able to get out of it.
- To avoid this, we can use a teleportation factor (move to a random page with a certain probability).

### Grivan-Newman Algorithm

- Used to find communities in a graph.
- It works by removing edges from the graph and checking the connectivity of the graph.
- Monke see edge with high betweenness centrality, Monke remove it.

### Fatman Evolutionary Model

- A model that simulates the evolution of a social network.
- It is based on the idea that individuals in a social network are constantly forming and breaking connections with each other.
- The preferential attachment is driven by,
  - The degree of existing nodes.
  - The relative fitness of new nodes.

### Granovetter's Theory

- Weak ties are more important than strong ties.
- Strong ties are usually friends and family.
- Weak ties are acquaintances.
- We can get more information from weak ties than strong ties.

### Spatial Segregation

- The tendency of individuals to associate with others who are similar to them in some way.
- Increase in tolerance threshold will lead to decrease in segregation.

#### Shelling's Model

- A model that simulates the segregation of individuals in a social network.
- It is based on the idea that individuals have a preference for living near others who are similar to them.
- The individual WILL move if they are not satisfied with their current location.
- Steps:
  - Randomly place individuals in a grid.
  - Allow individuals to move to different locations based on their preferences.
  - Repeat until no one wants to move.
- Local decision making will lead to global segregation.

#### Linear Threshold Model

- It captures the diffusion of information in a social network.
- Each node has a threshold.
- When the number of neighbors that are active exceeds the threshold, the node becomes active.

### Structural Balance Theory

- I have two friends, and they dont like each other.
- Then I can convince both of them to be friends.
- If they dont become friends, then I will be friends with one of them and not the other.

#### Balance Theorem

- Only two sides will be present when fighting.
- When another is added, they will be forced to choose a side.
- Only two structurally balanced states are possible:
  - All positives.
  - Positive- Negative -Positive.

### Principle of Repeated Improvement

- The idea that individuals in a social network will continue to improve their connections until they reach a stable state.
- A points to B, if A gains popularity, B will also gain popularity and vice versa.

### Milgram's Experiment

- The small world phenomenon.
- The idea that individuals in a social network are connected by a small number of links.
- It shows that any two people in the world are connected by an avarage of six degrees of separation.
- The limitations of the experiment are:
  - The sample size was small (only in USA).
  - Many people did not respond to the letters.
  - Network was not random.

### Watts-Strogatz Model

- A model that simulates the small world phenomenon.
- It is based on the idea that individuals in a social network are connected by a small number of links.
- It works by starting with a regular graph and randomly rewiring some of the edges.
- The model has three parameters:
  - N: Number of nodes.
  - K: Number of neighbors.
  - P: Probability of rewiring an edge.
- The model shows that a small number of random connections can lead to a small world network.

### Kleinberg's Model

- It is a model of decentralized search in a social network.
- Links following a power law distribution with distance enables efficient search.

## Closures

### Triad Closure

- When one person has two friends, it is highly likely that the other two become friends.

### Foci Closure

- When two people have a common activity, they are likely to become friends.

### Structural Closure

- When one person has an activity, he makes his friend join the activity.

## Neighborhood Overlap

- Common neighbors that two nodes share.

## Bridge

- An edge connecting two components.

### Local Bridge

- Connects two nodes that have fewer or no connections between them or their neighbors.

### Structural Hole

- A gap between two components that aren't connected.
- Usually a BROKER helps in transfer of knowledge.

## Power Law

- Bell Curve only works when it is a sum of many random variables.
- Power Law is a distribution that is not normal.
- Graph:
  $$
  P(x) = \frac{1}{x^2}
  $$

## Social Capital

- The resources that are available to an individual through their social network.
- It can be used to gain access to information, opportunities, and support.

## Embeddedness

- If stranger meets, NO
- If stranger already knew some of our friends, YES
- The degree to which a relationship is supported by other relationships.

## Betweenness Centrality

- The number of times a node acts as a bridge along the shortest path between two other nodes.
- It is used to find the most important nodes in a network.
- The formula is:

  $$
  Betweenness Centrality = \sum_{i \neq j} \frac{\sigma_{st}(v)}{\sigma_{st}}
  $$

  where:

  - $v$ is the node.
  - $\sigma_{st}$ is the number of shortest paths from node $s$ to node $t$.
  - $\sigma_{st}(v)$ is the number of shortest paths from node $s$ to node $t$ that pass through node $v$.

## Homophily Index

- The tendency of individuals to associate and bond with similar others.
- The formula is:

  $$
  Homophily Index = \frac{\text{No of similar connections}}{\text{Total connections}}
  $$
