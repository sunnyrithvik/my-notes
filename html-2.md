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
