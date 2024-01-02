# drop-down-func

- hide or show element on click.

## how to use this?

parameter => element toggler, element data attribute value, element data attribute, classList to show drop down element, active-toggler, close drop down element when this is clicked

```css
/* style menu item */
.active-toggler {
  background-color: black;
  color: white;
}

/* show sub menu item */
.visible {
  display: block;
}
```

```html
<div id="main-container">
  <header>
    <nav id="nav-bar">
      <ul class="nav-bar-contents">
        <li class="nav-bar-list">
          <div class="nav-bar-item" data-nav-bar-item="1">home</div>
          <div class="nav-sub-item" data-nav-sub-item="1">
            <ul class="nav-bar-links">
              <li>
                <a class="nav-bar-link" href="">nav-bar-link</a>
              </li>
              <li>
                <a class="nav-bar-link" href="">nav-bar-link</a>
              </li>
              <li>
                <a class="nav-bar-link" href="">nav-bar-link</a>
              </li>
              <li>
                <a class="nav-bar-link" href="">nav-bar-link</a>
              </li>
              <li>
                <a class="nav-bar-link" href="">nav-bar-link</a>
              </li>
            </ul>
          </div>
        </li>
      </ul>
    </nav>
  </header>
</div>
```

```js
import dropDown from "@aloe_vera/drop-down-func/package/nav-func";

const navBarItem = document.querySelectorAll("div[data-nav-bar-item]");

dropDown({
  // toggler
  elementToListen: navBarItem,
  itsDataAttribute: "data-nav-bar-item",

  // toggle classList to
  subElement: "div[data-nav-sub-item",
  classListValue: "visible",

  togglerClassListValue: "active-toggler",

  // toggle toggler and it's sub element using a main container here or a cross
  closerToggler: 'div[id="main-container"]',
}).dropDownElement();
```
