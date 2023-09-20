# Week 2

## (CSS)

Cascading Style Sheets, commonly known as CSS, is a stylesheet language used in web development to describe the visual presentation and formatting of web documents, including HTML and XML documents. CSS separates the structure and content of a web page (handled by HTML) from its style and layout, making it easier to maintain and apply consistent styling across multiple pages. Here are the key aspects of CSS:

Selectors: CSS selectors are used to target HTML elements that you want to style. Selectors can be based on element names, classes, IDs, attributes, and more. For example:

Element Selector: p selects all `<p>` elements.
Class Selector: .my-class selects all elements with class="my-class".
ID Selector: #my-id selects the element with id="my-id".
Properties and Values: CSS rules consist of one or more property-value pairs. Properties define what aspect of the element you want to style (e.g., color, font-size, margin), and values specify how you want to style it (e.g., blue, 16px, 10px 20px).

Rule Syntax: A CSS rule consists of a selector followed by a block of property-value pairs enclosed in curly braces. For example:

css
Copy code
h1 {
  color: blue;
  font-size: 24px;
}
External, Internal, and Inline CSS:

External CSS: You can link an external CSS file to your HTML document using the `<link>` element in the `<head>` section. This allows you to separate your CSS from your HTML, making it easier to maintain and reuse styles across multiple pages.
Internal CSS: You can include CSS directly within the HTML document using the `<style>` element in the `<head>` section. This is useful for small-scale styling or when you want to apply unique styles to a single page.
Inline CSS: You can apply styles directly to individual HTML elements using the style attribute. Inline styles are typically used for quick overrides or specific one-off styles.
Selectors and Specificity: CSS follows a set of rules to determine which styles should be applied when multiple rules target the same element. Specificity is a way to measure how specific a selector is, and it determines which styles take precedence.

Cascading: The "C" in CSS stands for "Cascading," which means that styles can cascade down from parent elements to child elements. Styles applied to a parent element can affect its children unless overridden by more specific child selectors.

Box Model: In CSS, every HTML element is considered a rectangular box with properties like width, height, padding, border, and margin. Understanding the box model is crucial for controlling the layout and spacing of elements.

Flexbox and CSS Grid: CSS provides layout models like Flexbox and CSS Grid, which offer powerful tools for creating responsive and complex layouts. Flexbox is best for one-dimensional layouts (e.g., rows or columns), while CSS Grid is ideal for two-dimensional grid-based layouts.

Media Queries: CSS allows you to use media queries to apply different styles based on the characteristics of the user's device, such as screen width, height, and orientation. This is essential for creating responsive web designs that adapt to different screen sizes.

Transitions and Animations: CSS can be used to create smooth transitions and animations for elements. This adds interactivity and enhances the user experience.

CSS is a fundamental technology in web development, and proficiency in CSS is essential for creating visually appealing and responsive web pages. By combining HTML for structure, CSS for presentation, and JavaScript for interactivity, web developers can build dynamic and engaging web applications.

## CSS Selectors

Element Selector:

The most basic selector, it targets all elements of a specific type.
Example: p selects all `<p>` elements on the page.
Class Selector:

Targets elements with a specific class attribute.
Example: .my-class selects all elements with class="my-class".
ID Selector:

Targets a single element with a specific ID attribute.
Example: #my-id selects the element with id="my-id".
Descendant Selector:

Selects an element that is a descendant of another element.
Example: ul li selects all `<li>` elements that are descendants of a `<ul>` element.

### Child Selector

Selects an element that is a direct child of another element.
Example: ul > li selects all `<li>` elements that are immediate children of a `<ul>` element.
Adjacent Sibling Selector:

Selects an element that is an adjacent sibling of another element.
Example: h2 + p selects the `<p>` element that directly follows an `<h2>` element.
Attribute Selector:

Selects elements with a specific attribute or attribute value.
Example: `[type="text"]` selects all elements with type="text".
Pseudo-Classes:

Pseudo-classes allow you to select elements based on their state or position.
Example: a:hover selects all `<a>` elements when the mouse hovers over them.
Pseudo-Elements:

