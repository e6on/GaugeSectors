# GaugeSectors

HADashboard custom gauge widget with 3 sector-based color representation of the displayed value.

#### gaugesectors
![Screenshot](/gaugesectors.png)

A widget to report on numeric values for sensors in Home Assistant in a gauge format.

The gauge has 3 custom sectors with high and low value and style colors. These must be in hex RGB format, and the graph will interpolate the color of the level bar in between sectors.

For example:

It means color will stay ```#FF0000``` for all values below 749, ```#4CFF00``` from 750 up until 760. Take it over 761 and your gauge will glow ```#FFD800```.
```
    gauge:
       widget_type: gaugesectors
       title: Pressure
       units: ""
       min: 710
       max: 790
       sector1_color: "#FF0000"
       sector1_lo: 710
       sector1_hi: 749
       sector2_color: "#4CFF00"
       sector2_lo: 750
       sector2_hi: 760
       sector3_color: "#FFD800"
       sector3_lo: 761
       sector3_hi: 790
```
#### Mandatory Arguments:

- `entity`  - the entity_id of the sensor to be monitored
- `max`  - maximum value to show
- `min`  - minimum value to show
- `sector1_color` - first sector color
- `sector2_color` - second sector color
- `sector3_color` - third sector color
- `sector1_lo` - first sector low value
- `sector2_lo` - second sector low value
- `sector3_lo` - third sector low value
- `sector1_hi` - first sector high value
- `sector2_hi` - second sector high value
- `sector3_hi` - third sector high value

#### Optional Arguments:

- `title`  - the title displayed on the tile
- `title2`  - a second line of title text
- `units`  - the unit symbol to be displayed, if not specified HAs unit will be used, specify “” for no units

#### Style Arguments:

- `widget_style`
- `title_style`
- `title2_style`
- `bgcolor`
- `color`

Note that the color settings require an actual color, rather than a CSS style.

## How to Install

Copy contents of `custom_widgets` folder to your HADashboard `custom_widgets` folder.
