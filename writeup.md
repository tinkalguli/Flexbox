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

>First we will discuss about main-Axis's properties which is applied based on the **main-Axis** .

- A. Display
- B. Flex-direction
- C. Flex-wrap
- D. Flex-flow
- E. Justify-content

#### A. Display

The **display** property is the first step to get a flexbox. We have to assign display property to the element. Display property has two values i.e. **flex** and **inline-flex** .

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

The **flex-direction** property determine the direction of the flex items in which items will lay down . Flex-direction property can take four properties i.e. **row**, **column**, **row-reverse**, **column-reverse** .

##### (i) row(default)

This is the default value for flex-direction . If we apply this value then we don't get any changes . In this situation main-Axis is horizontal and cross-Axis  is vertical.

```
.container {
    flex-direction: row;
  }
```

![flex-direction: row;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/row.png)

##### (ii) column

This value will set the items from top to bottom means vertically . In this situation the main-axis takes the place of cross-axis and the cross-axis takes the place of the main-axis .

```
.container {
    flex-direction: column;
  }
```

![flex-direction: column;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/column.png)

##### (iii) row-reverse

By applying this value we will get the same result as row(default) value but in the opposite direction i.e. from right to left .

```
.container {
    flex-direction: row-reverse;
  }
```

![flex-direction: row-reverse;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/row-reverse.png)

##### (iv) column-Reverse

This value is also opposite to the column value . The items will lay down in opposite direction i.e. from bottom to top .

```
.container {
    flex-direction: column-reverse;
  }
```

![flex-direction: column-reverse;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/column-reverse.png)

#### C. Flex Wrap

The **flex-wrap** property determines how the flex-container will adjust the flex-items inside it .

When we have extra items in a flex container then this property comes handy . Lets take an example :

```
<div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
    <div class="item">6</div>
    <div class="item">7</div>
    <div class="item">8</div>
    <div class="item">9</div>
  </div>

  * {
    margin: 0;
    padding: 0;
  }
  .container {
    display: flex;
    background: #FAFFFC;
    border: 5px solid #182945;
  }
  .item {
    background: #9EDDEB;
    padding: 40px 50px;
    font-size: 34px;
    margin: 10px;
  }
```

![flex-wrap](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/flex-nowrap.png)


In this example we can see that flex-items are overflowing . By default, the flex-container will always accommodate all the new items in a single line, even although the browser needs to be scrolled horizontally. We can fix this problem by **flex-wrap** property .

**Flex-wrap** property have three values i.e. **nowrap**, **wrap**, **wrap-reverse** .

##### (i) nowrap(default)

This is the default value which will not make any changes . The container will always accommodate all the items in a single line even although the browser needs to be scrolled horizontally.

```
.container {
    flex-wrap: nowrap;
  }
```

![flex-wrap: nowrap;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/flex-nowrap.png)

##### (ii) wrap

This value will automatically break the items into new lines , if the container does not has enough space to accommodate enough items in a single line .

```
.container {
    flex-wrap: wrap;
  }
```

![flex-wrap: wrap;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/flex-wrap.png)

##### (iii) wrap-reverse

The wrap-reverse is similar to wrap value, but this value wraps the items in the reverse direction .

```
.container {
    flex-wrap: wrap-reverse;
  }
```

![flex-wrap: wrap-reverse;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/wrap-reverse.png)

#### D. Flex flow

The **flex-flow** is the combination of **flex-direction** and **flex-warp** property means it is a shorthand property . The flex-flow property accepts two values at a time, where the first value is for the flex-direction and the last value is for flex-wrap.

```
.container {
    flex-flow: row wrap;
  }
```

#### E. Justify Content

The **justify-content** property controls the alignment of the items on the "main-axis" . It also helps to make use of extra space remaining in a flex container. This property takes six values i.e. **flex-start**, **flex-end**, **center**, **space-between**, **space-around**, **space-evenly** .

##### (i) flex-start(default)

