# Flexbox Fundamentals

## Demystifying alignment in flexbox children

**[📹 Video](https://egghead.io/lessons/flexbox-demystifying-alignment-in-flexbox-children)**

Because flexbox layout is so * *ahem* * flexible, it can be difficult to remember which properties do what and what values to use when you need an element to be positioned just right in the browser.

In this lesson, the following properties are detailed:

- `justify-content`
- `align-items`
- `align-self`

The values for each of these properties will be detailed, as well.

---

### Before we jump in, let's get a quick refresher on `flex-direction` 👍:

`flex-direction` defaults to row which is displayed horizontally.

Following the transcript, we can note that this flexbox property's value can be changed to:

- `row` – This is the default position for the `flex-direction` property.
- `row-reverse` – The children will flow from left to right.
- `column`– The column will display vertically.
- `column-reverse` - The children to flow from bottom to top.

---

## Alignment via flexbox children properties

### `justify-content` affects way the children are aligned along the direction the content is flowing.

In other words, depending on where your element starts, the justify-content will affect how the extra space along the flex directioin is used.

Think about it: Is your flex-direction set to `row` (that's horizontally)? Then, `justify-content` will affect the extra space at the top, or start, of your element... but, *why?*

It's because `justify-content` defaults to `flex-start` meaning that the child will crop up the its starting point. In the case of Garth's example, the children are all starting at the top.

#### `justify-content` values include:
-   `flex-start`    - the child will start at the container's top
-   `flex-end`  - the child will start at the container's bottom
-   `center`    - the child will start at the center, or in the middle, of the container
-   `space-between` - if there are multiple child elements, this value will stick one child to the start of the flow and the last child to the end, with the children in between spaced out evenly.
-   `space-around`  - the space around each child will be evenly distributed.

🤔 Learn more about justify-content values, including `initial` and `inherit` here: [MDN web docs – justify-content](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content)

---

### `align-items` declares how to use the space perpendicular to the `flex-direction`

`align-items` defaults to stretch. Because of this, your browser will show the child element at 100% of its container height.

#### To move items within their containers, you can use `align-items` values which include:

-   `flex-start`    - this will move your children to the top
-   `flex-end`  - this will move your children to the bottom
-   `flex-center`   - this will move your children to the center
-   `flex-baseline` - this will move your children to the baseline of the first line of text in the element.

---

### `align-self` is the same as `align-item` but is applied to specific, individual children

`align-self` defaults to `auto`, meaning that it will do whatever `align-item` tells it to do.

So if you want a specific child to display in the container in a way that's different from the other children, you'll have to give it a value to `align-self`.

🤔 Resources for alignment: [align-items](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items), [align-self property](https://www.w3schools.com/CSSref/css3_pr_align-self.asp)