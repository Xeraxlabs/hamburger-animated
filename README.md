# hamburger-animated

A simple animated hamburger component, It can be easily modified and used for your project, A complete guide about how to build this project from scratch is covered in this [Youtube video](https://www.youtube.com/)

### Recommended sizes

If you intend to use the hamburger component for your project the 150px width and height might just be too big unless you are building for ultra wide screens, Below we have compiled a width and height that would be suitable for most mobile devices, you can decide to use them or follow the guide in deciding what size works best for you.

```css
.hamburger {
  width: 45px;
  height: 45px;
}
```

You might just notice that after reducing the hamburger menu's size the vertical spacing between the bars are just too much, you need to reduce the translateY values so they can match your hamburger;

```css
.bars::before {
  transform: translateY(-8px);
}
.bars::after {
  transform: translateY(8px);
}
```

This fixes it for the most part, You can decide to come with up with your values, remove the background and border radius if your project deos not require them.

## Fast Lane
For users that just want to use this component right away, just copy the HTML, CSS and Javascript Snippet below and ensure you link them properly and everything should work just fine, If you chang the class names, ensure to update them in the HTML,CSS and JS files respectively. You can watch the full video of how to build this project [Here](https://www.youtube.com/)

### HTML

```html
<!--  Animated hamburger menu starts here -->

 <div class="hamburger" onclick="toggleClassName()">
     <div class="bars"></div>
 </div>
 
 <!--  Animated hamburger menu ends here -->


```
### CSS

```css
/* Animated Hamburger menu starts here */

.hamburger {
    width: 45px;
    height: 45px;
    background: tomato;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    transition: all 0.4s ease;
    transform: translateY(-20px);

}

.hamburger:hover {
    transform: translateY(0);
}

.bars {
    background: #fff;
    height: 3px;
    width: 60%;
    position: relative;
    display: flex;
    justify-content: center;
    transition: transform 0.4s ease;

}

.bars::before {
    content: '';
    width: 80%;
    height: 3px;
    background: #fff;
    position: absolute;
    transform: translateY(-8px);

}

.bars::after {
    content: '';
    width: 80%;
    height: 3px;
    background: #fff;
    position: absolute;
    transform: translateY(8px);
}

.crossburger {
    background: black;
}

.crossburger .bars {
    background: transparent;
    transform: rotate(180deg);
}

.crossburger .bars::before {
    transform: translateY(0px) rotate(45deg);
}

.crossburger .bars::after {
    transform: translateY(0px) rotate(-45deg);

}
/* Animated Hamburger menu ends here */


```
### JS

```javascript
// Animated hamburger menu starts here

var hamburgerdiv = document.querySelector(".hamburger")
function toggleClassName() {
    hamburgerdiv.classList.toggle('crossburger')
}

// Animated hamburger menu ends here


```

## License

Hamburger is licensed under the [MIT license](http://opensource.org/licenses/MIT).

## Related

- [Dx-explore](https://github.com/Xeraxlabs/dx-explore)
