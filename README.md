# CSS Utilities

This module contains a set of CSS classes that can be added to the classes property of controls in applications to quickly apply a number of frequently-used styles. 

## Version
1.0 initial release

## Table of Contents
- [CSS Utilities](#css-utilities)
  - [Version](#version)
  - [Table of Contents](#table-of-contents)
- [Setup](#setup)
  - [Application Setup](#application-setup)
  - [Applying the module](#applying-the-module)
  - [Customising Class Display](#customising-class-display)
  - [Upgrading the module](#upgrading-the-module)
  - [How to implement a utility class](#how-to-implement-a-utility-class)
- [Supported classes](#supported-classes)
  - [Typography](#typography)
    - [Titles \& headings](#titles--headings)
    - [Large \& small text](#large--small-text)
    - [Text styles](#text-styles)
    - [Text casing](#text-casing)
    - [Word spacing](#word-spacing)
    - [Letter spacing](#letter-spacing)
    - [Line height](#line-height)
    - [Breaking words](#breaking-words)
    - [Code block or preformatted text](#code-block-or-preformatted-text)
  - [Buttons](#buttons)
    - [Primary](#primary)
    - [Secondary](#secondary)
    - [Tertiary](#tertiary)

# Setup

## Application Setup
1. Check the Enable Style Sheet checkbox in the application properties

## Applying the module

**Stadium 6.6 or higher**
1. Create a folder called "CSS" inside of your Embedded Files in your application
2. Drag the two CSS files from this repo [*utils-variables.css*](utils-variables.css) and [*utils.css*](utils.css) into that folder
3. Paste the link tags below into the *head* property of your application
```html
<link rel="stylesheet" href="{EmbeddedFiles}/CSS/utils.css">
<link rel="stylesheet" href="{EmbeddedFiles}/CSS/utils-variables.css">
``` 

**Versions lower than 6.6**
1. Copy the CSS from the two css files into the Stylesheet in your application

## Customising Class Display
1. Open the CSS file called [*utils-variables.css*](utils-variables.css) from this repo
2. Adjust the variables in the *:root* element as you see fit
3. Overwrite the file in the CSS folder of your application with the customised file

## Upgrading the module
To upgrade the CSS in this module, follow the [steps outlined in this repo](https://github.com/stadium-software/samples-upgrading)

[Back to top](#table-of-contents)

## How to implement a utility class
1. First, make sure you have [applied the module](#applying-the-module)
2. Find a class you want to add in the list below
3. Add the class to the classes property of a control in lower case

![Implementing a class on a Control](images/Utils-Implement.png)

# Supported classes

## Typography

### Titles & headings
Titles and heading classes affect various aspects of text display

Customise any of these by changing the related [*variables*](utils-variables.css)

**Class name**
```css
h1
```
**h1 variables**
```css
--utils-h1-font-size: 32px;
--utils-h1-font-weight: 600;
--utils-h1-line-height: 1.5;
--utils-h1-margin-top: 1em;
--utils-h1-margin-bottom: .5em;
```

**Class name**
```css
h2
```
**h2 variables**
```css
--utils-h2-font-size: 24px;
--utils-h2-font-weight: 600;
--utils-h2-line-height: 1.5;
--utils-h2-margin-top: 1em;
--utils-h2-margin-bottom: .5em;
```

**Class name**
```css
h3
```
**h3 variables**
```css
--utils-h3-font-size: 18px;
--utils-h3-font-weight: 600;
--utils-h3-line-height: 1.5;
--utils-h3-margin-top: 1em;
--utils-h3-margin-bottom: .5em;
```

**Class name**
```css
page-title
```
**page-title variables**
```css
--utils-page-title-font-size: 22px;
--utils-page-title-font-weight: 600;
--utils-page-title-line-height: 1.5;
--utils-page-title-margin-top: 1em;
--utils-page-title-margin-bottom: .5em;
```

**Class name**
```css
subtitle
```
**subtitle variables**
```css
--utils-subtitle-font-size: 18px;
--utils-subtitle-font-weight: 600;
--utils-subtitle-line-height: 1.5;
--utils-subtitle-margin-top: 1em;
--utils-subtitle-margin-bottom: .5em;
```

[Back to top](#table-of-contents)

### Large & small text
Large & small text classes affect the size of displayed text 
```css
large-text
```
```css
small-text
```

[Back to top](#table-of-contents)

### Text styles
Text style classes affect the style of displayed text 
```css
italic
```
```css
bold
```
```css
underline
```

[Back to top](#table-of-contents)

### Text casing
Text casing classes allow for changing the case of displayed text 
```css
lower-case
```
```css
upper-case
```
```css
captitalize
```

### Word spacing
Word spacing classes allow for increasing or decreasing the spaces between words

1. Append a pixel value to the base class name between -3 and 10
2. Increments by 1 (-1, 0, 1, etc.)

Example for 'word-spacing: 3px;'
```css
word-spacing-3
```
Example for 'word-spacing: -1px;'
```css
word-spacing--1
```

### Letter spacing
Letter spacing classes allow for increasing or decreasing the spaces between letters
1. Append a pixel value to the base class name between -3 and 3
2. Increment by 1 (-1, 0, 1, etc.)

Example for 'letter-spacing: 4px;'
```css
letter-spacing-4
```
Example for 'letter-spacing: -1px;'
```css
letter-spacing--1
```

### Line height
Line height classes allow for increasing or decreasing the line-height attribute of displayed text
1. Calculated as percentage of font-size
2. Append a value to the base class name between 50 and 250 (the equivalent of line-height:0.5 to 2.5;)
3. Increments by 10 (50, 60, 70, etc.)

Example for 'line-height: 140%;' (the equivalent of 'line-height:1.4;')
```css
line-height-140
```

### Breaking words
This class prevents word overflow by hyphenating long words

Only works with width-restricted elements
```css
break-word
```

### Code block or preformatted text
Provides for the display of code or other preformatted text. In preformatted text line breaks are preserved. 

```css
code-block
```
**Code-block variables**
```css
--utils-code-background-color: #ddd;
--utils-code-font-color: #333;
--utils-code-font-size: 14px;
--utils-code-max-width: 100%;
--utils-code-min-width: 100px;
--utils-code-padding: .3em;
```

## Buttons
Provides for three button styles. The display of each type can be customised in the [*utils-variables.css*](utils-variables.css) file

### Primary
Primary buttons 
```css
primary
```

**Primary button variables**
```css
--utils-primary-button-background-color: #3399ff;
--utils-primary-button-border-color: #2196f3;
--utils-primary-button-border-width: 1px;
--utils-primary-button-border-radius: 3px;
--utils-primary-button-font-color: white;
--utils-primary-button-font-size: 14px;
--utils-primary-button-text-transform: uppercase;
--utils-primary-button-text-decoration: none;
--utils-primary-button-padding: 10px 16px;
--utils-primary-button-box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
--utils-primary-button-outline-color: white;
--utils-primary-button-outline-width: 1px;

--utils-primary-hover-button-background-color: #1976d2;
--utils-primary-hover-button-border-color: #2196f3;
--utils-primary-hover-button-border-width: 1px;
--utils-primary-hover-button-border-radius: 3px;
--utils-primary-hover-button-font-color: #fff;
--utils-primary-hover-button-font-size: 14px;
--utils-primary-hover-button-text-transform: uppercase;
--utils-primary-hover-button-text-decoration: none;
--utils-primary-hover-button-padding: 10px 16px;
--utils-primary-hover-button-box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
```

### Secondary
Secondary buttons 
```css
secondary
```
**Secondary button variables**
```css
--utils-secondary-button-background-color: rgb(255, 255, 255);
--utils-secondary-button-border-color: #2196f3;
--utils-secondary-button-border-width: 1px;
--utils-secondary-button-border-radius: 3px;
--utils-secondary-button-font-color: #3399ff;
--utils-secondary-button-font-size: 14px;
--utils-secondary-button-text-transform: uppercase;
--utils-secondary-button-text-decoration: none;
--utils-secondary-button-padding: 10px 16px;
--utils-secondary-button-box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
--utils-secondary-button-outline-color: white;
--utils-secondary-button-outline-width: 1px;

--utils-secondary-hover-button-background-color: rgba(255,255,255,.8);
--utils-secondary-hover-button-border-color: #2196f3;
--utils-secondary-hover-button-border-width: 1px;
--utils-secondary-hover-button-border-radius: 3px;
--utils-secondary-hover-button-font-color: #3399ff;
--utils-secondary-hover-button-font-size: 14px;
--utils-secondary-hover-button-text-transform: uppercase;
--utils-secondary-hover-button-text-decoration: none;
--utils-secondary-hover-button-padding: 10px 16px;
--utils-secondary-hover-button-box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
```

### Tertiary
Tertiary buttons 
```css
tertiary
```
**Tertiary button variables**
```css
--utils-tertiary-button-background-color: transparent;
--utils-tertiary-button-border-color: white;
--utils-tertiary-button-border-width: 1px;
--utils-tertiary-button-border-radius: 3px;
--utils-tertiary-button-font-color: #3399ff;
--utils-tertiary-button-font-size: 14px;
--utils-tertiary-button-text-transform: uppercase;
--utils-tertiary-button-text-decoration: none;
--utils-tertiary-button-padding: 10px 16px;
--utils-tertiary-button-box-shadow: none;
--utils-tertiary-button-outline-color: white;
--utils-tertiary-button-outline-width: 1px;

--utils-tertiary-hover-button-background-color: transparent;
--utils-tertiary-hover-button-border-color: white;
--utils-tertiary-hover-button-border-width: 1px;
--utils-tertiary-hover-button-border-radius: 3px;
--utils-tertiary-hover-button-font-color: #2196f3;
--utils-tertiary-hover-button-font-size: 14px;
--utils-tertiary-hover-button-text-transform: uppercase;
--utils-tertiary-hover-button-text-decoration: underline;
--utils-tertiary-hover-button-padding: 10px 16px;
--utils-tertiary-hover-button-box-shadow: none;
```
