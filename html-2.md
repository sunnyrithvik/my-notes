# HTML & CSS

## HTML - II

## Layouts

### Box Model

- content
- padding
- border
- margin

> margin collapsing
        merging two margins

### Sizing Elements

> - By default, width and height property is applied to content box i.e. box-sizing: content-box
> - To apply width and height to the border box, we need to use box-sizing: border-box
> 
> - content in universal selectors in css does not apply to pseudo elements
> - We have to specify in universal selectors for pseudo elements
> - We can use *::before and *::after to add pseudo elements to all elements
> - width and height properties are applied to only block level elements
> - Inline elements does not follow width and height properties

#### Display property

- `inline`
- `block`
- `inline-block`
- `none`
- `table`
- `flex`
- `grid`

### Overflowing

- `visible` (default)
- `hidden`
- `scroll`
- `auto`

> overflow : overflow-x + overflow-y

### Measuring Units

#### Absolute

- `px(pixel)`
- `pt(point)`
- `in(inch)`
- `cm(cm)`
- `mm(mm)`

#### Relative

- `%` - relative to the size of the parent(container)
- `em` - relative to the font size of the element
- `rem` - relative to the font size of the root element
- `vw` - relative to 1% of the viewport width
- `vh` - relative to 1% of the viewport height
- `vmin` - relative to the smaller of `vw` and `vh`
- `vmax` - relative to the larger of `vw` and `vh`

### Positioning

- `position: static` (default)
- `position: relative` - relative to its normal position
- `position: absolute` - relative to the nearest positioned ancestor
(The container must be positioned relative and it is by default removed from normal flow of the page)
- `position: fixed` - relative to the viewport
- `position: sticky` - relative to the viewport, but only when the element is scrolled into
view. Otherwise, it behaves like `relative`

> To change the order of appearance

- `z-index: 1` (on the top)
- `z-index: -1` (behind)

### Floating Elements

- `float: none` (default)
- `float: left`
- `float: right`

> To clear items (on same direction)

- `clear: none` (default)
- `clear: left`
- `clear: right`
- `clear: both`

- parent collapsing of float elements
(parent elements do not see floated elements)

Method 1:

- use div with a property of clear

```html
<div style="clear: both;"></div>
```

Method 2:

- use clearfix class in parent

```css
clearfix::after {
    content: "";
    display: block;
    clear: both;
}
```

Method 3: (avoid)

- use overflow: hidden on the parent element

### Flexbox

- `flex-direction: row`
- `flex-direction: column`
- `flex-direction: row-reverse`
- `flex-direction: column-reverse`

```css
display: flex,
flex-direction: column
```

Axes

- main axis(primary)
- cross axis(secondary)

#### Aligning items

- justify-content (along the main axis)
- align-items (along the cross axis)
- align-content (along the cross axis)

- `justify-content: flex-start`
- `justify-content: flex-end`
- `justify-content: center`
- `justify-content: space-between`
- `justify-content: space-around`
- `justify-content: space-evenly`
- `align-items: flex-start`
- `align-items: flex-end`
- `align-items: center`
- `align-items: baseline`
- `align-items: stretch`

For multiple lines we use align-content

- `align-content: center`
- `align-content: flex-start` (default)
- `align-content: flex-end`
- `align-content: space-between`
- `align-content: space-around`
- `align-content: space-evenly`
- `flex-wrap: nowrap` (default)
- `flex-wrap: wrap`
- `flex-wrap: wrap-reverse`

For alignment of individual items(flex items) we use align-self

- `align-self: center`
- `align-self: flex-start`
- `align-self: flex-end`
- `align-self: stretch` (default)
- `align-self: baseline`

#### Sizing Items (on flex items)

- `flex-basis` (the initial size of a flex item)
- `flex-grow` (the amount of space a flex item can take up)
- `flex-shrink` (the amount of space a flex item can shrink by)
- `flex`

##### Flex syntax

- flex (flex-grow, flex-shrink, flex-basis)
- flex (flex-grow, flex-shrink or flex-basis)
- flex (flex-grow or flex-shrink)

### Grid

- `display: grid`
- `grid-template-rows: repeat(3, 100px);`
- `grid-template-columns: repeat(2, 100px);`
- `grid-template: repeat(3, 100px) / repeat(2, 100px)`
- `grid-template: repeat(3, 100px) / 30% 70%`
- `grid-template: 100px auto 100px / 100px 30fr 70fr`
- `grid-template-areas: "header header" "main main sidebar" "footer footer
footer";`

#### Aligning Items

- `justify-items` (along the horizontal axis)
- `align-items` (along the vertical axis)

> Note:
>
> - `justify-items` and `align-items` are the same as `justify-content` and `align-content` for flexbox, except that they apply to the grid container's children, not the grid container itself.
> - content is used for entire grid
> - items is used for individual items
> - default value of `justify-items` and `align-items` is `stretch`

#### Gap

- `row-gap`
- `column-gap`
- `gap` (default value is 0px)
- `gap (row-gap, column-gap)`

#### Placing Items

- `grid-row`
- `grid-column`
- `grid-area`

> Examples:
> `grid-column: 1 / 3`
> `grid-column: 1 / -1`
> `grid-column: 1 / span 2`
> `grid-area: (start)(r/c)/ (end)(r/c)`
> `grid-area: 1/1 / 1/3`
> `grid-area: header or main or footer or sidebar`
> For empty cell use .(dot) in grid-template-areas
