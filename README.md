### De Bruijn Graph Construction
This repository contains a Python implementation of a De Bruijn graph constructor. The algorithm builds a graph from a DNA sequence based on a given k value, where each node represents a (k-1)-mer and directed edges represent overlapping k-mers.

### Code Structure
The code consists of a single main function:

de_bruijn_graph(k, text)
Constructs a De Bruijn graph from a given DNA string and k-mer length.

### Parameters:

* k (int): Length of the k-mer.
* text (str): DNA sequence.

### Returns:

* A dictionary representing the graph. Each key is a (k-1)-mer, and its value is a list of (k-1)-mers that follow it in the sequence.

### Example Usage
```
# Sample input
k_value = 12
input_text = "TCCCGGTGAACAAGTTTTACTGGCC..."

# Generate the De Bruijn graph
result_graph = de_bruijn_graph(k_value, input_text)

# Print the result
for node, neighbors in result_graph.items():
    print(f"{node}: {' '.join(neighbors)}")

```

### Output Format
The graph is printed in the format:

<node>: <neighbor1> <neighbor2> ...
Where each line represents the outgoing edges from a (k-1)-mer node.

### Dependencies
This implementation uses only standard Python libraries and requires:
Python 3.x
No external packages are necessary.

### License
This project is licensed under the MIT License - see the LICENSE file for details.