This default value make flex-items start from the starting point on the "main-axis" and left the remaining space at the end . If items are laid down in a row than items starts from left to right and if the items are laid down in a column than items starts from top to bottom .

```
.container {
   justify-content: flex-start;
 }
```

![justify-content: flex-start;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/intro.png)

##### (ii) flex-end

All the flex-items are laid out towards the endpoint of the "main-axis" and left the extra space in the starting point(if remains) .

```
.container {
   justify-content: flex-end;
 }
```

![justify-content: flex-end;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/flex-end.png)

##### (iii) center

The 'center' value for 'justify-content' will center the flex-items along the "main-axis" line and evenly distribute the extra space between starting point and end point of the main-Axis(if remains) .

```
.container {
   justify-content: center;
 }
```

![justify-content: center;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/flex-end.png)

##### (iv) space-between

The extra space in the flex container will be evenly distributed between the flex-items, where the first item in the container will stick to the starting point of the "main-axis" and the last item will stick to the endpoint of the main-axis.

```
.container {
   justify-content: space-between;
 }
```

![justify-content: space-between;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/space-between.png)

##### (v) space-around

The extra space in the flex container will be evenly distributed around the flex-items on the "main-axis". Means on the left as well as on the right side of the flex-items there will equal amount of space.


```
.container {
   justify-content: space-around;
 }
```

![justify-content: space-around;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/space-around.png)

##### (vi) space-evenly

The extra space in the flex container will be distributed in such a way that, the space between any two items as well the space of the item from the edge of the container will be equal.

```
.container {
   justify-content: space-evenly;
 }
```

![justify-content: space-evenly;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/space-evenly.png)

>Now we will look into the properties which are based on the **cross-Axis** .

- A. Align-items
- B. Align-content

#### A. Align Items

The **align-items** property is similar to **justify-content** property . The only difference is that the align-items property works on "cross-axis". It defines how the "flex-items" will be laid out on the "cross-axis" inside a "flex container". This property has five values i.e. **stretch**, **flex-start**, **flex-end**, **center**, **baseline** . Items should have some fix  height(items in a row) or width(items in a column) to get the effect of these property values .

##### (i) stretch(default)

This is the default value . Basically items stretch to fill up the container space . If the container has some fix height(items in a row) or fix width(items in a column) then we can stretch the items by using this value .

```
.container {
    display: flex;
    background: #FAFFFC;
    border: 5px solid #182945;
    height: 350px;
  }
```

or

```
.container {
    display: flex;
    background: #FAFFFC;
    border: 5px solid #182945;
    height: 350px;
    align-items: stretch;
  }
```

![align-items: stretch;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/stretch.png)

##### (ii) flex-start

The flex-items will be laid out from the starting point on the "cross-Axis" . Basically items starts from the starting point of the "cross-Axis" . Still we can use this value , if the  container has some fix  height(items in a row) or width(items in a column) .

```
.container {
    display: flex;
    background: #FAFFFC;
    border: 5px solid #182945;
    height: 350px;
  }
```

or

```
.container {
    display: flex;
    background: #FAFFFC;
    border: 5px solid #182945;
    height: 350px;
    align-items: flex-start;
  }
```

![align-items: flex-start;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/align-start.png)

##### (iii) flex-end

The flex-items will be laid out towards the endpoint on the "cross-axis" . Items should have some fix  height(items in a row) or width(items in a column) to get the effect of this value .

```
.container {
    display: flex;
    background: #FAFFFC;
    border: 5px solid #182945;
    height: 350px;
    align-items: flex-end;
  }
```

![align-items: flex-end;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/align-end.png)

##### (iv) center

The center value for align-items property will center the flex-items along the "cross-axis" line . It is necessary to have some fix  height(items in a row) or width(items in a column) to get the effect of this value .

```
.container {
    display: flex;
    background: #FAFFFC;
    border: 5px solid #182945;
    height: 350px;
    align-items: center;
  }
```

![align-items: center;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/align-center.png)

##### (v) baseline

