---
sidebar_position: 21
---

# Attribute-based Styling

GOAT allows users to apply **attribute-based styling** techniques to enhance the data visualization on maps. This approach allows the visual representation to **reflect variations and patterns in the data**, making it easier to recognize and understand complex information spatially.

Under the <code>Layer design</code> <img src={require('/img/map/styling/styling_icon.webp').default} alt="Styling Icon" style={{ maxHeight: "25px", maxWidth: "25px", objectFit: "cover"}}/> menu, you will find the available styling settings for the layer selected.  <code>Fill Color</code>, <code>Stroke Color</code>, <code>Custom Marker</code>, and <code>Labels</code>. Each option has the <b>options button</b><img src={require('/img/map/styling/options_icon.png').default} alt="Options Icon" style={{ maxHeight: "25px", maxWidth: "25px", objectFit: "cover"}}/>. Under it, you will find the attribute-based styling, for that specific style setting (either Fill Color, Stroke Color, Custom marker, or Label). Style your map based on its dataset attributes. To edit the style attribute make sure the attribute toggle is ON, and then click the <b>options button</b><img src={require('/img/map/styling/options_icon.png').default} alt="Options Icon" style={{ maxHeight: "25px", maxWidth: "25px", objectFit: "cover"}}/>.


:::tip HINT
If you like to save your styling settings and use them in further projects, you can do so by [saving a style as default](../layer_style/styling/#default-settings). 
:::

## Select Attribute 

For the attribute-based styling, first, select the attribute that you like to visualize in the field <code>Color based on</code>. The data shall be ordered by a **data classification method** and associated with a <code>Color Palette</code>, and a <code>Color Scale</code>.

<div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center'}}>

  <img src={require('/img/map/styling/attribute_selection.gif').default} alt="Attribute Selection" style={{ maxHeight: "auto", maxWidth: "auto", objectFit: "cover"}}/>

</div> 

## Color Palette

 Under Palette, you will find GOAT's comprehensive set of palettes, all designed to provide **visually impactful spatial data representation**. 
 For further customization, you may set different <code>Palette Type</code>, <code>Palette Steps</code>,  
 A color palette is a collection of colors chosen to represent the values scale or categories, within your dataset. 
 Under the Palette, you may select from different pallettes types.
 
 GOAT provides a comprehensive set of predefined palettes, each of which has been designed to provide a **visually impactful representation of spatial data**. These palettes are categorized into four different groups for ease of selection and application.

The color palette provides several customization options. You can define your **number of steps** for a palette, you can **reverse** the colors and you can also define your **custom palette**.

<p></p>

| Palette Type| Example | Description |
| :-: | --- | ---|
| Diverging | <img src={require('/img/map/styling/diverging_palette.png').default} alt="diverging" style={{ maxHeight: "auto", maxWidth: "auto", objectFit: "cover"}}/> | This type of color palette is ideal for displaying data that is centred around a critical midpoint or has a natural division. It is particularly useful for displaying data characterised by both positive and negative variations from a central value, allowing these variations to be visualised clearly and effectively. |
| Sequential | <img src={require('/img/map/styling/sequential_palette.png').default} alt="sequential" style={{ maxHeight: "auto", maxWidth: "auto", objectFit: "cover"}}/> | This color palette is designed for data that follows a natural progression or ordered sequence. It excels at visualising continuous data, where values either incrementally increase or decrease along a spectrum. This makes it particularly suitable for clearly displaying data that gradually changes from one extreme to the other. |
| Qualitative | <img src={require('/img/map/styling/qualitative_palette.png').default} alt="qualitative" style={{ maxHeight: "auto", maxWidth: "auto", objectFit: "cover"}}/> | This color palette is designed for data that is categorised into specific, distinct groups or classes. Qualitative color palettes are designed to distinguish between discrete categories. Importantly, these palettes do so without suggesting any inherent order or relative importance between the different categories. |
| Singlehue | <img src={require('/img/map/styling/singlehue_palette.png').default} alt="singlehue" style={{ maxHeight: "auto", maxWidth: "auto", objectFit: "cover"}}/> | This color palette is a type of color scheme used in data visualisation that uses different hues, shades and tones of a single color. This approach creates a visually coherent and harmonious aesthetic that can be particularly effective in conveying information without the distraction of multiple colors. |


<div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center'}}>

  <img src={require('/img/map/styling/color_palettes.gif').default} alt="Color Palettes" style={{ maxHeight: "auto", maxWidth: "auto", objectFit: "cover"}}/>

</div> 

## Color Scale

Under the <code>Color Scale</code>, you will find the **data classification method** and the **color scale** that associates data values with a spectrum of colors. It converts a given data value within a given range (domain) into a corresponding color from a given color spectrum (range). GOAT provides six predefined **data classification methods**: [Quantile](#quantile), [Standard Deviation](#standard-deviation), [Equal Interval](#equal-interval), [Heads and Tails](#heads-and-tails), [Custom Breaks](#custom-breaks-for-numbers), and [Custom Ordinal](#custom-ordinal-for-strings).

## Data Classification Methods

### Quantile

The Quantile classification divides data into **groups with an equal number of values in each class** based on their attribute values. This method is useful for analyzing and visualizing patterns in data and can help identify trends and patterns that may not be obvious easily. The fact that the data values are grouped in equal quantities within each class makes this approach **ideal for data that is linearly distributed**. Per default, the data is distributed into 7 classes. 

<div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center'}}>

  <img src={require('/img/map/styling/quantile.png').default} alt="Quantile" style={{ maxHeight: "auto", maxWidth: "auto", objectFit: "cover"}}/>

</div>  


:::tip HINT
Want to deeper understand what quantile classification is? Check our [Glossary](../../further_reading/glossary/#quantile-classification).
:::

### Standard Deviation

The Standard Deviation method is a **statistical approach** used in data visualization. It uses the concept of standard deviation, a measure of the **amount of variation or dispersion in a set of values**, to determine how data points are assigned to different color categories. This method is valuable for its ability to provide a statistical perspective on the data, allowing users to quickly grasp the **relative dispersion and distribution of values** within the dataset. Per default, the data is distributed into 7 classes. 

<div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center'}}>

  <img src={require('/img/map/styling/standard_deviation.png').default} alt="Standard Deviation" style={{ maxHeight: "auto", maxWidth: "auto", objectFit: "cover"}}/>

</div> 

### Equal Interval

For the Equal Interval classification, the range of the attribute values is divided into **equal interval classes**. Per default, the data is distributed into 7 classes. 

<div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center'}}>

  <img src={require('/img/map/styling/equal_interval.png').default} alt="Equal Interval" style={{ maxHeight: "auto", maxWidth: "auto", objectFit: "cover"}}/>

</div> 

### Heads and Tails

The Heads and Tails method is used to deal with **datasets with a skewed distribution**. It's designed to highlight extremes in the data, focusing on the **'heads' (the very high values)** and the **'tails' (the very low values)**. This method is particularly useful for datasets where the most important information is found in the extremes, and where highlighting these values can lead to greater insight and understanding. Per default, the data is distributed into 7 classes. 

<div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center'}}>

  <img src={require('/img/map/styling/heads_tails.png').default} alt="Heads and Tails" style={{ maxHeight: "auto", maxWidth: "auto", objectFit: "cover"}}/>

</div> 


### Custom Breaks (for <code>numbers</code>)

The Custom Break classification is a data visualization method used for **numerical data**. It allows users to define **custom breakpoints** or **thresholds** and therewith provides a tailored approach for context-specific visualizations. 


### Custom Ordinal (for <code>strings</code>)

The Custom Ordinal classification is a data sorting and visualisation method applied to **string data**, such as categories, labels, or text-based variables. Unlike numerical data, where order is typically based on magnitude, string data often lacks a natural order. The Custom Order method therefore allows users to **define their own ordering rules for strings**, creating a customised sequence tailored to their specific needs. 

<div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center'}}>

  <img src={require('/img/map/styling/ordinal.png').default} alt="Custom Ordinal for strings" style={{ maxHeight: "auto", maxWidth: "auto", objectFit: "cover"}}/>

</div>


Therefore, additional steps can be added and multiple string values selected per group from a drop-down menu. The drop-down menu thereby lists all attribute values of the dataset. 

<div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center'}}>

  <img src={require('/img/map/styling/custom_ordinal.gif').default} alt="Custom Ordinal for strings" style={{ maxHeight: "300px", maxWidth: "300px", objectFit: "cover"}}/>

</div> 



import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

## Style Settings

<Tabs>
  <TabItem value="fill color" label="Fill Color" default> Fill Color can either be one single color or a color palette. GOAT offers a set of preset colors and palettes to style your map. 
    For attribute-based Fill Color select a Field from the selected <code>Layer</code>.
    GOAT applies a random color palette to your results. 
    <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center'}}>

   <img src={require('/img/map/layers/fill-color.gif').default} alt="Custom Ordinal for strings" style={{ maxHeight: "500px", maxWidth: "500px", objectFit: "cover"}}/>

   </div> 

  </TabItem>
  <TabItem value="stroke color" label="Stroke Color"> Stroke Color by default is one single color. Apply attribute-based styling to apply a color scale to the layer stroke. 
    For attribute-based Stroke Color select a Field from the selected <code>Layer</code>.
    GOAT applies a random color palette to your results. 

   <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center'}}>

   <img src={require('/img/map/layers/stroke-color.gif').default} alt="Custom Ordinal for strings" style={{ maxHeight: "500px", maxWidth: "500px", objectFit: "cover"}}/>

   </div> 



  </TabItem>
  <TabItem value="custom marker" label="Custom Marker"> When available, the custom marker has an icon library to best represent your data set.

<div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center'}}>

   <img src={require('/img/map/layers/attribute-based-custom-marker.gif').default} alt="Custom Ordinal for strings" style={{ maxHeight: "500px", maxWidth: "500px", objectFit: "cover"}}/>

   </div> 

  </TabItem>
</Tabs>