Pseudo-elements select parts of an element rather than the whole element.
Example: p::first-line selects the first line of text within all `<p>` elements.
Grouping Selectors:

You can group multiple selectors together and apply the same styles to all selected elements.
Example: `h1`, `h2`, `h3` selects all `<h1>`, `<h2>`, and `<h3>` elements and applies the same styles to them.
Universal Selector:

Selects all elements on the page.
Example: * selects all elements.
Negation Selector:

Excludes elements that match a specific selector.
Example: p:not(.special) selects all `<p>` elements that do not have the class special.

### Declaration Block

The declaration block is enclosed in curly braces {} and contains one or more property-value pairs.
Each property defines an aspect of the styling (e.g., color, font-size, margin), and each value specifies how that aspect should be styled (e.g., blue, 16px, 10px 20px).
Properties and values are separated by a colon, and each declaration is terminated with a semicolon.
Example declaration block

```css
    selector{
        property-name : value ;
        property-name : value ;
        property-name : value ;
    }
```

```css
    p {
        color : red
    }
```

### Comments

You can add comments to your CSS code using `/* to start the comment and */` to end it.
Comments are ignored by browsers and are used to provide explanations or notes within your CSS code.
Example comment

```css
    /*This is CSS Comment*/
```

```css
    /*Styling all h1 in the HTML*/
    h1
    {
        text-align : center ; /*Describes that each h1 tag in html will be centerized*/
    }
```

## CSS Properties

### CSS Backgrounds

CSS provides several background properties that allow you to control the background of HTML elements. These properties help you set background colors, images, repeat patterns, position backgrounds, and more. Here are some commonly used CSS background properties:

#### background-color

Specifies the background color for an element.

```css

    body
    {
        background-color: red; /*sets the background color to red.*/
    }

```

#### background-image

Specifies an image to be used as the background.

```css
    div{
        background-image: url('background.jpg');
         /*sets the background to the image file "background.jpg."*/
    }
```

#### background-repeat

Controls how a background image is repeated.
Values:

- repeat (default): Repeats both horizontally and vertically.
- repeat-x: Repeats only horizontally.
- repeat-y: Repeats only vertically.
- no-repeat: Does not repeat.

#### background-size

Sets the size of the background image.
Values:

- auto (default): The browser calculates the size based on the image's intrinsic dimensions.
- cover: Scales the image to cover the entire element, maintaining aspect ratio.
- contain: Scales the image to fit within the element, maintaining aspect ratio.

#### background-position

Defines the starting position of the background image within the element's background area.
You can use keywords like left, center, or right, and percentages or pixel values.

```css
div{
    background-position: center center; 
    /* centers the background image both horizontally and vertically. */
}

```

#### background-attachment

Specifies whether the background image is fixed or scrolls with the content.
Values:

- scroll (default): The background scrolls with the content.
- fixed: The background stays fixed relative to the viewport.

### CSS Color Property

The CSS color property is used to specify the text color for an HTML element's content. It allows you to control the color of text within elements such as paragraphs, headings, links, and more. The color property accepts various color values, including color names, hexadecimal values, RGB values, and HSL values. Here are some examples of how to use the color property:

```css
    h1 {
        color : red; /*Changes the color of the headings to red*/
    }
```

```css
    p
    {
        color : green; /*changes the color of any paragraph to green*/
    }
```

### CSS Width and Height

In CSS, the width and height properties are used to control the dimensions of HTML elements, such as boxes, images, and other content. These properties allow you to specify how wide and tall an element should be, providing control over the layout and presentation of web content. Here's how to use the width and height properties:

#### width Property

The width property specifies the width of an element. It can accept various types of values, including:

Fixed Values: You can specify a fixed width in:

- pixels (px)
- centimeters (cm)
- millimeters (mm)
- inches (in)
- other units.

```css
    div
    {
        width: 300px; /* Fixed width of 300 pixels */
    }
```

```css
 .child-element
 {
    width: 50%; /* Width is 50% of the parent's width */
 }
```

```css
    .content
    {
        width: auto; /* Width adjusts based on content */
    }
```

#### Height Property

The height property specifies the height of an element. Like the width property, it accepts various types of values, including:

