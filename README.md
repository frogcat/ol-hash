# ol-hash
Simple OpenLayers plugin to save map view state in URL hash

# usage

```html
<!doctype html>
<html lang="en">
  <head>
    <link rel="stylesheet" href="https://openlayers.org/en/v4.3.4/css/ol.css" type="text/css">
    <style>
      .map {
        height: 400px;
        width: 100%;
      }
    </style>
    <script src="https://openlayers.org/en/v4.3.4/build/ol.js" type="text/javascript"></script>

    <!-- Step2. import ol-hash.js -->
    <script src="ol-hash.js"></script>
    <title>OpenLayers example</title>
  </head>
  <body>
    <h2>My Map</h2>
    <div id="map" class="map"></div>
    <script type="text/javascript">
      var map = new ol.Map({
        target: 'map',
        layers: [
          new ol.layer.Tile({
            source: new ol.source.OSM()
          })
        ],
        view: new ol.View({
          center: ol.proj.fromLonLat([37.41, 8.82]),
          zoom: 4
        })
      });
      // Step2: call ol.hash(map)
      ol.hash(map);
    </script>
  </body>
</html>
```
