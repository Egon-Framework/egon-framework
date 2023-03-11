# Installation and Setup

## Installation and Setup

Official Egon releases are available via the pip package manager:

```bash
pip install egon
```

Alternatively, the latest development version can be downloaded and installed from [GitHub](https://github.com/Egon-Framework/egon):

```bash
pip install git+https://github.com/Egon-Framework/egon
```


## How it Works

Egon works by breaking down your analysis into discrete, reusable units. 
Those units can then be tested individually before being assembled and deployed as a single coherent pipeline. 
Consider the classic example of an ETL pipeline:


The pipeline shown above consists of three discrete steps, each of which are connected in a particular order. 
With Egon, this structure is represented as a collection of interconnected Node objects: 

Node objects can be connected in any order and are designed to run asynchronously. 
This means you can scale your analysis by allocating as many resources as necessary to each node. 
Nodes are also smart enough to automatically exit once they are no longer needed, freeing up resources on the host machine.