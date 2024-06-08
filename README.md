# Level 1: Basic CSS

## Basic Syntax

```
selector{
    property: value;
}
```

**Selector eg.**: h1, p, div, id, class etc.

## Styling Methods:

1. **Inline Styling**: Directly in HTML element using `style` attribute.

   ```
   <h1 style="color:red">Prakhar </h1>
   ```

2. **Internal Styling**: In HTML document using `<style>` tag.

```
     <style>
        h1 {
            color: red;
        }
        </style>
```

3. **External Stylesheet**: Writing CSS in a separate doc & linking it with the HTML file.

### **Note**:

Inline style is always on the priority as compared to the other two.

# Properties in CSS

## 1. Color Property:

      Used to set the color of foreground

      color:red;
      color:green;
      color:blue;
      etc.

## 2. Background Color Property:

      Used to set the color of background

      background-color:red;
      background-color:green;
      background-color:blue;
      etc.

### Color Systems:

1. **RGB (Red, Green, Blue)**:

   color:rgb(255,0,0) [red]
   </br>
   color:rgb(0,255,0) [green]
   </br>
   color:rgb(0,0,255) [blue]
   </br>
   color:rgb(255,255,255) [white]
   </br>
   color:rgb(0,0,0) [black]

2. **HEX (Hexadecimal) Code**:

   color:#ff0000 [red]
   </br>
   color:#00ff00 [green]
   </br>
   color:#0000ff [blue]

## 3. Selectors:

Used to target HTML elements to apply styles.

### Types of Selectors:

1. **Universal Selector**
   \*{}
2. **Element Selector**:
   h1{}, p{}, div{}, etc.
3. **Id Selector**:
   id is equivalent to a unique name given to some html element.
   It is not good practise to haven Multiple elements cannot having same id
   #id_name{}
4. **Class Selector**:
   class is equivalent to a group name given to some html elements.
   Multiple elements can have same class
   .class_name{}

**NOTE**: CSS sets style of the elements in the order they arrive in the stylesheet.
The style property coming at later stage will be prioritized as compared to the styles coming a earlier stage.

If you want to override the styles, you can use !important keyword after the style property value.

## 4. Text Properties:

**1. text-align**:
</br>
text-align:left/right/center/start/end;

**2. text-decoration**:
</br>
text-decoration:underline/overline/line-through/none;

**3. font-weight**:
</br>
how light or dark the font appears

font-weight: normal/bold/bolder/light/100-900
</br>

- font-weight<=400 -> lighter texture
- font-weight>400 -> darker texture

**4. font-family**:
Style of the font.
</br>
font-family: arial;
</br>
font-family: arial, roboto;
(if arial fails on a specific browser, apply roboto. This is known as fall back mechanism.)
</br>
There are two types of font families:
</br>

> Generic Font Family:

- Serif
- Sans-Serif
- Cursive
- Fantasy
- Monospace

> Specific Font Family:
> </br>

