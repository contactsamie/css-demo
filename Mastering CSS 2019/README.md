# Mastering CSS 2019

## Studying Note:
 1. [First CSS Stylesheets](#first-css-stylesheets)
 2. [Styling Text](#styling-text)
 3. [Selector](#selector)
 4. [Styling Forms and Buttons](#styling-forms-and-buttons)
 5. [Box Model](#box-model)
 6. [Positioning](#positioning)
 7. [Transitions and Animations](#transitions-and-animations)
 8. [Next](#next)

# First CSS Stylesheets

### Inline Styles
	
	You may use inline styles with just about any HTML element.

	Because of the inconvenience of inline styles and difficulty of maintenance of the document, in general, inline styles are often not optimal for production.

	The one exception for usage of inline styles is in the production of HTML5 emails. When producing HTML5 emails, you almost always have to use inline styles.

### Styles in the document head

### Attaching an external stylesheet with link
	
Note that the style tags are not used in an external document
	
# Styling Text

### Color
	
1. Named Colors
	
	Named colors actually have its drawbacks. For example, can you visualize the difference between Gold and GoldenRod?

2. RGB Colors

	RGB (Red-Blue-Green) are colors produced by mixing various intensities of the colors of red, blue and green. 
	This is similar to how many monitors work by mixing red, blue and green light in various intensities at each pixel.


3. Hexadecimal Colors

	 Instead of representing these values with the numbers 0-255, the hexadecimal number system is used with a range from 0-FF.

### Text Alignment
	
left, center, right, and justify
	
### Text Transform

capitalize, uppercase, and lowercase

### Text Decoration

underline and overline

### Spacing Text

1. text-indent

2. letter-spacing

3. line-height

4. word-spacing (don't adjust it)

### Text Shadow

1. The text-shadow rule allows you to place a drop shadow effect behind the text

2. The text-shadow rule has three components. The first is the horizontal offset of the shadow. The second component is the vertical offset of the shadow, and the third is the color of the shadow expressed as a named, RGB or hex color. 

### Working with Fonts

1. font-family

	CSS also allows choosing back-ups in case the first font choice is not available.
	
2. font-style

	italic or normal

3. font-weight

	bold or normal

4. font-size
	
# selector

### Tag Selectors

Tag selectors allow you to select element for styling by the tag name.
	
### ID Selector

ID’s are intended to be used once and only once on a page. 

Traditionally ID’s have been used to provide unique identifiers for content blocks within a web page.

Note the use of the hash sign preceding the attribute value

### Class Selector

Classes are intended to be deployed multiple times on a page.

Classes are a flexible way to select multiple content elements for formatting.

Note the use of the period to indicate a class in the selector in the style sheet.

### Multiple Selectors

	There are times when it’s strategic to select more than a single element at a single time.
	
### Decendant Selectors

As you’ve likely realized, HTML5 provides a hierarchical document skeleton. Elements that are inside other elements are said to be descendants.

Descendent selectors are one strategy for isolating a specific tag that may be used elsewhere in the document.

```
div > h2 {    
	color: brown; 
}
```
 
### Attribute Selectors

Attribute selectors, as you might imagine, allow you to select an element based on the attribute that it contains. 
	
```
[align] {    
	display: none; 
}
```
```
[align=center] {    
	display: none; 
}
```
	
### Pseudo-Selectors

```
p::first-line {    
	font-size: 1.25em; 
}
```

# Styling Forms and Buttons

### Form Surface

We’ve chosen to use placeholders instead of Labels to make the form as clean as possible.

```
form {    
	width: 80%;    
	border: 1px solid black;    
	padding: 10px;    
	background-color:  #fafafa; 
}
```

### Form elements

#### Text Inputs

```
input {    
	width: 100%;    
	height: 35px;    
	margin-bottom: 20px;    
	font-size: 1.75em;    
	background-color: #ececec;    
	border: none;    
	border-bottom: 2px dashed black; 
}
```

#### Styling the Select

```
select {    
	width: 100%;    
	font-size: 1.75em;    
	background-color: #ececec; 
}
```

#### Styling the CheckBox

The Checkbox is displayed by using the input tag, like other form elements. We have to differentiate it from the other input elements on the form, so we use the attribute selector.

```
input[type=checkbox] {    
	width: 20px;    
	height: 20px;    
	zoom: 2; 
}
```

#### Styling the labels

```
form p {    
	font-family: Arial;    
	font-size: 1.5em; 
}
```

#### Styling the Buttons

```
button {    
	width: 100%;    
	height: 35px;    
	font-size: 1.75em;    
	background-color: orange;    
	border-radius: 10px; 
}
```
# Box Model

Our box model begins with the inner portion of the box, the content. 

By default, the width of our box is defined as the width of the content inside it.

### Width

By setting the CSS width rule for the box, the element will be 50% of the width of the parent element, no matter how wide the window is.

```
box1 {    
	background-color: red;    
	color: white;    
	width: 50%; 
}
```

Here is an example of absolute width. At 200px the text is too long for the box but the text will flow to accommodate the text, and the height will adjust.

```
box1 {    
	background-color: red;    
	color: white;    
	width: 200px; 
}
```

### Height

The height CSS rule allows us to specify the height of the box, regardless of the amount of content inside the element. 

```
box1 {    
	background-color: red;    
	color: white;    
	width: 200px; 
	height: 400px;
}
```

### Padding

By adjusting the padding, we create some buffer space between around the text. This space takes on the same background color as the content.

```
box1 {    
	background-color: red;    
	color: white;    
	width: 200px; 
	height: 400px;
	padding: 10px;
}
```

We can also control the padding on each side separately.

```
box1 {    
	background-color: red;    
	color: white;    
	width: 200px; 
	height: 400px;
	padding-top: 20px;    
	padding-left: 40px; 
}
```
 
#### Time-Saving Tip

We can also adjust the padding on all four sides of div using the following shorthand:

The shorthand adjusts the padding in the box starting at the top and continuing in a clockwise direction.

```
box2 {    
	padding: 10px 20px 30px 40px; 
}
```
 
We can also set padding use a slight variation on the shorthand above:
If only two values are listed the first number is for top and bottom; the second number applies to the left and right.

```
box2 {    
	padding: 10px 20px; 
}
```

The padding adds to the overall width of the box. If you had 40px of padding on the left and right-hand side of the box, the total width of the 400px div would be 480px.

### Margin

The margin is the space between the element and the next element or the parent element. It will take on the background color of the parent element.

```
box1 {    
	background-color: red;    
	color: white;    
	width: 200px; 
	height: 400px;
	padding: 40px; 
	margin: 40px; 
}
```

### Border

According to the box model, between the padding and the margin, going all the way around the element, is the border. 
The border width and other properties can be selected in your CSS.

```
box1 {    
	background-color: red;    
	color: white;    
	width: 200px; 
	height: 400px;
	padding: 40px; 
	margin: 40px; 
	border: 20px solid black; 
}
```

border works a bit differently because it takes three arguments. 
The example above specifies:
	The width: 20px 
	The type: solid 
	The color: black

The border also contributes to the total width of the element.

```
Width 	Type
400 	Width of content
80 		40 for left and right padding
40 		20 for left and right border
80 		40 for left and right margin
---------------------------------------------
600 	Total width of the logical Division
```

# Positioning

### Static Positioning

It is default value for the CSS.
When you use static positioning, each element is lined up one on top of each other in the order in which they appear in the HTML.

### Relative Positioning

This will make its position relative to its normal position in the page element stack
Please note: 
	With Relative Positioning, the space that would have ordinarily occupied is still being held open. 
	Other elements will not move to fill in the space created.

Example:
```
.orange-box {    
	height: 200px;    
	width: 200px;    
	background: orange;
	
    position: relative;    
	top: 200px;    
	left: 200px; 
}
```

Then "top: 200px" will move the element down 200px from it’s static position. 

### Absolute Positioning

Absolute positioning allows you to select an exact position for the element within the browser window. 
Unlike relative positioning, the element will be taken out of the element flow, and other elements will fill the empty space created.

Example:
```
.orange-box {    
	height: 200px;    
	width: 200px;    
	background: orange;
	
    position: absolute;    
	bottom: 0px;    
	right: 0px; 
}
```

These rules will put the orange box in the lower right-hand corner of the browser window. 
If we add a large amount of content, the orange box will overlay the content, no matter how much content we add.

#### Absolute Positioning based on another element

Absolute positioning adjusts the positioning based the closest positioned ancestor. 

Example:
```
.purple-box {    
	height: 20px;    
	width: 20px;    
	background: purple;    
	position: absolute;    
	left: 10px;    
	top: 10px; 
}

<div class="orange-box">
	<div class="purple-box"></div> 
</div>    
```

### Fixed Positioning

Fixed positioning is very much like absolute positioning with one crucial difference: Elements assigned fixed positioning will not scroll with the rest of the content on the page. 
Like absolute positioning, the element will be removed from the flow, and the next element will take up its space.

Example:
```
.orange-box {            
	height: 200px;            
	width: 200px;            
	background: orange;    
    
	position: fixed;
	bottom: 0px;
	right: 0px;
}      
```

Then "bottom: 0px" - The element will be placed 0px away from the bottom edge. 

Now if we scroll, you’ll notice that unlike the absolute positioned element, the fixed doesn’t scroll with the content. 
Fixed positioning is often used when the design requires an item always be visible on the screen-Like a footer

# Transitions and Animations

## Transitions

To create a transition effect, you must specify two things:

	1. the CSS property you want to add an effect to
	2. the duration of the effect

Note: The transition effect will start when the specified CSS property changes value.

### Properties

transition-delay
	
	The transition-delay property specifies a delay (in seconds) for the transition effect.
	
transition-duration
	
	Specifies how many seconds or milliseconds a transition effect takes to complete

## Transformation

CSS transforms allow you to move, rotate, scale, and skew elements.

## Methods

translate 

	The translate() method moves an element from its current position (according to the parameters given for the X-axis and the Y-axis).
	
scale 

	The scale() method increases or decreases the size of an element (according to the parameters given for the width and height).
	
rotate 

	The rotate() method rotates an element clockwise or counter-clockwise according to a given degree.
	
skew 

	The skew() method skews an element along the X and Y-axis by the given angles.
	
# next
		
