---
title: "Layouts"
weight: 10
# bookFlatSection: false
bookToc: false
# bookHidden: false
# bookCollapseSection: false
# bookComments: true
---
## Layouts
A layout is a container that positions UI elements according to 
certain rules.  There are four main layouts in NativeScript:

1. StackLayout
2. GridLayout
3. FlexboxLayout
4. AbsoluteLayout

### StackLayout
StackLayout positions elements one after the other, either as 
separate lines (the default) or across a row
 (orientation="horizontal"). 
 
{{< figure src="../../images/StackLayout.jpg" >}} 

### Example Code
```xml
<StackLayout>
    <Label text="first item"></Label>
    <Label text="second item"></Label>
    <Label text="third item"></Label>
</StackLayout>
```

You can fine-tune the placement of elements with these two attributes:

* horizontalAlignment="left | center | right | stretch"
* veticalAlignment="top | center | bottom | stretch" 

These alignment attributes would go on the child elements of a StackLayout container.

### GridLayout
GridLayout arranges elements in a table format of rows and columns. There are two attributes that 
define the row and column structure of the layout:

* columns="N1, N2, N3"  -  Three columns with widths
N1..3.
* rows="N1, N2, N3"     - Three rows with height N1..3.

Instead of a number, a column can be *auto* for as much as the element needs or 
*asterisk* for take all available space (a stretch). 

Once you have specified the rows and columns, you can 
place child elements in cells using the properties *row=N*
and *col=M*.  These are indexed from zero.  There are two 
additional child properties, *rowSpan* and *colSpan*.  These are used when 
you want an element to extend over multiple cells.  

{{< figure src="../../images/GridLayout.jpg" >}} 

### Example Code
```xml
<GridLayout columns="*, *, *" rows="*, *, *">
    <Label text="one" row="0" col="0"></Label>
    <Label text="two" row="1" col="1"></Label>
    <Label text="three" row="2" col="2"></Label>
</GridLayout>
```
### FlexboxLayout
The FlexboxLayout does what css flex does, namely allow
you to position a number of elements along a row (default) or
vertically (flexDirection="column").  The benefit of using
FlexboxLayout is in how you can justify elements to the left. right,
or center, control their relative sizes, align, and so on.

{{< figure src="../../images/FlexboxLayout.jpg" >}}

### Example Code
```xml
<FlexboxLayout alignItems="center" justifyContent="flex-end">
    <Label text="Label 1" width="10" height="30" backgroundColor="lightblue"></Label>
    <Label text="Label 2" width="10" height="30" backgroundColor="lightyellow"></Label>
    <Label text="Label 3" width="10" height="30" backgroundColor="pink"></Label>
</FlexboxLayout>
``` 

### AbsoluteLayout
AbsoluteLayout uses coordinates off the top left of the container to 
position elements. The parameters you use to set the position are *left* and *top*.

{{< figure src="../../images/AbsoluteLayout.jpg" >}}

### Example Code
```xml
<AbsoluteLayout width="210" height="210" backgroundColor="lightgray">
    <Label text="10, 10" left="10" top="10" width="90" height="90" backgroundColor="red"></Label>
    <Label text="110, 10" left="110" top="10" width="90" height="90" backgroundColor="green"></Label>
    <Label text="110, 110" left="110" top="110" width="90" height="90" backgroundColor="blue"></Label>
    <Label text="10, 110" left="10" top="110" width="90" height="90" backgroundColor="yellow"></Label>
</AbsoluteLayout>
```

 

