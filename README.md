# javascript-snippets
Javascript snippets and examples.

### onclick event
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

```
let myImage = document.querySelector("img");

myImage.onclick = function() {
    let mySrc = myImage.getAttribute("src");
    if (mySrc === "{{ site.baseurl }}/assets/images/GitHub_Logo.png") {
        myImage.setAttribute("src", "{{ site.baseurl }}/assets/images/github-mark.png");
        myImage.alt = "github mark";
        myImage.style.width = "35%";
    } else {
        myImage.setAttribute("src", "{{ site.baseurl }}/assets/images/GitHub_Logo.png");
        myImage.alt = "github logo";
        myImage.style.width = "50%";
    }
}
```
