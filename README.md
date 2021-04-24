# 🦠 Covid 19 Dashboard - A Dashboard Cum Web App 🦠

Checkout the dashboard app here -- https://covid-streamlit-2021.herokuapp.com/
<br>

![](https://www.calexico.ca.gov/vertical/Sites/%7B342ED706-1EBB-4FDE-BD1E-9543BAD44C09%7D/uploads/COVID.jpg)

Coronaviruses or Covid-19 are a large family of viruses that may cause respiratory illnesses in humans ranging from common colds to more severe conditions such as Severe Acute Respiratory Syndrome (SARS) and Middle Eastern Respiratory Syndrome (MERS).

• 'Novel coronavirus' is a new, previously unidentified strain of coronavirus.

• The novel coronavirus involved in the current outbreak has been named SARS-CoV-2 by the World Health Organization (WHO).

• The disease it causes has been named “coronavirus disease 2019” (or “COVID-19”).

## Primary objectives
* Basic options for users to choose
  * Cumulative or daily changes measures
  * Global aggregate stat or per-country information
* Display a basic statistics for selected area (Global or for specific country)
* Draw a heatmap detailing given a region and measure (e.g., Daily infections increases in the US)
* Draw a Choropleth with the same selection (Country-level or state-level comparisons)

## Data sources and helpful resources
* Data sources
  * [Johns Hopkins University Github](https://github.com/CSSEGISandData/COVID-19): Global nCov-19 dataset
  * [KCDC](http://ncov.mohw.go.kr/): South Korean dataset providing provincial-level details
  * [NaturalEarth](http://naturalearthdata.com/): Geographical shapedata for countries (admin0) and states-level (admin1) data to be used (1:10m data is used for selected countries for states details while 1:50m used for others)
* Useful resources
  * [polygon conversion](https://gist.github.com/mapmeld/8742ae89c6d687171d00/): To convert `MultiPolygon` geojson to `Polygon` form (Nick Doiron)
  * [simplify](https://philmikejones.me/tutorials/2016-09-29-simplify-polygons-without-creating-slivers/): Using rmapshaper::simplify() in R to greatly reduce file sizes (Phil Mickey Johns)
  * [dissolve](https://philmikejones.me/tutorials/2015-09-03-dissolve-polygons-in-r//): Merge small-scale districts into larger level ones (e.g., counties -> states) (Phil Mickey Johns)

## Descriptions of objects
* Heatmap
  * Two separate charts are drawn, one for infections and the other for casaulties
  * Regions on y-axis are pre-sorted by the figures (ordered in a descending manner for top-25 disricts)
* Choropleth
  * Both measures are drawn on a single choropleth (casualties on top of infections)
  * Infections are shown by the color depth while casualties are represented by elevations of the regions
  
## Selected modules used
  * [Altair](http://altair-viz.github.io/): Altair chart module used to draw heatmap (`streamlit.altair_chart`)
  * [Pydeck](http://pydeck.gl/): Pydeck mapping module used to draw Choropleth/PolygonLayer (`streamlit.pydeck_chart`)


### Prerequisites

You need to have the following dependecies before running the app:

- pandas `pip install pandas`
- numpy `pip install numpy`
- scipy `pip install scipy`
- plotly `pip install plotly`
- streamlit `pip install streamlit`
- streamlit-folium `pip install streamlit-folium`
- datetime `pip install DateTime`


### Usage

1. Install all dependencies mentioned in __Prerequisites__.
2. Open CLI/prompt and make sure Streamlit is installed by running the command `streamlit --version`. You should see something like this : `Streamlit, version 0.67.1`.
3. Do this for all other dependencies as well just to make sure everything is in right place and you are good to go.
4. Go to your working directory(where you have placed the .py file and other components) and open CLI.prompt there.
5. Type in the following command and press Enter :<br>
   `streamlit run app.py`<br>
   Please wait for 5-10 seconds for command to run.

## Authors

1. Yashaswi Singh (https://www.linkedin.com/in/yashaswi-singh1/)
2. Swaroop Gupta (https://www.linkedin.com/in/swaroopgupta/)
