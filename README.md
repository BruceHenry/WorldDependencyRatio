# 2015-2100 World Population Data

A visualization of world population data from 2015 to 2100 using [D3.js](https://d3js.org/).
<br>
[<img src="https://gist.githubusercontent.com/BruceHenry/f9c8fdaa96182f18c5517a0d18323f40/raw/0c2763039f565f32412a994c7e437278bd687c43/thumbnail.png"/>](https://brucehenry.github.io/WorldPopulationData/)
<br>
[Have a look!](https://brucehenry.github.io/WorldPopulationData/)

Here is a video that introduces this project in details.([Link to Youtube](https://www.youtube.com/watch?v=vXrLY6MyOS8&t=14s))

***
## How to Use
- __Select the Data Type__<br>
In the data type selector (middle bottom of the map), you can select the data type you want from Population, Median Age, Total Dependency Ratio and Old Age Dependency Ratio.

- __Select Country__<br>
By clicking any country in the map or selecting in the country selector (right bottom of the map) , the age pyramid and the bar chart below will change according to your selection.

- __Select Year__<br>
By drag the bottom year bar or clicking the bars in the bar chart, you can select the year you want and the map will change according to your selection. 

## Introduction of Concept
- [Total dependency ratio](https://en.wikipedia.org/wiki/Dependency_ratio) is a measure showing the number of dependents, aged 0 to 14 and over the age of 65, to the total population aged 15 to 64. This indicator gives insight into the amount of people of nonworking age compared to the number of those of working age.
<br/><br/><img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/e7515ecc13b474b4953708350ad4197be7b6e40f"/>

- Old-age dependency ratio is aged over the age of 65, to the total population aged 15 to 64.
<br/><br/><img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/1864839236c02e2787c3fa2cac420edfcf8e5de2"/>

## Data Source
The data is from [United Nations: World Population Prospects 2017](https://esa.un.org/unpd/wpp/Download/Standard/Population/).

## Prototypes and Developing Stages
1. __Static Map__<br>
At first, I made a world map with 2050 Dependency Ratio data of each country. You can find it [here](https://bl.ocks.org/BruceHenry/1f282ffffdbf42d499b3ee034a4c23d1). 

2. __Selectable Year and Country__<br>
Since this prototype only shows one year (2050) of Dependency Ratio data, I want to start a project that allows user to select the year to see the change of data in different years. I think a range input `<input type="range">` would be a perfect choice for this year selector. Then I think clicking a country in the map to select a country is pretty good idea.

3. __Selectable Data__<br>
After accomplishing selectable year and country, what about showing more kinds of data. Then I add a data selector which enables users to select diferent kinds of data, and the map will be in different colors. I use Python to pre-process the data instead of processing multiple CSV files using D3.

## Deployment

This project uses NPM and Webpack. To get started, clone the repository and install dependencies like this:

```
cd WorldPopulationData
npm install
```

You'll need to build the JavaScript bundle using WebPack, using this command:

```
npm run build
```

To see the page run, you'll need to serve the site using a local HTTP server.

```
npm install -g http-server
http-server
```

Now the site should be available at localhost:8080.

For automatic refreshing during development, you can start the Webpack Dev Server like this:

```
npm run serve
```

## References
1. The idea of using bar chart comes from [UNHCR Historical Refugee Data](http://data.unhcr.org/dataviz/).
2. The idea of year range input is from [Custom range input slider with labels](https://codepen.io/trevanhetzel/pen/rOVrGK).
3. The map is built by [DataMaps](http://datamaps.github.io/).
