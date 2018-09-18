# JS-2DPolygon
2D polygon class written in javascript (ES6 syntax). Includes some common 2D functions.

The class stores the polygon points as an array of standard JS Objects with the props: 
```javascript
point = {
  x: //x coord, 
  y: //y coord 
}
```
So create a Polygon it's as simple as:
```javascript
var myPolygon = new PGM2DPolygon([point1, point2...]);
```

Or you could also do:
```javascript
var myPolygon = new PGM2DPolygon();
myPolygon.addPoint(point1);
myPolygon.addPoint(point2);
myPolygon.addPoint(point3);
//...
```
Once you'd created the polygon you have point-polygon inclusion tests with orientation independence and working with convex and non-convex polygons. 
You'll simply call: 
```javascript
myPolygon.isInside({x:some coord, y:some coord})
```

For convenience it's also included the classical ray intersections inclusion test, only works with convex polygons but can be more perfomant.
You could use it as: 
```javascript
myPolygon.isInsideConvex({x:some coord, y:some coord})
```
