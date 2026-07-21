# CSS Fundamentals Notes

# CSS Units

CSS units define the size of elements, text, spacing, and other properties. Choosing the right unit is important for creating responsive and accessible websites.

---

# Types of CSS Units

CSS units are divided into two categories:

1. Absolute Units
2. Relative Units

---

# 1. Absolute Units

Absolute units have a fixed size. They remain the same regardless of screen size or parent elements.

| Unit | Meaning     | 
| ---- | ----------- | 
| px   | Pixels      |
| cm   | Centimeters | 
| mm   | Millimeters | 
| in   | Inches      | 
| pt   | Points      | 
| pc   | Picas       | 

# 2. Relative Units

Relative units depend on another value such as the viewport or parent element.

#### em
#### rem
#### %
#### vw (Viewport Width)
#### vh (Viewport Height)

---

# CSS Typography

Typography is the art of displaying text beautifully and readably.

It controls:

* Font
* Size
* Weight
* Style
* Alignment
* Decoration
* Line spacing
* Letter spacing

---

# Text Properties

## color

```css
p{
    color:red;
}
```

Changes text color.

---

## text-align

```css
h1{
    text-align:center;
}
```

Values

* left
* right
* center
* justify

---

## text-decoration

```css
a{
    text-decoration:none;
}
```

Values

* underline
* overline
* line-through
* none

---

## text-transform

```css
text-transform:uppercase;
```

Values

* uppercase
* lowercase
* capitalize

---


## letter-spacing

```css
letter-spacing:5px;
```

Controls space between letters.

---

## word-spacing

```css
word-spacing:15px;
```

Controls space between words.

---


## text-shadow

```css
text-shadow:2px 2px 5px gray;
```

Adds shadow to text.

---

# Font Properties

## font-family

```css
font-family:Arial, sans-serif;
```

Specifies the font.

---

## font-size

```css
font-size:20px;
```

Controls text size.

---

## font-weight

```css
font-weight:bold;
```

Values

100–900

---

## font-style

```css
font-style:italic;
```
---

## font

Shorthand property.

```css
font:italic bold 20px Arial;
```

Order:

```
Style
Weight
Size
Family
```

---

# @font-face

Allows custom fonts.

```css
@font-face{
    font-family:"MyFont";
    src:url("fonts/myfont.ttf");
}

h1{
    font-family:"MyFont";
}
```

### Why use @font-face?

* Custom branding
* Unique typography
* Offline fonts
* No dependency on installed fonts

---

# CSS Colors

CSS supports multiple ways to define colors.

---

# 1. Named Colors

```css
color:red;
background:blue;
```

Examples

* red
* green
* yellow
* black
* white
* orange
* purple
* cyan

There are about **140+ predefined color names** in CSS.

---

# 2. Hexadecimal Colors

Format

```
#RRGGBB
```

Example

```css
color:#FF0000;
```

Breaking it down:

```
RR = Red
GG = Green
BB = Blue
```

Each pair ranges from:

```
00 → FF
```

Decimal

```
0 → 255
```

### Common Colors

| Color  | Hex     |
| ------ | ------- |
| Red    | #FF0000 |
| Green  | #00FF00 |
| Blue   | #0000FF |
| White  | #FFFFFF |
| Black  | #000000 |
| Yellow | #FFFF00 |

---

# 3. RGB

Format

```css
rgb(red,green,blue)
```

Example

```css
color:rgb(255,0,0);
```

Range

```
0-255
```

---

# RGBA

A = Alpha (Opacity)

```css
rgba(255,0,0,0.5)
```

Opacity

```
0 = Transparent

1 = Fully Visible
```

---

# 4. HSL

Hue

Saturation

Lightness

```css
hsl(120,100%,50%)
```

### Hue

```
0 → 360 degrees
```

0

↓

Red

120

↓

Green

240

↓

Blue

360

↓

Red again

---

### Saturation

```
0%
```

Gray

```
100%
```

Pure color

---

### Lightness

```
0%
```

Black

```
50%
```

Original color

```
100%
```

White

---

# HSLA

```css
hsla(120,100%,50%,0.5)
```

Alpha controls opacity.

---

# CSS Box Model

Every HTML element is considered a rectangular box.

```
+---------------------------+
|         Margin            |
|  +---------------------+  |
|  |      Border         |  |
|  | +---------------+   |  |
|  | |   Padding     |   |  |
|  | | +-----------+ |   |  |
|  | | | Content   | |   |  |
|  | | +-----------+ |   |  |
|  | +---------------+   |  |
|  +---------------------+  |
+---------------------------+
```

The box consists of:

1. Content
2. Padding
3. Border
4. Margin

---

# Border Properties

## border

```css
border:2px solid black;
```

---

## border-width

```css
border-width:5px;
```

---

## border-style

```css
border-style:dashed;
```

Values include:

* solid
* dashed
* dotted
* double
* groove
* ridge
* inset
* outset
* none

---

## border-color

```css
border-color:red;
```

---

## border-radius

```css
border-radius:20px;
```

Makes rounded corners.

Circle

```css
border-radius:50%;
```

---

# Padding

Padding is the space **inside** the border, between the content and the border.

```css
padding:20px;
```

Shorthand

```css
padding:10px 20px 30px 40px;
```

Order

```
Top

Right

Bottom

Left
```

---

# Margin

Margin is the space **outside** the border.

```css
margin:20px;
```

Auto Center

```css
width:300px;
margin:auto;
```

---

# Box Sizing

By default,

```css
box-sizing:content-box;
```

Width only includes content.

Example

```css
width:200px;
padding:20px;
border:5px solid;
```

Actual width becomes

```
250px
```

---

# border-box

```css
box-sizing:border-box;
```

Now,

Width already includes

* Content
* Padding
* Border

Final width remains

```
200px
```

---

# Why Use border-box?

Almost every modern project starts with

```css
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}
```

---