The baseline value aligns the items based on the baseline of the text. this value depends on the content baseline . It is necessary to have some fix  height(items in a row) or width(items in a column) to get the effect of this value . Lets take an example :

```
<!-- HTML -->
  <div class="container">
    <div class="item item1">1</div>
    <div class="item item2">2</div>
    <div class="item item3">3</div>
    <div class="item item4">4</div>
  </div>

  <!-- CSS -->
  .container {
    display: flex;
    background: #FAFFFC;
    border: 5px solid #182945;
    height: 350px;
    align-items: baseline;
  }
  .item {
    background: #9EDDEB;
    padding: 40px 50px;
    margin: 10px;
  }
  .item1 {
    font-size: 34px;
  }
  .item2 {
    font-size: 20px;
  }
  .item3 {
    font-size: 48px;
  }
  .item4 {
    font-size: 72px;
  }
```

![align-items: baseline;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/baseline.png)

#### B. Align Content

The **align-content** property is similar to both justify-content and align-items property . The difference is that the justify-content and align-items property works on the individual items or line but the align-content property works on the multi-line flex container. The align-content property aligns flex container's lines when there is extra space on the cross-axis. If all the "flex-items" are on a single line in a container then this property does not affect. This property has six values i.e. **stretch**, **flex-start**, **flex-end**, **center**, **space-between**, **space-around** .

Lets make some multiple columns first :

```
<div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
    <div class="item">6</div>
    <div class="item">7</div>
    <div class="item">8</div>
    <div class="item">9</div>
  </div>

  .container {
    display: flex;
    flex-wrap: wrap;
    background: #FAFFFC;
    border: 5px solid #182945;
    height: 350px;
  }
  .item {
    background: #9EDDEB;
    padding: 40px 50px;
    margin: 10px;
  }
```

##### (i) stretch(default)

The **stretch** is the default value for the align-content property. All the items are stretched to take up the remaining space on the "cross-axis".

```
.container {
    display: flex;
    flex-wrap: wrap;
    align-content: stretch;
  }
```

![align-content: stretch;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/content-stretch.png)

##### (ii) flex-start

All the items in a multi-line flex container will be aligned from the starting point on the "cross-axis".

```
.container {
    display: flex;
    flex-wrap: wrap;
    align-content: flex-start;
  }
```

![align-content: flex-start;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/content-start.png)

##### (iii) flex-end

All the items in a multi-line flex-container will be aligned towards the endpoint on the "cross-axis".

```
.container {
    display: flex;
    flex-wrap: wrap;
    align-content: flex-end;
  }
```

![align-content: flex-end;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/content-end.png)

##### (iv) center

Items are laid out to the center of the multi-line flex-container on the "cross-axis".

```
.container {
    display: flex;
    flex-wrap: wrap;
    align-content: center;
  }
```

![align-content: center;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/content-center.png)

##### (v) space-between

The spaces are evenly distributed between the flex-items on the "cross-axis" as justify-content: space-between property works on the "main-axis".

```
.container {
    display: flex;
    flex-wrap: wrap;
    align-content: space-between;
  }
```

![align-content: space-between;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/content-between.png)

##### (vi) space-around

The spaces are evenly distributed around the flex-items on the "cross-axis" as justify-content: space-around property works on the "main-axis".

```
.container {
    display: flex;
    flex-wrap: wrap;
    align-content: space-around;
  }
```

![align-content: space-around;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/content-around.png)

### 1.Properties of Flex-items

>First we will discuss about main-Axis's properties which is applied based on the **main-Axis** .

- A. Order
- B. Flex-grow
- C. Flex-shrink
- D. Flex-basis

#### A. Order

We know that the elements are laid out according to the order in which it is written in the HTML document . The **order** property is used to reorder the flex-item within a flex-container without changing the source code in an HTML document . The property accepts unitless value in number, it can be negative or positive . te default value for this property is "0" . The items are reordered according to the values applied to the order property, from lowest to highest . If the order value for the items is the same then the items are laid out according to the order appeared in HTML source code . Lets take an example :

