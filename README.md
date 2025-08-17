# L.Donut

Makes it possible to draw donuts with `L.Donut` on Leaflet maps. 

It extends `L.Circle` and adds a inner radius. Look into the [Demo](https://falke-design.github.io/L.Donut/).



![grafik](https://user-images.githubusercontent.com/19800037/139536038-b0d85d7d-461c-490f-94a9-5956677bab0b.png)

## Leaflet V1+

```js
var donut = new L.Donut(map.getCenter(),{
  radius: 2000,
  innerRadius: 1000,
  innerRadiusAsPercent: false,
}).addTo(map);
```

### Installation

Download **L.Donut.js** and include them in your project.
```html
<script src="./src/L.Donut.js"></script>
```
or use the script over cdn:
```html
<script src="https://cdn.jsdelivr.net/gh/Falke-Design/L.Donut@latest/src/L.Donut.js"></script>
```

## Leaflet V2+

```js
import {Donut} from 'leaflet-donut';

var donut = new Donut(map.getCenter(),{
  radius: 2000,
  innerRadius: 1000,
  innerRadiusAsPercent: false,
}).addTo(map);
```

### Installation

Download **L.Donut-leaflet-v2.js** and include them in your project.
```html
<script type="importmap">
  {
      "imports": {
          "leaflet": "https://unpkg.com/leaflet@2.0.0-alpha.1/dist/leaflet.js",
          "leaflet-donut": "./src/L.Donut-leaflet-v2.js"
      }
  }
</script>
```
or use the script over cdn:
```html
<script type="importmap">
  {
      "imports": {
          "leaflet": "https://unpkg.com/leaflet@2.0.0-alpha.1/dist/leaflet.js",
          "leaflet-donut": "https://cdn.jsdelivr.net/gh/Falke-Design/L.Donut@latest/src/L.Donut-leaflet-v2.js"
      }
  }
</script>
```

## Methods:

You can use `new L.Donut`

| Method                              | Returns   | Description                                                                                                                |
| :---------------------------------- | :-------- | :------------------------------------------------------------------------------------------------------------------------- |
| L.Donut(`latlng`,`options`)         | `this`    | Creates the Donut shape.                                                                                                   |
| setInnerRadius(`radius`)            | `this`    | Sets the inner radius of a circle. Units are in meters or percent. The outer radius must be greater then the inner radius. |
| getInnerRadius()                    | `Number`  | Returns the current inner radius of a circle. Units are in meters or percent.                                              |

## Options:

| Option                              | Description                                                                               |
| :---------------------------------- | :---------------------------------------------------------------------------------------- |
| radius                              | Outer radius. The outer radius must be greater then the inner radius.                     |
| innerRadius                         | Inner radius. It can be a meter value or a percent (0-1) value of the outer radius.       |
| innerRadiusAsPercent                | Default `false`. Defines if the inner radius is a percent value of the outer radius.      |
| <`L.Circle` options>                | Other `L.Circle` options: [Docs](https://leafletjs.com/reference.html#circle)             |
