# Specifying Heating and Cooling Setpoint Schedule and HVAC Type
Setpoint schedules are often dynamic based on occupancy. In office spaces for example, on the weekends and nights the space is allowed to warm outside of comfotable levels because noone is there. 

## Disconnect setpoint definition introduced in Module 4
```{image} ../_static/spec2/spec2_1.png
:width: 100%
:align: center
```
<br/><br/>

## Route program definition through new "Program Type" component
```{image} ../_static/spec2/spec2_2.png
:width: 100%
:align: center
```
<br/><br/>

## Creating weekly setpoint schedules
Above, in a new block, create the "Apply Setpoint" and two "Weekly Schedule" components as shown. One will be for heating and the other will be for cooling.

```{image} ../_static/spec2/spec2_3.png
:width: 100%
:align: center
```
<br/><br/>

## Hourly setpoint specification
Add and adust setpoint values for weekday and weekend schedules as shown. Do not connect before adjusting otherwise it will simulate after each update and take a long time. 

```{image} ../_static/spec2/spec2_4.png
:width: 100%
:align: center
```
<br/><br/>

## Add type limits for each weekly shedule as shown to avoid errors.
```{image} ../_static/spec2/spec2_5.png
:width: 100%
:align: center
```
<br/><br/>

## Connect your "Setpoint" block to your "Program Type"
This should cause a new simulation to run. Try to guess if your new setpoints will lower or raise EUI. 

```{image} ../_static/spec2/spec2_6.png
:width: 100%
:align: center
```
<br/><br/>

## Specifying HVAC System Type
You can define other HVAC System Types using components found in the HVAC tab in HB-Energy. 

```{image} ../_static/spec2/spec2_7.png
:width: 100%
:align: center
```
<br/><br/>

## Linking the HVAC Type component
Here is how to link the HVAC Type component to the rest of your simulation. Try different types and see how your EUI changes. 

```{image} ../_static/spec2/spec2_8.png
:width: 100%
:align: center
```
<br/><br/>
