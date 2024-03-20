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
- [Supported classes](#supported-classes)
  - [How to implement a utility class](#how-to-implement-a-utility-class)
  - [Typography](#typography)
    - [Titles \& headings](#titles--headings)
    - [Large \& small text](#large--small-text)
    - [Text styles](#text-styles)
    - [Text casing](#text-casing)
    - [Word spacing](#word-spacing)
    - [Letter spacing](#letter-spacing)
    - [Line height](#line-height)
    - [Breaking words](#breaking-words)
  - [Buttons](#buttons)
    - [Primary](#primary)
    - [Secondary](#secondary)
    - [Tertiary](#tertiary)
  - [Code-Block](#code-block)
    - [code-block](#code-block-1)

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

# Supported classes

## How to implement a utility class
1. First, make sure you have [applied the module](#applying-the-module)
2. Find a class you want to add in the list below
3. Add the class to the classes property of a control in lower case

![Implementing a class on a Control](images/Utils-Implement.png)

## Typography

### Titles & headings
Titles and heading classes affect text display

Customise any of these by changing the related [*variables*](utils-variables.css)
```css
h1
```
```css
h2
```
```css
h3
```
```css
page-title
```
```css
subtitle
```

**Available variables**
```css
/*TITLES & HEADINGS*/
--utils-h1-font-size: 32px;
--utils-h1-font-weight: 600;
--utils-h1-line-height: 1.5;
--utils-h1-margin-top: 1em;
--utils-h1-margin-bottom: .5em;

--utils-h2-font-size: 24px;
--utils-h2-font-weight: 600;
--utils-h2-line-height: 1.5;
--utils-h2-margin-top: 1em;
--utils-h2-margin-bottom: .5em;

--utils-h3-font-size: 18px;
--utils-h3-font-weight: 600;
--utils-h3-line-height: 1.5;
--utils-h3-margin-top: 1em;
--utils-h3-margin-bottom: .5em;

--utils-page-title-font-size: 22px;
--utils-page-title-font-weight: 600;
--utils-page-title-line-height: 1.5;
--utils-page-title-margin-top: 1em;
--utils-page-title-margin-bottom: .5em;

--utils-subtitle-font-size: 18px;
--utils-subtitle-font-weight: 600;
--utils-subtitle-line-height: 1.5;
--utils-subtitle-margin-top: 1em;
--utils-subtitle-margin-bottom: .5em;
```

[Back to top](#table-of-contents)

### Large & small text
Large & small text classes affect text display
```css
large-text
```
```css
small-text
```

[Back to top](#table-of-contents)

### Text styles
Text style classes affect text display
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
1. Affect text display
2. Apply class as shown
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
1. Affects the word-spacing property
2. Append a pixel value between -3 and 10
3. Increment by 1 (-1, 0, 1, etc.)

Example for 'word-spacing: 3px;'
```css
word-spacing-3
```
Example for 'word-spacing: -1px;'
```css
word-spacing--1
```

### Letter spacing
1. Affects the letter-spacing property
2. Append a pixel value between -3 and 3
3. Increment by 1 (-1, 0, 1, etc.)

Example for 'letter-spacing: 4px;'
```css
letter-spacing-4
```
Example for 'letter-spacing: -1px;'
```css
letter-spacing--1
```

### Line height
1. Affects the line-height property
2. Calculated as percentage of font-size
3. Append a value between 50 and 250 (the equivalent of line-height:0.5 to 2.5;)
4. Increment by 10 (50, 60, 70, etc.)

Example for 'line-height: 140%;' (the equivalent of 'line-height:1.4;')
```css
line-height-140
```

### Breaking words
1. Prevents word overflow
2. Apply as shown to width-restricted elements
```css
break-word
```

## Buttons

Provides for three button styles. The display of each type can be customised in the [*utils-variables.css*](utils-variables.css) file

### Primary
Primary buttons 
```css
primary
```

### Secondary
Secondary buttons 
```css
secondary
```

### Tertiary
Tertiary buttons 
```css
tertiary
```

## Code-Block

Provides for the display of code or other preformatted text. In preformatted text line breaks are preserved. 

### code-block

