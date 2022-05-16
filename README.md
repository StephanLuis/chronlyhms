<div id="top"></div>

<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

[![npm bundle size][npm-bundle-size]][npm-bundle-size]
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![RepoSize][reposize-shield]][reposize-url]




<!-- PROJECT LOGO -->
<br />
<div align="center">
  
  
  <a href="https://github.com/StephanLuis/chronlyhms">
    <img src="readme/logo.svg" alt="Logo" width="90" height="90">
  </a>

  <h3 align="center">ChronlyHMS-- Best 'Time Only' Input</h3>

  <p align="center">
    A 'time only' input that works on Safari in very close imitation of a time input on Chrome.  Time spans up to 999 hrs are natively implemented as well as small time spans to 1 millisecond.<br> </p>
    <br />
    <a href="https://github.com/StephanLuis/chronlyhms"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="http://practisemaster.com/demos/chronoHMStest.html">View Demo</a>
    ·
    <a href="https://github.com/StephanLuis/chronlyhms/issues">Report Bug</a>
    ·
    <a href="https://github.com/StephanLuis/chronlyhms/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

<!-- [![Product Name Screen Shot][product-screenshot]](https://example.com) -->

Yes! It seems CRAZY in 2022 that there is not a native 'time only' input for HTML.  <br>No user input control for time that is not rendered independant of date or time of day.  ChronlyHMS is for a value of time  as hours, minutes, seconds <b>only</b>! <br> Why is it difficult to 'code' a countdown timer? Why can't it be done with one control, look at google's timer and other coundown timers! All use multiple inputs.  Shouldn't a user be able to 'scientifically' specify a time with one control?  <br>The closest HTML5 input type- time when configured with UX for hours to millisecs is very finicky and rendered differently on Chrome and Safari <b>and</b> mobile is different from laptop, so I've simplified that!

<img src="readme/html.png" alt="drawing" width="60%"/>

<!-- [![HTML Screen Shot][html-screenshot]](https://example.com) -->

The very worst is Safari on desktop and mobile undermine those snazzy input type=time efforts and update the input depending on OS settings for desktop or provide a control with restricted capability...

<img src="readme/safariBad.png" alt="drawing" width="60%"/>
<!-- [![Safari Screen Shot][safari-screenshot]](https://example.com) -->


<h3> Bob is rescued by ChronlyHMS! </h3>

The objective is a minimised vanilla javascript plugin that reproduces the behaviour of the input type=time on Chrome.  This way at least two of the major browsers are supported, Safari and Chrome, on desktop and mobile operating systems. 

<i>Does this loose any functionality?</i>  No!  document.querySelector('#bob').value  has a getter and setter!  So values can be set and retrieved by ID.


There are a few plugins (links to come), but controls with the plugin still treated time as a date (ex 24hr max).  Still it seems in 2022 the most relable is multi input (more links to come ), the best example is the Google countdown timer.  And that's wrong because time is a basic unit that should be separate from calendar complexities.  That got me thinking, why isn't there an input control for it implemented across browsers??  I needed one so coded ChronlyHMS.

Here's why:
* Time is hours minutes and seconds (and millisecs) and needn't be associated with part of a day or a date
* The date association breaks UX and is varied with browser implementation
* I found no other crossbrowser solution
* I thought this would be a great open source project
* So there is no need to continue modifying number inputs for use with time 

Of course, this is functional and in it's infancy.  With some contribution this is a project that can inspire change to the HTML spec.


Feel free to vote for WhatWG inclusion of a into the HTML spec! (link comming soon)

<p align="right">(<a href="#top">back to top</a>)</p>



### Built With

This section should lists any major frameworks/libraries used to for this project. Any add-ons/plugins are in the acknowledgements section.

* [Node.js](https://nodejs.org/)
* [Webpack](https://webpack.js.org/)
* [Gitpod](https://www.gitpod.io/)
* [OpenSauce](https://angular.io/)
* [Selenium](https://www.selenium.dev/)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

There are no pre-requisites for using ChronlyHMS if you're not compiling/ packaging you javascript.  If you are packaging:

### Prerequisites

This is an example of how to get started with npm and webpack, other frameworks should work too.
* npm & webpack
  ```sh
  npm install npm@latest -g
  npm init -y
  npm install webpack webpack-cli --save-dev
  ```
  * Webpack requires configuration for packaging ChronlyHMS CSS
  see [Webpack CSS Loader](https://webpack.js.org/loaders/css-loader/)
  

### Installation

With packaging:
_Below is an example of how you can instruct your audience on installing and setting up your app. This template doesn't rely on any external dependencies or services._

1. Install from NPM
 ```sh
  npm i chronlyhms
 ```
2. import ChronlyHMS javascript and css
 ```sh
 import ChronlyHMS from 'chronlyhms';
 import 'chronlyhms/src/chrono.css'
```
  
Without packaging:

1. Add script:
 ```sh
 <script src="https://cdn.jsdelivr.net/npm/chronlyhms@1.0.65/dist/chronoBundle.min.js"></script>
  
 ```


<p align="right">(<a href="#top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

ChronlyHMS requires an input element with the attribute 'data-univHMS'.  There's no more code than that needed.  
```sh
<input id='bob' data-univHMS></input>
```

_For more examples, please refer to the source of  [chronoHMStest](http://practisemaster.com/demos/chronoHMStest.html)_

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [x] Emperically determine <input type="time"> behaviour
- [x] Reverse engineer input behaviour (arrows, digits, 0 addition, etc.)
- [x] Cross browser/ cross os manual tests  
- [ ] Get Chrome behavioural specification for <input type="time">
- [ ] Add end to end multi-browser, multi-os Selinium tests
- [ ] Update demo page (either PM.com or JSfiddle type)
- [ ] Multi-language documentation (Google translate of this page?)
    - [ ] Chinese
    - [ ] Spanish

See the [open issues](https://github.com/StephanLuis/chronlyhms/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See [`LICENSE.txt`](https://github.com/StephanLuis/chronlyhms/blob/main/LICENSE)  for more information.

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Stephan Luis - stephan@learnsense.org

Project Link: [https://github.com/StephanLuis/chronlyhms](https://github.com/StephanLuis/chronlyhms)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Resources I've found helpful and would like to give credit to:


* [GitHub Pages](https://pages.github.com)
* [Font Awesome](https://fontawesome.com)
* [Best Readme](https://github.com/othneildrew/Best-README-Template)
* [Img Shields](https://shields.io)



<p align="right">(<a href="#top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->


[contributors-shield]: https://img.shields.io/github/contributors/StephanLuis/chronlyhms?style=for-the-badge
[contributors-url]: https://github.com/StephanLuis/chronlyhms/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/StephanLuis/chronlyhms?style=for-the-badge
[forks-url]: https://github.com/StephanLuis/chronlyhms/network/members
[stars-shield]: https://img.shields.io/github/stars/StephanLuis/chronlyhms?style=for-the-badge
[stars-url]: https://github.com/StephanLuis/chronlyhms/stargazers
[issues-shield]: https://img.shields.io/github/issues/StephanLuis/chronlyhms?style=for-the-badge
[issues-url]: https://github.com/StephanLuis/chronlyhms/issues
[license-shield]: https://img.shields.io/github/license/StephanLuis/chronlyhms?style=for-the-badge
[license-url]: https://github.com/StephanLuis/chronlyhms/blob/main/LICENSE
[reposize-shield]: https://img.shields.io/github/repo-size/stephanluis/chronlyhms?style=for-the-badge
[reposize-url]: https://github.com/StephanLuis/chronlyhms
[product-screenshot]: images/screenshot.png
[npm-bundle-size]: https://img.shields.io/bundlephobia/minzip/chronlyhms?style=for-the-badge

[html-screenshot]: readme/html.png
[safari-screenshot]: readme/safariBad.png
