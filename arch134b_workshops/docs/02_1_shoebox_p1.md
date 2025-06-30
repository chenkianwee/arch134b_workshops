## Weather Data Visualization with Ladybug Tools

This tutorial demonstrates how to use the Ladybug plugin in Grasshopper to create a dashboard of climate analysis graphics from an EPW weather file. This process is fundamental for understanding the local climate and informing early-stage design decisions.

By the end of this tutorial, you will have created a set of visualizations in your Rhino viewport similar to the one below, which includes an hourly temperature plot, a wind rose, a monthly data chart, and a psychrometric chart for Van Nuys, California.

```{image} arch134b_workshops/_static/shoebox1/shoebox1_1.png
:width: 100%
:align: center
```

<br/><br/>

Step 1: Prepare Sun Path and Wind Rose Visualizations

The Sunpath and WindRose are two key components for site analysis. The Sunpath diagram helps visualize the sun's position throughout the year, crucial for daylighting and shading studies. The WindRose shows the direction, frequency, and speed of wind, which informs natural ventilation strategies.

Place the Ladybug_Sunpath and Ladybug_WindRose components on the Grasshopper canvas. We will connect data to their inputs later. Notice the various inputs that allow for customization of the graphics.

Generated {image} arch134b_workshops/_static/shoebox1/weather_2.png
:width: 100%
:align: center
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
{image} arch134b_workshops/_static/shoebox1/weather_2.png
IGNORE_WHEN_COPYING_END

<br/><br/>

Step 2: Set Up an Hourly Data Plot

Ladybug allows you to visualize any hourly data stream from the weather file. A common choice is the dry-bulb temperature, which shows the temperature fluctuations throughout the days and seasons.

Add the Ladybug_Hourly Plot component to the canvas.

To control where the plot appears in the Rhino viewport, connect a coordinate point to the _base_pt_ input. In this example, we use a panel with the coordinates -500, -80, 0. This will place the chart's bottom-left corner at that location.

Generated {image} arch134b_workshops/_static/shoebox1/weather_3.png
:width: 100%
:align: center
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
{image} arch134b_workshops/_static/shoebox1/weather_3.png
IGNORE_WHEN_COPYING_END

<br/><br/>

Step 3: Use Panels for Text Input

In Grasshopper, Panel components are essential for adding custom text, notes, or numerical data. We will use them to input file paths and coordinates.

To create a Panel, double-click on an empty part of the Grasshopper canvas.

A search bar will appear. Type "Panel" and press Enter, or select it from the list. An empty yellow panel will be created. You can then double-click the panel to edit its content.

Generated {image} arch134b_workshops/_static/shoebox1/weather_4.png
:width: 100%
:align: center
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
{image} arch134b_workshops/_static/shoebox1/weather_4.png
IGNORE_WHEN_COPYING_END

<br/><br/>

Step 4: Assemble the Core Visualization Script

Now, let's assemble the main part of our script. The entire process starts with importing the weather data.

The central component is Ladybug_Import EPW. The outputs of this component provide all the raw hourly data from the weather file.

Connect the desired data outputs from Import EPW to the _data inputs of the various charting components (HourlyPlot, MonthlyChart, PsychrometricChart). For example, connect dry_bulb_temperature to the HourlyPlot's _data input.

Use Panel components with different coordinates for each chart's _base_pt_ input to arrange them neatly in the Rhino viewport.

Generated {image} arch134b_workshops/_static/shoebox1/weather_5.png
:width: 100%
:align: center
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
{image} arch134b_workshops/_static/shoebox1/weather_5.png
IGNORE_WHEN_COPYING_END

<br/><br/>

Step 5: Locate and Copy the Weather File Path

Before the Import EPW component can work, it needs to know where to find the weather file on your computer. EPW files can be downloaded for free from sources like the DOE EnergyPlus website.

Using your computer's file explorer, navigate to the location where you saved your EPW file (e.g., USA_CA_Van.Nuys.AP.722886_TMYx.epw).

Right-click on the file and select "Copy as path". This copies the full file location to your clipboard.

Generated {image} arch134b_workshops/_static/shoebox1/weather_6.png
:width: 100%
:align: center
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
{image} arch134b_workshops/_static/shoebox1/weather_6.png
IGNORE_WHEN_COPYING_END

<br/><br/>

Step 6: Import the Weather Data into Grasshopper

The final step is to feed the copied file path into our Grasshopper script.

Add a Panel component to your canvas (as shown in Step 3).

Double-click the panel and paste (Ctrl+V) the file path you copied in the previous step. The panel should now contain the full path to your EPW file.

Connect the output of this Panel to the _epw_file input of the Ladybug_Import EPW component.

Once this connection is made, Ladybug will read the file, and all the connected visualization components will update to display the data, generating the complete dashboard in your Rhino viewport.

Generated {image} arch134b_workshops/_static/shoebox1/weather_7.png
:width: 100%
:align: center
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
{image} arch134b_workshops/_static/shoebox1/weather_7.png
IGNORE_WHEN_COPYING_END

<br/><br/>
