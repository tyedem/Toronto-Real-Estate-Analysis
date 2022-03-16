Pythonic Monopoly

![Toronto at night](Images/toronto.jpg)

*[Photo by James Wheeler](https://www.pexels.com/@souvenirpixels?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels) | [Free License](https://www.pexels.com/photo-license/)*

## Background

Harold's company has just started a new Real Estate Investment division to provide customers with a broader range of portfolio options. Harold was tasked with building a prototype dashboard, and he needs your help. The real estate team wants to trial this initial offering with investment opportunities for the Toronto market. If the new service is popular, then they can start to expand to other markets.

This dashboard's goal is to provide charts, maps, and interactive visualizations that help customers explore the data and determine if they want to invest in rental properties in Toronto.

In this homework assignment, you will help Harold accomplish the following tasks:

1. [Complete a notebook of rental analysis](#Rental-Analysis)

2. [Create a dashboard of interactive visualizations to explore the market data](#Dashboard)

The data provided for this homework was retrieved from the following websites:

* [Toronto Open Data](https://open.toronto.ca/)

* [Census Profile, 2016 Census - Toronto Metropolitan Area, Ontario and Canada](https://www12.statcan.gc.ca/census-recensement/2016/dp-pd/prof/details/page.cfm?Lang=E&Geo1=CMACA&Code1=535&Geo2=PR&Code2=01&SearchText=toronto&SearchType=Begins&SearchPR=01&B1=All&TABID=1&type=0)


**Note:** If you encounter technical difficulties using PyViz, refer to the troubleshooting section of the [PyViz Installation Guide](PyVizInstallationGuide.md).

---

## Files

* [toronto_neighbourhoods_census_data.csv](Starter_Code/Data/toronto_neighbourhoods_census_data.csv)

* [toronto_neighbourhoods_coordinates.csv](Starter_Code/Data/toronto_neighbourhoods_coordinates.csv)

* [Rental Analysis Starter Jupyter Notebook](Starter_Code/rental_analysis.ipynb)

* [Dashboard Starter Jupyter Notebook](Starter_Code/dashboard.ipynb)

## Instructions

### Rental Analysis

The first step to building the dashboard is to work out all of the calculations and visualizations in an analysis notebook. Once the code is running properly, it can be copied over to a dashboard code and used with Panel to create the final layout. Use the `rental_analysis.ipynb` to complete the following:

#### Dwelling Types Per Year

In this section, you will calculate the number of dwelling types per year and visualize the results as a bar chart using the Pandas plot function.

**Note:** By default, the colour of the bar charts is blue. However, it is hard to see the difference between the yearly data.

As an optional challenge, you can manually use the `color` parameter of the `plot()` function to change the colour of each bar chart.

| Default Bar Charts                                  | Colored Bar Charts                                   |
------------------------------------------------------|------------------------------------------------------|
|![default_bar_charts](Images/default_bar_charts.png) | ![colored_bar_charts](Images/colored_bar_charts.png) |

#### Average Monthly Shelter Costs in Toronto Per Year

In this section, you want to visualize the average monthly shelter costs per year to understand rental income trends over time better. You will visualize the average (mean) shelter cost for owned and rented dwellings per year and visualize it as line charts.

As an optional challenge, you can plot each line chart in a different colour.

1. Calculate the average monthly shelter costs for owned and rented dwellings for each year.

2. Visualize the monthly shelter costs per year as line charts.

    ![gross-rent.png](Images/gross-rent.png)

#### Average House Value per Year

In this section, you want to determine the average house value per year. An investor may want to better understand the sales price of the rental property over time. For example, a customer will want to know if they should expect an increase or decrease in the property value over time so they can determine how long to hold the rental property. You will visualize the `average_house_value` per year as a bar chart.

1. Calculate the mean `average_house_value` for each year.

2. Visualize the `average_house_value` per year as a line chart.

  ![average-sales.png](Images/average-sales.png)

#### Average Prices By Neighbourhood

In this section, you want to compare the house value by neighbourhood.

1. Create a new DataFrame with the mean house values by neighbourhood per year.

2. Visualize the mean `average_house_value` per year with the neighbourhood as a dropdown selector.

**Hint:** Use `hvplot` to obtain the interactive dropdown selector for the neighbourhood.

  ![avg-price-neighbourhood.png](Images/avg-price-neighbourhood.png)

#### Number of Dwelling Types per Year

In this section, you want to visualize the number of dwelling types per year in each neighbourhood. You want to provide investors a tool to understand the evolution of dwelling types over the years.

**Hint:** Use `hvplot` to create an interactive visualization of the average number of dwelling types per year with a dropdown selector for the neighbourhood.

![dwelling_types_per_year](Images/dwelling_types_per_year.png)

#### Top 10 Most Expensive Neighbourhoods

In this section, you want to figure out which neighbourhoods are the most expensive. You will need to calculate the mean house value for each neighbourhood and then sort the values to obtain the top 10 most expensive neighbourhoods on average. Plot the results as a bar chart.

![top-10-expensive-neighbourhoods.png](Images/top-10-expensive-neighbourhoods.png)

#### Neighbourhood Map

In this final section, you will read in neighbourhood location data and build an interactive map with the average prices per neighbourhood. Use a scatter Mapbox object from Plotly express to create the visualization. You will need your Mapbox API key for this.

Remember that to create maps visualizations using Plotly Express, you will need to create an account at [mapbox](https://www.mapbox.com/) and [create an access token](https://docs.mapbox.com/help/how-mapbox-works/access-tokens/#creating-and-managing-access-tokens).

  ![neighbourhood-map.png](Images/neighbourhood-map.png)

#### Cost Analysis (Optional Challenge)

Plotly express offers a broad selection of interactive plots. In this optional challenge section, you will use Plotly express to create a couple of plots that investors can interactively filter and explore various factors related to the house value of Toronto's neighbourhoods.

1. Create a bar chart row facet to plot the average house values for all Toronto neighbourhoods per year.

    **Hint:** You can learn more about facet plots in Plotly Express in [this link](https://plotly.com/python/facet-plots/).

   ![bar_chart_row](Images/bar_chart_row.png)

2. Create a sunburst chart to conduct a cost analysis of the most expensive neighbourhoods in Toronto per year.

    **Hint:** You can learn more about sunburst charts in Plotly Express in [this link](https://plotly.com/python/sunburst-charts/).

    ![sunburst](Images/sunburst.png)

### Dashboard

Now that you have worked out all of the code and analysis, you will use the Panel library to build an interactive dashboard for all of the visualizations. There are no hard requirements for the layout of this dashboard, so use your imagination and creativity!

Use the `dashboard.ipynb` starter notebook for your dashboard code. Copy over the code for each visualization and place this into separate functions (1 function per visualization). This will make it easier to build and modify the layout later. Each function should return the plot figure in a format that Panel can use to plot the visualization.

Sample Dashboard:

  ![dashboard-demo.gif](Images/dashboard-demo.gif)
