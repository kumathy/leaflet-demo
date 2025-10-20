# <p align="center">Interactive Map Demo 🗺️</p>

<p align="center">
  <img alt="Leaflet" src="https://img.shields.io/badge/Leaflet-199900?style=for-the-badge&logo=leaflet&logoColor=white">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">
  <img alt="HTML5" src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
</p>

<p align="center">
  <img src="https://github.com/CS2613-FA23/explorationactivity2-anh-tran2106/assets/84007510/d6c51aa4-ddf5-410d-b6fd-b3a48b3faf29" alt="Interactive Map Screenshot" width="700"/>
</p>

<p align="center">An interactive map web app built with 
  <a href="https://leafletjs.com/">Leaflet.js</a> and the 
  <a href="https://rapidapi.com/wirefreethought/api/geodb-cities">GeoDB Cities API</a> to explore Canadian cities 🇨🇦 🏙️
</p>

> [!NOTE]
> This project was created for **CS2613 Exploration Activity #2** (Fall 2023 - UNB). It demonstrates basic integration between the **Leaflet.js mapping library** and the **GeoDB Cities API** to create an interactive, browser-based map.

## Getting Started

### Prerequisites
- A **GeoDB Cities API key** from [RapidAPI](https://rapidapi.com/wirefreethought/api/geodb-cities)

### Installation

1. **Clone this repository**
```bash
git clone https://github.com/kumathy/leaflet-demo.git
```

2. **Navigate to the project directory**
```bash
cd leaflet-demo
```

3. **Add your API key**

> In index.html, replace the placeholder (around line 71) with your key:
```js
const apiKey = 'YOUR_API_KEY_HERE';
```

4. **Run the demo**

> Open index.html in your browser:
```bash
open index.html
```

## How to search
Enter a location of a Canadian City in this format:
```
City Name, Province/Territory Alpha Code
```

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

📘 Full list of internationally approved alpha codes [here](https://www12.statcan.gc.ca/census-recensement/2021/ref/dict/tab/index-eng.cfm?ID=t1_8).

