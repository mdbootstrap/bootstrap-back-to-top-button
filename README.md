# Bootstrap Scroll Back To Top button - examples & tutorial

Back To Top button built with Bootstrap 5. Learn how to create a button that appears when you start scrolling and, when clicked, takes you to the top of the page.

To learn more read [Buttons Docs](https://mdbootstrap.com/docs/standard/components/buttons/).

## Basic example

HTML
```html
<!-- Back to top button -->
<button type="button" class="btn btn-danger btn-floating btn-lg" id="btn-back-to-top">
  <i class="fas fa-arrow-up"></i>
</button>

<!-- Explanation -->
<div class="container mt-4 text-center" style="height: 2000px;">
  <p>
    Start scrolling the page and a strong
    <strong>"Back to top" button </strong> will appear in the
    <strong>bottom right corner</strong> of the screen.
  </p>

  <p>
    Click this button and you will be taken to the top of the page.
  </p>
</div>
```

CSS
```css
#btn-back-to-top {
  position: fixed;
  bottom: 20px;
  right: 20px;
  display: none;
}
```
JavaScript
```javascript
//Get the button
let mybutton = document.getElementById("btn-back-to-top");

// When the user scrolls down 20px from the top of the document, show the button
window.onscroll = function () {
  scrollFunction();
};

function scrollFunction() {
  if (
    document.body.scrollTop > 20 ||
    document.documentElement.scrollTop > 20
  ) {
    mybutton.style.display = "block";
  } else {
    mybutton.style.display = "none";
  }
}
// When the user clicks on the button, scroll to the top of the document
mybutton.addEventListener("click", backToTop);

function backToTop() {
  document.body.scrollTop = 0;
  document.documentElement.scrollTop = 0;
}
```

#### Much more examples and a detailed description can be found at [📄 Scroll Back To Top button documentation page]https://mdbootstrap.com/docs/standard/extended/back-to-top/)
