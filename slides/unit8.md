class: center, middle

# Unit 8
## Accessibility, Optimization, and Deployment

---
class: left

# Web Accessibility & \#a11y ~

> The power of the Web is in its universality. Access by everyone regardless of disability is an essential aspect.

<cite>-- Tim Berners-Lee, W3C Director and inventor of the World Wide Web</cite>

## The A11Y Project

A community-driven effort to make web accessibility easier. A11y offers accessibility pattern libraries, website checklists, software, tools, and other resources.

???

* [W3C Accessibility](http://www.w3.org/standards/webdesign/accessibility)
* [Web Accessibility Initiative (WAI)](http://www.w3.org/WAI/)
* [The A11y Project](https://a11yproject.com/)

---
class: left

# Broad Categories of Disabilities

### Vision impairment
### Mobility impairment
### Auditory impairment
### Cognitive impairment

---
class: left

# Vision Impairment

### Low or no vision
### Screen reader
### Braille display
### Screen magnifier
### Browser text zoom

---
class: left

# Mobility Impairment

### Limited or no use of hands
### Modified mice and keyboards
### Foot pedals
### Joysticks
### Assistive voice software

---
class: left

# Auditory Impairment

### Limited or no hearing
### Miss out on multimedia audio

---
class: left

# Cognitive Impairment

### Memory problems
### Reading and comprehension problems
### Difficulty with problem solving
### Attention limitations

---
class: left

# Accessibility 101 ~

## How Do We Make Our Websites More Accessible?

* Start with good design and great user experience (UX)
* Write standards-compliant, [semantic HTML](https://www.lifewire.com/why-use-semantic-html-3468271)
* Separate content/structure (HTML) and presentation (CSS)
* Provide alternatives when necessary (alt tags, transcripts, video captions, etc.)
* Design sites simply and clearly (which benefits _all_ users)

???

* [25 Accessibility Testing Tools](https://dynomapper.com/blog/27-accessibility-testing/246-top-25-awesome-accessibility-testing-tools-for-websites)
* [Section 508: GSA Government IT Accessibility Guide](http://section508.gov)

---
class: left

# Exercise: Accessibility Exercise

### ➡️ [Go to Exercise](https://github.com/betamore/fewd-accessibility-exercise)

**Some helpful resources:**

* [HTML: A Good Basis for Accessibility](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/HTML)
* [How to Structure an HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/How_to_structure_an_HTML_form)
* [HTML Form Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element#Forms)

---
class: left

# ARIA ~

## (Accessible Rich Internet Applications)

ARIA is a set of attributes that add accessibility information to non-semantic HTML elements. It utilizes **roles** and **properties** to provide enhanced meaning and accessibility.

```js
// Example div that is enhanced with ARIA role and attributes
<div id="percent-loaded" role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100" />
```
If you can use a native HTML element or attribute to create the necessary semantics and behavior, rather than re-purposing an element and adding an ARIA role, state or property to make it accessible, then do so.

```js
// The code below is preferable to the enhanced div above, since it utilizes the native <progress> HTML element
<progress id="percent-loaded" max="100" value="75"></progress>
```

???

* [ARIA in HTML](https://www.w3.org/TR/html-aria/)
* [ARIA | MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
* [HTML Developers: Please Consider (native HTML5 features over ARIA attributes)](http://html5doctor.com/html-developers-please-consider/)

---
class: left

# Browser & Device Testing ~

## A few ways to do it...

### Local server
### Virtual machines
### Web-based tools
### Actual (mobile) device

???

* [IE Testing with Virtual Box and Modern.ie](http://wesbos.com/ie-testing-virtual-box/)
* [Test Microsoft Edge and versions of IE6 through IE11 using free virtual machines.](https://dev.windows.com/en-us/microsoft-edge/tools/vms/)
* [Browsershots](http://browsershots.org/)
* [Screenfly](http://quirktools.com/screenfly/)
* [Responsinator Device Testing](https://www.responsinator.com/)

---
class: left

# Spinning Up a Local Server ~

## Two Basic Methods

1. From your local file system:
  * Navigate to the desired file (file can be html, css, js, img, etc.)
  * Right click the file > Open With > Chrome/Safari/Firefox/other browser of choice

2. From the command line:
  * Install `node.js`
  * Install `node-static` globally with `npm install -g node-static`
  * `cd` into your project directory
  * Run the server with `static`

???

* [Intro to Web Servers by Chris Uehlinger](http://chrisuehlinger.com/StaticWebSiteTutorial/#/)
* [Install node.js and npm on macOS](https://blog.teamtreehouse.com/install-node-js-npm-mac)
* [node-static package on npm](https://www.npmjs.com/package/node-static)
* [http-server > An alternative to node-static](https://github.com/http-party/http-server)

---
class: left

# Compression & Minification ~

### Server-side compression (via gzip) and minification of your HTML, CSS, and JS reduce the overall size of your files. This reduced file size makes them load faster in the browser, providing better UX and providing a speed/performance boost to your site's SEO.

???

* [The Difference Between Minification and Gzipping](https://css-tricks.com/the-difference-between-minification-and-gzipping/)
* [How to Minify CSS, JS, and HTML](https://codeburst.io/how-to-minify-css-js-and-html-ddd9dbea25c6)
* [Code Minifier and Beautifier Tool](http://minifycode.com/)

---
class: left

# Deploying Your Project

## There are _TONS_ of options for deploying (aka hosting) your static web projects:

* [Amazon S3](https://aws.amazon.com/getting-started/projects/host-static-website/)
* [Google Cloud or Firebase](https://cloud.google.com/solutions/web-serving-overview)
* Other cloud-based hosting > [Surge](https://surge.sh/), [Now](https://zeit.co/now), [Paperplane.io](https://www.paperplane.io/), [Aerobatic](https://www.aerobatic.com/), etc.
* Cheapo hosting > GoDaddy, HostGator, Bluehost, etc.

We are going to try out these 2:

* [GitHub Pages](https://help.github.com/en/categories/github-pages-basics)
* [Netlify](https://www.netlify.com/)
