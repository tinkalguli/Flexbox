# Flexbox

Flexbox gives us a efficient way of layout . We can place contents in different rows and columns and give some space around an between the contents.

To apply flexbox to a layout we have to assign **display: flex or display: inline-flex** to the container or the items. If we set the **display: flex or display: inline-flex** property to an element then the element convert into a **flex container** and the child elements will convert into **flex items** .

Before discuss about flexbox we should know about ***axis*** where the flex-items will lay down.

> Main-Axis : Main-Axis appears in the direction of the flex-items. If the flex-items lay down in a row(horizontally) then the **X-Axis**(horizontal-Axis) will be the **main-Axis** and if the flex-items lay down in a column then the **Y-axis**(vertical-Axis) will be the **main-Axis** of the flexbox.
>
> Cross-Axis : Cross-Axis appears in the perpendicular direction of the flex-items or the main-Axis . If the flex-items lay down in a row(horizontally) then the **Y-Axis**(vertical-Axis) will be the **cross-Axis** and if the flex-items lay down in a column then the **X-axis**(horizontal-Axis) will be the **cross-Axis** of the flexbox.

![image](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/axis.png)


## Properties of flexbox

We have some properties for flex-container and some properties for flex-items . Then we can categorize the properties based on Axis . Some properties work on main-Axis and some properties work on the cross-Axis . So now we know that we can apply **display: flex or display: inline-flex** property in the flex-container as well as flex-items . Basically we apply this property to the flex-container. All properties are listed bellow :


- Properties of Flex-container
  - For main-Axis
    - Display
    - Flex-direction
    - Flex-wrap
    - Flex-flow
    - Justify-content
  - For cross-Axis
    - Align-items
    - Align-content
- Properties of Flex-items
  - For main-Axis
    - Order
    - Flex-grow
    - Flex-shrink
    - Flex-basis
  - For cross-Axis
    - Align-self


### 1.Properties of Flex-container

First we will discuss about main-Axis's properties which is applied based on the main-Axis .

#### A. Display

This is the first step to get a flexbox. We have to assign display property to the element. Display property has two values i.e. **flex** and **inline-flex** .

##### (i) flex

It works normally , it takes the whole width of the display .

```
.container {
    display: flex;
  }
```

![display: flex](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/intro.png)


##### (ii) inline-flex

This value is similar to the **inline-block** display property , it takes the width according to the size of the content .

```
.container {
    display: inline-flex;
  }
```

![display: inline-flex](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/inline-flex.png)


#### B. Flex Direction

It determine the direction of the flex items in which items will lay down . Flex-direction property can take four properties i.e. **row**, **column**, **row-reverse**, **column-reverse** .

##### (i) Row(default)

This is the default value for flex-direction . If we apply this value then we don't get any changes . In this situation main-Axis is horizontal and cross-Axis  is vertical.

```
.container {
    flex-direction: row;
  }
```

![flex-direction: row;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/row.png)

##### (ii) Column

This value will set the items from top to bottom means vertically . In this situation the main-axis takes the place of cross-axis and the cross-axis takes the place of the main-axis .

```
.container {
    flex-direction: column;
  }
```

![flex-direction: column;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/column.png)

##### (iii) Row reverse
