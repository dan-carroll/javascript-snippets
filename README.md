# javascript-snippets
Javascript snippets and examples.

This code snippet from the [Adding an image changer](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics#adding_an_image_changer) section of the "JavaScript basics" page from the "mdn web docs Getting started with the web Guide" did not work correctly with ".onclick" event.

```
const myImage = document.querySelector("img");

myImage.onclick = () => {
  const mySrc = myImage.getAttribute("src");
  if (mySrc === "images/firefox-icon.png") {
    myImage.setAttribute("src", "images/firefox2.png");
  } else {
    myImage.setAttribute("src", "images/firefox-icon.png");
  }
};
```

What did work for me may have been due to the browser and JavaScript engine being utilized. (Google Chrome Version 114.0.5735.111 on Windows 10).

