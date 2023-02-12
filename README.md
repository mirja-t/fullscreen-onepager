![Fullpage-Onepager-Logo](/dist/assets/images/fullscreen-onepager-logo.png "Fullpage-Onepager-Logo")

# Fullscreen Onepager

This Application displays the sections of a Onepager as fullscreen pages with page transition.

## Structure

There has to be a wrapping container. Inside that wrapper, there is a navigation and the container for the sections.

```
<div id="fullpagewrapper">
    <nav id="nav">
        <ul>
            <li id="section-0" class="active"><a href="#section-0">Section 1</a></li>
            <li id="section-1"><a href="#section-1">Section 2</a></li>
            <li id="section-2"><a href="#section-2">Section 3</a></li>
        </ul>
    </nav>
    <main id="fullpage" class="main-container">
        <section id="home" class="section active">
            <div class="container">
                ...
            </div>
        </section>
         <section id="home" class="section active">
            <div class="container">
                ...
            </div>
        </section>
    </main>
</div>
```

## Initialization

The fullpage class is initialized with 3 mandatory arguments:

* The wrapping container
* The sections-wrapper
* The navigation (must contain the nav elements as direct children)

The fourth argument is optional: 

##### The config object

The config object expects a key 'breakpoint'. On viewports below that breakpoint, the whole page is scrollable.

```
const fpwrapper = document.getElementById('fullpagewrapper');
const fp = document.getElementById('fullpage');
const nav = document.querySelector('nav#nav ul');
const config = {
    breakpoint: 991
}
const fullpage = new Fullpage(fpwrapper, fp, nav, config);
```

## Demo site

[fullscreen-onepager.netlify.app](https://fullscreen-onepager.netlify.app/) 

![Fullpage-Onepager-Screenshot](/dist/assets/images/fullscreen-onepager-screenshot.jpg "Fullpage-Onepager-Screenshot")

