# Interative Map Demo 🗺️
![image](https://github.com/CS2613-FA23/explorationactivity2-anh-tran2106/assets/84007510/d6c51aa4-ddf5-410d-b6fd-b3a48b3faf29)

This repository is my work for the Exploration Activity #2 of CS2613 - Fall 2023 - University of New Brunswick. This is forked from a Github profile created by Github Classroom.

This demo's purpose is to demonstrates the use of the basic functionalities of [Leaflet](https://leafletjs.com/), allowing websites to display maps as well as interacting with them. It also makes use of [GeoDP Cities API](https://rapidapi.com/wirefreethought/api/geodb-cities) to navigate the map to a selected Canadian City.

## Getting Started

### Prerequisites

Once you clone the project, open ```index.html``` in a code editor and change the ```apiKey``` to your own API Key at ```line 71``` .

The line should look like this:
```
const apiKey = 'example API key';
```

To get your API key, you need to make an Account on [RapidAPI](https://rapidapi.com/wirefreethought/api/geodb-cities) and get your API Key there.

After this, right clicking on the ```index.html``` file should take you to a browser where you can see the demo in action.

## How to search

In order to search for a Canadian City, input the location in the field at the bottom of the screen in the following format:

```
City Name, Internationally Approved Alpha Code for Province/Territory
```

Press the **submit** button to perform the search.

You can see the full list of the internationally approved alpha codes [here](https://census.gc.ca/census-recensement/2021/ref/dict/tab/index-eng.cfm?ID=t1_8).

Some input examples:

```
Fredericton, NB
```

```
Moncton, NB
```

```
Toronto, ON
```
