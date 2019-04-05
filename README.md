# Useful Overpass Queries
[Overpass-turbo](http://overpass-turbo.eu/) is a great to quickly get data and stats from OpenStreetMap.

## Newer than
* get the objects which have been added to OpenStreetMap since a specific timestamp
* copy these lines to overpass-turbo
  ```
  [out:json][timeout:600];
  // gather results
  (
    node(newer:"2019-04-05T16:00:00Z")({{bbox}});
    way(newer:"2019-04-05T16:00:00Z")({{bbox}});
    relation(newer:"2019-04-05T16:00:00Z")({{bbox}});
  );
  // print results
  out meta;
  >;
  out skel qt;
  ```
* adjust the timestamp
* draw a bounding box for the area you are interested in