- specific fonts with different styles within the same font family
- Arial, Times New Roman, Tahoma
  </br>
  [Refer](https://www.tutorjoes.in/css_tutorial/css_properties_font_family)

**5. font-size**:
CSS allows to set font size in many units, but the most common one is pixels(px).
</br>
font-size: 25px;

**Units in CSS**:

1. Absolute

- **px** (Pixel):
  </br>
  96px = 1 inch = 2.54 cm
- **cm** (Centimeter)
- **mm** (Millimeter)
- **in** (Inch)
- **pt** (Point), etc.

2. Relative

- to be discussed later

6. line-height:
   defines the space between lines of text.
   </br>
   line-height: 2px;
   </br>
   line-height: normal;

7. text-transform:
   transforms the text to uppercase, lowercase, capitalize, etc.
   </br>
   text-transform: uppercase/lowercase/capitalize/none;

# Level 2: Box Model in CSS

- **Height**
- **Width**
- **Border**
- **Padding**
- **Margin**

  [Image of box model](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQyEgPUCKC2AhWrGtAXNa4SH9MRbVtdpZlkoQ&s)

## Height:

By default, it sets the content area _height_ of the element.
</br>
div{
height: 50px;
}

## Width:

By default, it sets the content area _width_ of the element.
</br>

```
div{
  width: 50px;
}
```

## Border:

Used to set an element's border

- border-width:2px;
- border-style:solid/dotted/dashed;
- border-color: black;

- Border Shorthand:
  </br>
  border: 2px solid black;
  (width style color)

- border-radius:
  Used to round the corners of an element's outer border edge.
  </br>
  border-radius: 10px;
  </br>
  border-radius: 50%;

**Note**: To create a circle of a div in CSS, we first make the div a square container by setting its height and width equal and then we set the border-radius to 50%.
</br>
_For eg_

```
div{
  height: 100px;
  width: 100px;
  border-radius: 50%;
}
```

## Padding:

Used to set the space between an element's content and its border.
</br>

- padding-left
- padding-right
- padding-top
- padding-bottom
- padding shorthand:
  </br>
  padding: 5px;
  padding: 10px 20px 30px 40px;
  (top right bottom left) -> clockwise

## Margin:

Used to set the space between an element's content and its border.
</br>

- margin-left
- margin-right
- margin-top
- margin-bottom
- margin shorthand:
  </br>
  margin: 5px;
  margin: 10px 20px 30px 40px;
  (top right bottom left) -> clockwise

### Display Property:

Used to control the layout of an element.

- In HTML, there are two types of elements:
  - block elements
  - inline elements
- **block** elements occupy the full 100% of width available.(eg. div)
- **inline** elements occupy only the space needed for their content. (eg. button)
- **inline-block**: similar to inline but we can set the margin and padding.
- **none**: to remove element from document flow.
- display property can be used to change the default display type of an element.
  </br>

  display: inline/block/inline-block/none

### Visibility

    visibility: hidden;

**Note**(_Impo._):

- visibility: hidden; -> hides the element but still occupies the space.
- display: none; -> removes the element from document flow and doesn't occupy space.

## Alpha Channel

sets the opacity of an element (0-1)

- RGBA
  color: rgba(255, 0, 0, 0.5);

  color: rgba(255, 0, 0, 1);

# Level 3

## Units in CSS

- Absolute (refer to level 1)
- Relative
  - %
  - em
  - rem

1. **Percentage(%)**:
   It is often used to define a **size as relative to an element's parent** object.

   width: 33%; <br>
   margin-left: 50%;

2. **em**:
   It is often used to define a **size as relative to the font-size of an element**
   - Font size of the parent, in the case of typological properties like font-size, and
   - Font size of the element itself, in the case of other properties like width, margin.
     Example:

```
#box1{
    height: 100px;
    width: 200px;
    background-color: green;
    font-size: 10px;
}

#box2{
    height: 50px;
    width: 30%;
    background-color: yellow;
    margin-left: 10%;
    font-size: 2em;
    /* double of parent's font-size */
    width: 5em;
    /* five times of element's font-size.
    width = 2*10px*5 */
}
```

3. **rem (Root EM)**:
   It is often used to define a **size as relative to the root element (HTML)**.
   Example:

```
html{
  font-size: 16px; /* default font-size */
  }

#box{
    font-size: 2rem; /* double of root's font-size */
    width: 5rem; /* five times of root's font-size */
    }
```

- rem is useful when you want to set a consistent font-size throughout the website, and you
  want to make sure that all elements scale accordingly when the root font-size changes.

4. **vw (Viewport Width) and vh (Viewport Height)** :
   It is often used to define a **size as relative to the viewport**.
   Viewport : size of the window in the browser.
   Example :

```
#box{
  width: 50vw; /* 50% of viewport width */
  height: 30vh; /* 30% of viewport height */
  }
```

- vw and vh are useful when you want to create a responsive design that adapts to the size of the viewport.

## Position Property:

The position property specifies the type of positioning method used for an element (static, relative, absolute, fixed).

- **static** : default postion (The top, right, bottom, left, and z-index properties have no effect)
- **relative** : The element is positioned relative to its normal position. (The top, right bottom, left, and z-index will work)
- **absolute** : The element is positioned relative to its first positioned(non-static position) ancestor element (removed from the flow.)
- **fixed** : The element is positioned relative to the viewport. (removed from flow)
  <br>
  **NOTE**: navbars and footers can be created using fixed postion.
  <br>
  <br>
  for navbar:
  ```
  postion: fixed;
  top: 0;
  ```
    <br>
  for footer:

```
    position: fixed;
    bottom: 0:
```

- **sticky** : The element is positioned based on the user's scroll position.
  The element gets fixed once user reaches the element after scrolling.

  Eg.

  ```
  #box{
    position: sticky;
    top: 0;
    left: 50px;
  }
  ```

```

## z-index:
The z-index property specifies the stack order of an element. An element with a higher z-index will be displayed above an element with a lower z-index, on the stack organization.
- By default the z-index of every element is zero
- > z-index: auto(0)
  > z-index: 1/2/3/.... (above the default)
  > z-index: -1/-2/-3/.... (below the default)
- z-index does not apply when the position is static.


## Backgroung-image:

The background-image property sets one or more background images for an element.

```

#box{
background-image: url('image.jpg');
}

```

- Along with background-image attribute, its always essential to use **background-size** attribute.
- **background-size** decides how the image fits in the web page.
- background-size: auto/cover/contain
- **auto**: The background image is displayed in its original size.
- **cover**: The background image covers the entire container, but may be cropped.
- **contain**: The background image is resized to fit inside the container, while maintaining its aspect ratio.
- Its always preferable to use *cover* for this attribute.
- **background-repeat**: specifies how the background image should be repeated.

```

#box{
background-image: url('image.jpg');
background-size: cover;
background-repeat: no-repeat;
}

```

## Flexbox:
It is a one-dimensional layout method for arranging items in rows and columns.

The flex model:
[flex model](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR4pGAAoVbB_iUf3UY2O-AbxsvwrFT8rb5y8w&s)

**Flex container**:
The container for which the display property is set to be flex.

### Flexbox Properties:
1. **Flexbox Direction
It sets how flex items are placed in the flex container, along which axis and direction.

- flex-direction: row; (default)
- flex-direction: column;  
- flex-direction: row-reverse;
- flex-direction: column-reverse;

**NOTE**: If a container is set to be flex then all the items inside the container would always fit itself inside the border of the container only till its font size(size of content) allows to do it though its dimesions are set otherwise.

2. **Flex properties for Flex Container**:
- justify-content: alignment along the main axis.

  flex-start/flex-end/centre/space-evenly/space-around/space-between

- align-items: alignment along the cross axis.
flex-start/flex-end/centre/stretch/baseline

- align-content: alignment of multiple lines along the cross axis.
flex-start/flex-end/centre/stretch/space-evenly/space-around/space-between

- flex-wrap: 
wrap/wrap-reverse/nowrap

3. **Flex properties for Flex Item**:
- flex-grow: specifies how much the item should grow relative to the other items in the flex container
- flex-shrink: specifies how much the item should shrink relative to the other items in the flex
- align-self: alignment of individual along the cross axis.