Fixed Values: You can specify a fixed height in pixels, centimeters, millimeters, inches, or other units.

```css
    div
    {
        height: 200px; /* Fixed height of 200 pixels */
    }
```

```css
    .child-element
    {
        height: 75%; /* Height is 75% of the parent's height */
    }
```

```css
    .content
    {
        height: auto; /* Height adjusts based on content */
    }
```

```css
    .item
    {
        max-height: 400px; /* Maximum height of 400 pixels */
        min-height: 100px; /* Minimum height of 100 pixels */
    }
```

Viewport Units: CSS provides viewport-relative units like vh (viewport height) and vw (viewport width) that allow you to set heights and widths relative to the size of the browser window.

```css
    .box
    {
        height: 50vh; /* Height is 50% of the viewport height */
        width: 30vw; /* Width is 30% of the viewport width */
    }
```

Using the width and height properties, along with other CSS properties like margin, padding, and box-sizing, you can precisely control the layout and size of elements on your web page. These properties are crucial for creating responsive and visually appealing web designs.

## CSS Text

CSS provides a wide range of text properties that allow you to control the appearance and styling of text within HTML elements. These properties enable you to specify the font, size, color, alignment, decoration, spacing, and other aspects of text presentation. Here are some commonly used CSS text properties

1. text-align
   - Sets the horizontal alignment of text within an element.
   - Values: `left`, `center`, `right`, or `justify`.

```css
    h1{
        text-align : center /*text position's in the center of it's parent */
    }
    span
    {
        text-align : left /*text position's in the left of it's parent */
    }
    p
    {
        text-align : right /*text position's in the right of it's parent */
    }
   ```

2 text-decoration
   - Controls the decoration of text (e.g., underline).
   - Values: `none`, `underline`, `overline`, `line-through`, or `inherit`.

   ```css
    a
    {
        text-decoration : none /*the most common used in links tags*/
    }
   ```

3. text-transform
   - Specifies how text is transformed, such as converting it to uppercase or lowercase.
   - Values: `uppercase`, `lowercase`, `capitalize`, or `none`.

   ```css
    h1
    {
        text-transform : uppercase; /*EACH LETTER IN THE TEXT IS UPPERCASED*/
    }
    p
    {
        text-transform : capitalize /*Each Letter In Each Word Is Capitalized*/
    }
    span
    {
        text-transform : lowercase /*each letter in each word is lowercased*/
    }
   ```

4. line-height
   - Sets the height of a line of text. It can affect line spacing and readability.

   ```css
    .description
    {
        line-height : 50px /*50px space between each line in the text*/
    }
   ```

5. letter-spacing
    - Controls the space between characters (letters) in text.

    ```css
        p
        {
            letter-spacing : 5px /*5px space between each letter in the same word*/
        }
    ```

6. word-spacing
    - Defines the space between words in text.
    
    ```css
        p
        {
            word-spacing: 5px; /*5px space between each word in the text*/
        }
    ```

7. text-shadow
    - Adds a shadow effect to text.
    
    ```css
        .header
        {
            text-shadow : 1px 1px 1px 1px black 
            /*shadow from (top & bottom) = 1px shadow from (right & left) = 1px */
            /*blur with 1px , shadow distrubution with 1px*/
            /*and finaly the color of the shadow is black*/
        }
    ```

    We can also use negative values as directions in shadow.

    ```css
        .header
        {
            text-shadow : -1px -1px 1px 1px black 
            /*shadow from (bottom & top) = 1px shadow from (left & Right) = 1px */
            /*blur with 1px , shadow distrubution with 1px*/
            /*and finaly the color of the shadow is black*/
        }
    ```
8. text-indent
    - text-indent specifies the space that will the content leave before starting the text

    ```css
        p
        {
            text-indent : 100px
            /*the text will start after 100px space from the beginnig*/
        }
    ```

9. direction:
    - Defines the direction of text, useful for languages that are written from right to left (e.g., Arabic or Hebrew).
    - Values: `ltr` (left to right) or `rtl` (right to left).
    
    ```css
        body
        {
            direction : rtl
            /*means that all items will start from right to left*/
        }
    ```

