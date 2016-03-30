# Gremlin 2 to 3 migration 

A humble help to move code from Gremlin 2 to Gremlin 3. 

## API matches
List of Gremlin 2 API, and their Gremlin 3 equivalent (or not).

All examples given in the context of the Modern Graph:
```
graph = TinkerFactory.createModern()
g = graph.traversal()
```

###_

###both
Same as in Gremlin 2.

###bothE
Same as in Gremlin 2.

###bothV
Same as in Gremlin 2.

###cap
Same as in Gremlin 2.

###E
Same as in Gremlin 2. Unless using 'Sugar plugin', don't omit the parenthesis.

Gremlin 3 :

```gremlin3
gremlin> g.E().count()
==>3
```

Gremlin 2 :

```gremlin2
gremlin> g.E().count();
==>2

// This is not possible without sugar plugin
gremlin> g.E.count();
==>2

```


###gather

###id

###in

###inE

###inV

###key

###label

###linkBoth[In/Out]

###map

###memoize

###order

###orderMap

###out

###outE

###outV

###path

###scatter

###select

###shuffle

###transform

###V

###[i]

###[i..j]

###and

###back

###dedup

###except

###filter

###has

###hasNot

###interval

###or

###random

###retain

###simplePath

###aggregate

###as

###groupBy

###groupCount

###optional

###sideEffect

###store

###table

###tree

###Branch

###copySplit

###exhaustMerge

###fairMerge

###ifThenElse

###loop

###Element.keys

###Element.remove

###Element.values

###Graph.addEdge

###Graph.addVertex

###Graph.e

###Graph.idx(String)

###Graph.load

###Graph.removeEdge

###Graph.removeVertex

###Graph.save

###Graph.v

###Index[Map.Entry]

###Pipe.enablePath

###Pipe.fill

###Pipe.iterate

###Pipe.next





## Recipes
/* Alphabetical order */


###Duplicate Edges

###Finding Edges Between Vertices

###Happy Birthday

###Hiding Console Output

###Paging Results

###Reading From a File

###Sampling

###Shortest Path

###Subgraphing

###Using External Classes

###Writing To File

### How to get a range within a collection of steps?

Use the 'range()' step.

Gremlin 3 :
```gremlin3
gremlin> g.V().range(0, 2).property().value('name')
==>lop
==>vadas
==>marko
```

Gremlin 2 :
```gremlin2
gremlin> g.V[0..2].name
==>lop
==>vadas
==>marko

// This is not possible anymore
gremlin> g.V[0..<2].name
==>lop
==>vadas

```


##### Annex

### Gremlin 3

* [TinkerPop3 Documentation](http://tinkerpop.apache.org/docs/3.1.1-incubating/reference/) - TinkerPop3 Documentation
* [TinkerPop Upgrade information](http://tinkerpop.apache.org/docs/3.1.1-incubating/upgrade/#_tinkerpop_3_1_1) - Upgrade information
* [Gremlin (Programming language)](https://en.wikipedia.org/wiki/Gremlin_(programming_language)) - Wikipedia on Gremlin



### Gremlin 2

* [Gremlindocs](http://gremlindocs.com/ ) - Gremlin Docs with examples
