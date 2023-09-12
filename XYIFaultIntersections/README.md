# XYI Fault Intersections Detection

Based on Manzocchi (2002)

## Preliminar SQL-MM Workflow and Code

1. Fault traces must be digitized in a arc-node topology fashion. That means fault intersections must be recognized and we cannot have
  undershoots or overshoots with dangling nodes.

2. Recognize nodes

```
  select distinct geometry  from 
  (
    select endpoint(geometry) geometry from <faultLayer>
  union
    select startpoint(geometry) geometry from <faultLayer>
  )

```
3. Save resulting node layer (nodeLayer)
4. Detection of Fault-Node Intersections

```
  select  b.geometry geometry, b.fid, a.pk_UID, count(*) n_arcs,
    case
	    when count(*) = 1 THEN 'I'
	    when count(*) = 2 THEN ''
	    when count(*) = 3 THEN 'Y'
	    when count(*) >= 4 THEN 'X'
    end
  as nodeType 
  from <faultLayer> as a, <nodeLayer> as b
	where touches(b.geometry, a.geometry)
	group by b.fid order by b.fid

```

This code will work if an unique identifier is selected both for fault layer and node layer.

## Expected Map Result 

![X, Y, I Nodes Detection](result230912.jpg).

## Connectivity Triangular Diagram

To be done!!

## Density Map of I and XY

It is suggested to use Heat Map Tools, until something more analytical tools will be implemented.

![X, Y, I Nodes Density Map](resultHeatMap230912.jpg).


## References
Manzocchi, T. 2002. The connectivity of two-dimensional networks of spatially 
correlated fractures. Water Resources Research, 38 (9), pp 1162.


