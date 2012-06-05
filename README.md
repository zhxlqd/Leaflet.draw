#Leaflet.draw
Adds support for drawing polys to Leaflet.

This plugin is based on @brunob's [draw plugin](https://github.com/brunob/leaflet.draw). I decided to create a new repo rather than forking as I wanted to take the coding style and functionality in a different direction.

#Using the plugin
If you are happy with the control being displayed below the zoom controls just set ````polyDrawControl = true```` when declaring your Leaflet map.

E.g.:

````
var cloudmadeUrl = 'http://{s}.tile.cloudmade.com/BC9A493B41014CAABB98F0471D759707/997/256/{z}/{x}/{y}.png',
cloudmade = new L.TileLayer(cloudmadeUrl, {maxZoom: 18}),
map = new L.Map('map', {layers: [cloudmade], center: new L.LatLng(-37.7772, 175.2756), zoom: 15, polyDrawControl: true });
````

If you would like to reposition the control or turn off poly type add the control manually:

````
var drawControl = new L.Control.Draw({
	position: 'topright',
	drawPolyline: false
});
map.addControl(drawControl);
````

See [example/map-polydraw.html](https://github.com/jacobtoye/Leaflet.iconlabel/blob/master/example/map-marker-iconlabels.html) for a working example.

#Official support
Leaflet plan to include drawing in 0.4 so this is just a band-aid until it comes. See https://github.com/CloudMade/Leaflet/issues/174