# Rose Filter

## Learning Objective

- Understand relevance of hexadecimal arithmatic to CSS, create
  prototype of popular app (Instagram)

## Prompt

Design a simple web app that features a color swatch preview (in 6 color hex notation, e.g. #a02bff), and filter button. When pressed, the filter button should apply a 'Rose' fitler, making the color of the swatch 20% more red, 10% less green, and 10% more blue. You should write this web app in pure JS, HTML, and CSS if possible.

## Interviewer Strategy Guide

- This problem involves knowing how CSS represents colors with 6-digit hex strings, as well as converting between base 10 and base 16.

- A CSS color string (eg, `#F3A256`) actually is a concatenation of 3 2-digit hex strings ranging from 0 to 255 (FF in hex), for the Red, Green, and Blue Saturation of a color.

- Prompt interviewee for how they would subtract 10% for the B/G values (10% must be converted to hexadecimal, which is 25)

- How does the interviewee plan to handle edge cases when the RGB value is is already at its max or min values (0 or 255)

- `ParseInt()` is a handy method for base conversions!

- Once the logical approach is solidified, how do we wire it together within the callback function of a click handler?

### Notes

Good sub-questions to ask:

- How is measuring a number hexadecimal (base-16) different from decimal (base-10). What is 10% in base-16?

- How is a 6-digit hex string constructed? How do those values correspond the a given RGB color value?

- How can we convert numbers from decimal to hex, and vice versa?

- What are some edge cases to consider? What if a color is completely saturated (#FF) or completely unsaturated (#00)?

- [js-fiddle](https://jsfiddle.net/d1oescjn/)

### Starting Point

```html
<body>
  <div id="swatch"></div>
  <p>You are viewing: <span id="value"></span></p>
  <button id="filter">Rose Filter</button>
</body>
```

```css
#swatch {
  height: 250px;
  width: 250px;
  border: 2px solid black;
}
```

```javascript
let colorStr = "1AB20D";
const swatch = document.getElementById("swatch");
const span = document.getElementById("value");
const roseBtn = document.getElementById("filter");
swatch.style.backgroundColor = span.innerHTML = `#${colorStr}`;
// Your Code Below
```

[jsfiddle](https://jsfiddle.net/Lvkcbtq9/)