```
<div class="container">
    <div class="item item1">1</div>
    <div class="item item2">2</div>
    <div class="item item3">3</div>
    <div class="item item4">4</div>
  </div>

  .container {
    display: flex;
  }
  .item {
    background: #9EDDEB;
    padding: 40px 50px;
    margin: 10px;
  }
  .item1 {
    order: 1;
  }
```

![order: 1;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/order1.png)

In the above example we assign **order: 1** to the item1 . Item1 has laid down at the end because order of the item1 is bigger than the other items(default **order: 0**) . Lets take an example which will help you understand the negative order and regarding the order in the html  :

```
<div class="container">
    <div class="item item1">1</div>
    <div class="item item2">2</div>
    <div class="item item3">3</div>
    <div class="item item4">4</div>
  </div>

  .container {
    display: flex;
  }
  .item {
    background: #9EDDEB;
    padding: 40px 50px;
    margin: 10px;
  }
  .item1 {
    order: 2;
  }
  .item2 {
    order: 1;
  }
  .item3 {
    order: 1;
  }
  .item4 {
    order: -1;
  }
```

![order: -1;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/order2.png)

In the above example item4 has laid down in the first place and item1 has laid down at the end because item4 has lowest order value which is "-1" and Item1 has the largest order value which is "2" . Item2 and item3 has the same order which is "1" so two of them comes after the item1 and they have laid down according to html markup order .

#### B. Flex Grow

The **flex-grow** property allows the items to grow if there is extra space inside the flex container . The property accepts unitless value in number which provides the ability to grow to the items . By default, the value for the flex-grow property is "0", which means the size of the item will be auto . It may accept any value but not negative . Suppose we have two items inside a flex-container and we want the items to grow in the same proportionality. Then we can set the value 1 for flex-grow property for the items . If all the items have flex-grow set to 1 the extra space will be distributed equally to all the items .

```
<div class="container">
    <div class="item item1">1</div>
    <div class="item item2">2</div>
  </div>

  .container {
    display: flex;
  }
  .item {
    background: #9EDDEB;padding: 40px 50px;
    margin: 10px;
    flex-grow: 1;
  }
```

![flex-grow: 1;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/flex-grow1.png)

If one of the items has a value of 2, the remaining space would take up twice as much space as the others .

```
<div class="container">
    <div class="item item1">1</div>
    <div class="item item2">2</div>
  </div>

  .container {
    display: flex;
  }
  .item {
    background: #9EDDEB;
    padding: 40px 50px;
    margin: 10px;
  }
  .item1 {
    flex-grow: 2;
  }
  .item2 {
    flex-grow: 1;
  }
```

![flex-grow: 2;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/flex-grow2.png)

#### C. Flex Shrink

The **flex-shrink** property is opposite to the flex-grow property. It allows the items to shrink if there is no extra space in the container . If we reduce the size of screen we will find that width of the items is also reducing as the size of screens is reducing . By default, the value for flex-shrink property is "1" and accepts values which is greater than "1" . Negative values are invalid . For a better understanding of flex-shrink property, we have to applied **flex-basis** property. The **flex-basis** property is to set the initial size of the item before the item will grow or shrink in a flex-container according to the extra space . Lets take an example :

```
<div class="container">
    <div class="item item1">1</div>
    <div class="item item2">2</div>
  </div>

  .container {
    display: flex;
  }
  .item {
    background: #9EDDEB;
    padding: 40px 50px;
    margin: 10px;
    flex-basis: 300px;
    flex-shrink: 1;
  }
```

![flex-shrink: 1;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/flex-shrink1.png)

In this above example we have applied **flex-shrink: 1** . If we reduce the size of the screen items will also reduce .

![flex-shrink: 1;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/flex-shrink2.png)

If we assign **flex-shrink: 0** then the items will overflow in the flex-container . Lets see with an example :

