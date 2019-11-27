# Master CSS

## Studying Note:
 1. [First CSS Stylesheets](#first-css-stylesheets)
 2. [Styling Text](#styling-text)
 3. [Selector](#selector)
 4. [Next](#next)

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
	
# next
		
