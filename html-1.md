# HTML

## HTML-1

> Default Encoding - UTF-8
> DOM Model

[CSS styles used](#css-styles-used)
[HTML Entities](#html-entities)
[Tables](#tables)
[Generic Elements](#generic-elements)
[Semantic Elements](#semantic-elements)
[CSS Order](#css-order)
[Relational Selectors](#relational-selectors)
[Pseudo - Class Selectors](#pseudo---class-selectors)
[Pseudo - Element Selectors](#pseudo---element-selectors)
[Selector Specificity](#selector-specificity)
[Colors](#colors)
[Gradients](#gradients)

### CSS styles used

- class - (.)
- id - (#)
- tag - (div)
- attributte - (a[])

---

### HTML Entities

- &lt; - `&lt;`
- &gt; - `&gt;`
- &amp; - `&amp;`
- &quot; - `&quot;`
- &apos; - `&apos;`
- &copy; - `&copy;`
- &nbsp; - `&nbsp;`

---

### Tables

- tr - table row
- td - table data
- th - table header
- thead - table header
- tbody - table body
- tfoot - table footer
- col - table column
- colgroup - table column group
- caption - table caption

---

#### Generic Elements

- div
- span

#### Semantic Elements

- article
- figure
- mark
- time
- figure

---

### CSS Order

- Order of CSS Importance
`Inline styles > Embedded > External`
- Order of CSS Specificity
`Inline styles > Embedded > External > ID > Class > Element > Pseudo-classes > P
seudo-elements > Attribute > Negation > Inheritance > Initial value`
- Order of CSS Cascade
`!important > Inline styles > Embedded > External > ID > Class > Element > Pseudo
-classes > Pseudo-elements > Attribute > Negation > Inheritance > Initial value`
- Order of CSS Priority
`!important > Inline styles > Embedded > External > ID > Class > Element > Pseudo
-classes > Pseudo-elements > Attribute > Negation > Inheritance > Initial value`

---

### Relational Selectors

- `> - Direct child`
- `+ - Adjacent sibling`
- `~ - General sibling`

---

### Pseudo - Class Selectors

- `:first-child`
- `:last-child`
- `:nth-child(n)`
- `:nth-last-child(n)`
- `:nth-of-type(n)`
- `:nth-last-of-type(n)`
- `:only-child`
- `:only-of-type`
- `:empty`
- `:link`
- `:visited`
- `:hover`
- `:active`
- `:focus`
- `:target`
- `:enabled`
- `:disabled`
- `:checked`
- `:not(s)`
- `:root`
- `:first-of-type`
- `:last-of-type`
- `:only-of-type`

---

### Pseudo - Element Selectors

- `::first-letter`
- `::first-line`
- `::before`
- `::after`
- `::selection`
- `::placeholder`

---

### Selector Specificity

`(a,b,c)`

- `a - Number of ID selectors`
- `b - Number of Class selectors, Attribute selectors, and Pseudo-classes`
- `c - Number of Type selectors, Universal selectors, Subselectors, and Pseudo-elements`

---

#### Colors

- Named Colors
- RGB
- RGBA
- HSL
- HSLA
- Hexadecimal

---

#### Gradients

(position,color1,color2)

- `linear-gradient`
- `radial-gradient`
- `repeating-linear-gradient`
- `repeating-radial-gradient`

---

`object-fit : cover`
`box-shadow: 10px`

> Normalize CSS whenever possible
> Use HTML and CSS Validators