```
<div class="container">
    <div class="item item1">1</div>
    <div class="item item2">2</div>
  </div>

  .container {
    display: flex;
  }
  .item {
    background: #9EDDEB;
    padding: 40px 50px;
    margin: 10px;
    flex-basis: 300px;
    flex-shrink: 0;
  }
```

![flex-shrink: 0;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/flex-shrink3.png)

#### D. Flex Basis

The **flex-basis** property is somewhat similar to the width property, as it accepts the values(in px, %, em, rem, etc.) similar to the width property . The flex-basis property is applied to set a base width(in case or row) or height(in case of column) or size of the flex-item from where the item will grow or shrink if necessary . By default, the value for flex-basis property is auto, which means the base size of the item will be computed based on the content inside it plus whatever the padding we will apply to the item .

```
<div class="container">
    <div class="item item1">1</div>
    <div class="item item2">2</div>
  </div>

  .container {
    display: flex;
  }
  .item {
    background: #9EDDEB;
    padding: 40px 50px;
    margin: 10px;
    flex-basis: 200px;
  }
```

![flex-basis: 200px;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/flex-basis.png)

> * Flex
This is the default value for the flex property where the first value is for flex-grow, second is for flex-shrink and the last value is for flex-basis . The last two value for flex property is optional . This is the default value for the flex property where the first value is for flex-grow, second is for flex-shrink and the last value is for flex-basis . The last two value for flex property is optional .

```
.item {
    flex: 0 1 auto;
  }
```

>If we ignore the last two values which is **flex-shrink** and **flex-basis** we can apply only **flex-grow** value to the **flex** property . Let's take an example with **flex-grow** value "1" .

```
.item {
    flex:  1;
  }
```

>Now we will discuss about cross-Axis's properties which is applied based on the **cross-Axis** .

- A. Align-self

#### A. Align-self

The **align-self** property is exactly similar to align-items property but only difference is **align-self** is applied to the flex items and **align-items** property is applied to the flex container . The **align-self** can take six values i.e. **auto**,  **stretch**,  **flex-start**,  **flex-end**,  **center**,  **baseline** . To get the result of this property there will be some space in the **cross-axis** because it always works on the **cross-axis** .

```
<div class="container">
    <div class="item item1">1</div>
    <div class="item item2">2</div>
    <div class="item item3">2</div>
  </div>

  .container {
    display: flex;
    height: 350px;
    align-items: flex-start;
  }
  .item {
    background: #9EDDEB;
    padding: 40px 50px;
    margin: 10px;
  }
```

##### (i) auto

The auto value for **align-self** property inherits, whatever the value is set for **align-items** in the flex-container. If it is **flex-star**, the **align-self** value will be also **flex-start** .

```
.item3 {
    align-self: auto;
  }
```

![align-self: auto;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/item-start.png)

##### (ii) stretch

The stretch property is to stretch out the size of individual items on the **cross-axis** to fill the extra space.

```
.item3 {
    align-self: stretch;
  }
```

![align-self: stretch;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/item-stretch.png)

##### (iii) flex-start

The item will be aligned from the starting point on the **cross-axis**.

```
.item3 {
    align-self: flex-start;
  }
```

![align-self: flex-start;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/item-start.png)

##### (iv) flex-end

The item will be aligned towards the endpoint on the **cross-axis** .

```
.item3 {
    align-self: flex-end;
  }
```

![align-self: flex-end;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/item-end.png)

##### (v) center

The item will be aligned at the center on the **cross-axis** .

```
.item3 {
    align-self: center;
  }
```

![align-self: center;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/item-center.png)

##### (vi) baseline

We have already seen baseline value for align-items property for the **flex-container** . The baseline value for **align-self** property also works based on the baseline of the content .

```
.item3 {
    align-self: baseline;
  }
```

![align-self: baseline;](https://raw.githubusercontent.com/suraj122/AC-STYLE-images/master/flexbox/item-baseline.png)


>It is better to use flexbox instead of float and inline-block technique .
