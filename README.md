# 🌲 FP Tree

The initial itemsets of the database are used to create the tree-like structure known as the frequent pattern tree. The FP tree's goal is to extract the most common pattern. An item from the itemset is represented by each node of the FP tree.

## 📐 Project Setup
```
git clone https://github.com/ROCCYK/FPTree
pip install wikipedia-api
import wikipediaapi
```

## 🖥 How to use

### Create an Object of wikipediaapi()
```
wiki_wiki = wikipediaapi.Wikipedia(language='en', extract_format=wikipediaapi.ExtractFormat.WIKI)
```

### Create a list of wikipedia pages
```
wiki = ["Genetic algorithm", "A* search algorithm", "Search tree", "Recursion (computer science)", "Linear search"]
```

### Create an Object of FPTree()
```
test = FPTree()
```

### Extract page data from FPTree()
```
data = test.getData(wiki)
```

### Create FPtree and HeaderTable from FPTree()
```
FPtree, HeaderTable = test.makeTree(data)
```

### Create a list to store frequent item set
```
frequent_itemset = []
```

### Mine FPTree()
```
test.mine(FPtree, HeaderTable, 5, set([]), frequent_itemset)
```

### View frequent item set list and display tree
```
print("All frequent itemsets:")
print(frequent_itemset)

print(FPtree.display())
```
