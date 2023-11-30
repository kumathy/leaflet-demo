# Library Overview

## Library Selection

For this Exploration Activity, I decided on **Leaflet** as my library of choice to research on. 

## Leaflet

**Leaflet** is a JavaScript library for interactive maps. It provides a lightweight, simple and easy-to-use framework for creating interactive maps on web pages.

## Functionalities

For my sample project, I created an interactive map demo where you can interact with the world map, choose different map layers, toggle marker and navigate to a selected Canadian City. the features used are listed below:

1. Initiating the map with the map layer of your choice with the `map` class.

```
var map = L.map('map').setView([45.9636, -66.6431], 14);

// OpenStreetMap layer
var openStreetMap = L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
});

openStreetMap.addTo(map);
```

2. Add a marker to display clickable icons on the map with `L.Marker`. Clicking on the icon shows a popup with some text.

```
// Marker
var myIcon = L.icon({
iconUrl: 'img/red_marker.png',
iconSize: [55, 55],
});
var marker = L.marker([45.9636, -66.6431], {icon: myIcon});
var popup = marker.bindPopup("Fredericton - " + marker.getLatLng()).openPopup()

popup.addTo(map);
```

3. Creating a layer controller with `L.control.layers` that allows users to switch between map layers and make the marker visible or not.

```
// Layer Controller
var baseMaps = {
    "OpenStreetMap": openStreetMap,
    "Google Streets": googleStreets,
    "Google Satellite": googleSatellite,
    "Google Terrain": googleTerrain,
    "Light": light,
    "Dark": dark
};

var overlayMaps = {
    "Marker": marker
};

var layerControl = L.control.layers(baseMaps, overlayMaps, {collapsed: false});
layerControl.addTo(map);
```
4. Use the `mousemove` MouseEvent to get the coordinates of the mouse and show it on the screen.

```
// Leaflet Event
map.on('mousemove', function(e){
    document.getElementsByClassName("coordinate")[0].innerHTML = `(${e.latlng.lat}, ${e.latlng.lng})`;
    console.log(`lat: ${e.latlng.lat}, lng: ${e.latlng.lng}`);
})
```

## When was Leaflet created

Leaflet was created in 2010 by Vladimir Agafonkin - a Russian software developer. It was first release in 2011 and has since gained popularity for its simplicity, versatility, and active developer community.  [[1]](https://en.wikipedia.org/wiki/Leaflet_(software)#:~:text=Leaflet%20began%20life%20in%202010,of%20the%20old%20API%20code.).

## Why I chose Pyglet

For this Exploration Activity, I wanted to find a library that is fun and interactive to research on, which Leaflet perfectly fits this description for me.

Additionally, I thought of the idea of using GeoDP Cities API [[2]](https://rapidapi.com/wirefreethought/api/geodb-cities) to search for a city, and how it would complement very well with this project, and I thought this would give me a great opportunity to learn how to use multiple libraries and APIs together.

## Reflection

### influence in learning JavaScript

This experience has definately improve my understanding of JavaScript, as well as helping me familiarize with html and css styling as well. It is very important in web development to be able to use these 3 tools well and I feel that I've gained a lot of valuable experience for them with this project.

### Overall experience

Overall, I enjoyed my experience learning Leaflet as well as getting a web page working. My work for this project took longer expected however, as I had to do some extra research on html, css styling as well as getting the GeoDP Cities API to work. For JavaScript PQ3, we used **axios** [[3]](https://axios-http.com/docs/intro) for API requests which I had some trouble getting it to run on web browsers, so I had to look into how to use **XMLHttpRequest** [[4]](https://en.wikipedia.org/wiki/XMLHttpRequest) instead.

In conclusion, I had a lot of fun messing with the features of Leaflet and getting the web page working. I would highly recommend anyone who wants an interactive and satisfying learning experience on how to use JavaScript libraries to give Leaflet a try.

## References
[1] [https://en.wikipedia.org/wiki/Leaflet_(software)#:~:text=Leaflet%20began%20life%20in%202010,of%20the%20old%20API%20code.](https://en.wikipedia.org/wiki/Leaflet_(software)#:~:text=Leaflet%20began%20life%20in%202010,of%20the%20old%20API%20code.)

[2] [https://rapidapi.com/wirefreethought/api/geodb-cities](https://rapidapi.com/wirefreethought/api/geodb-cities)

[3] [https://axios-http.com/docs/intro](https://axios-http.com/docs/intro)

[4] [https://en.wikipedia.org/wiki/XMLHttpRequest](https://en.wikipedia.org/wiki/XMLHttpRequest)
