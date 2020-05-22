Consulta en Overpass para contar poligonos


/*

[out:csv("name";false)];
[out:json][timeout:25];
*/

[out:json][timeout:25];
// gather results
(
  // query part for: “leisure=playground and access!=no and access!=private”
  way["source"="cidi"](user:"Marliz94")(changed:"2020-05-18T00:00:00Z","2020-05-19T00:00:00Z" )({{bbox}});
);
// print results
out body;
>;
out skel qt;

