K7434-2B2JE-6QJPH-RJDV6-UV9WA
clas_12 object structure

**Return hashmap array containing**

- *sector
- *superlayer
- *layer
- object[] unit - store Line3d Objects

```
	Use hash of these items as key for hashmap
	Map for each detector (different class for each)
```

- DC Class has 216 objects (sectors)
- Each of the 216 has unique key which will be stored in a map.
- Make a convenience method in the base class that takes a sector, supl, and layer and createa a hash that is used as a key to retrieve the data and compose an array to be returned back to the client.

**Interpreting data stream**

- Coordinates `x` `y` `z` are all points of a shape on a `3d` plane.
- they consist of `start` and `end` point locations as denoted by the `xml` data.
- The first points of these fields correspond to each other. Gathering this data to interpret this plane using an array of the string of data split by spaces would consist of a similar implementation `x[0], y[0], z[0]`.
- The sample `xml` feed contains `288` layers

**The xml data feed consists of 288 layers, each assigned to sectors 1 through 6**. `Make a java class called Sector that contains all of the layers pertaining to that specific sector. Each of these layers will retain all of the data from the xml feed.`

Sectors 0 - 5
Regions 0 - 2
