# Unit 16 | Assignment - Data Journalism and D3

## Background

The editor wants to run a series of feature stories about the health risks facing particular demographics by sifting through the latest information from the U.S. Census Bureau and the Behavioural Risk Factor Surveillance System.

## Task

### Level 1: D3 Dabbler

Find a correlation between two data variables, each measured state by state and taken from different data sources and then visualize the correlation with a scatter plot and embed the graphic into an .html file. Accomplish these in four steps as shown below.

#### 1. Find the Data

Look for demographic information using the 2014 one-year estimates from the U.S. Census Bureau's American Community Survey. Specify your information using the [American FactFinder](http://factfinder.census.gov/faces/nav/jsf/pages/searchresults.xhtml) tool. When searching through the data, be sure to select these options in the left sidebar:

* Topics -> Dataset -> 2014 ACS 1-year estimates

* Geographies -> Select a geographic type -> State - 040 -> All States within United States and Puerto Rico

Next, Search for data on health risks using 2014 survey data from the [Behavioral Risk Factor Surveillance System](https://chronicdata.cdc.gov/Behavioral-Risk-Factors/BRFSS-2014-Overall/5ra3-ixqq). 

#### 2. Format and Test the Data

Format data for D3. With two data types chosen, grab the value columns from each and paste them into a new Excel document. Create header names that  can be easily accessed with JavaScript (concise, lower cased, camelCased). Make sure that rows and columns line up — You may need to delete Guam from your data sheet so that your Census and BRFSS data matches.

Test for correlation with Excel's `=CORREL()` function. Value must be either less than -0.5 or more than 0.5—these values would indicate a moderate correlation and a story that might be worth pursuing (shoot for -0.75 or 0.75 if possible).

When a suitable match is found, delete any correlation cells from sheet and save the file as `data.csv`. Place it in the `data` folder.

#### 3. Visualize the Data

Using the D3 techniques, create a scatter plot that represents each state with circle elements. Code this graphic in the `app.js` file and pull in the data from `data.csv` by using the `d3.csv` function. 

* The x-values of the circles should match the demographic census data, while the y-values should represent the risk data.

* Include state abbreviations in the circles.

* Create and situate your axes and labels to the left and bottom of the chart.

* Generate this chart in the `d3.html` file in your assignment directory.

* Note: You'll need to use `http-server` to display the graphic since you're pulling data in from a source outside of your app.js file.

#### 4. Embed into an iframe

Embed `d3.html` in `index.html` with an iframe. Add a quick written analysis of data below the graphic.