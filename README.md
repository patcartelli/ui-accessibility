# ui-accessibility

[![license][license-image]][license-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][dependencyci-image]][dependencyci-url]

> notes on interface accessibility.

## Design Accessibility Guidelines

### Design
+ Color is not used as the sole method of conveying meaning or distinguishing visual elements.
+ Do not rely on visuals or sound to indicate important instructions for operating content.
    + Incorrect: Only uses sound to indicate success or only uses color to indicate success.
    + Correct: Uses both a sound or color as well as a label to indicate success.
+ Text meets AA (4.5:1) color contrast requirements.
  + [Check your Color Contrast!](http://jxnblk.com/colorable/demos/text/)
+ Every call to action (such as buttons, form elements, etc.) must be meaningfully named.
    + Design as much as possible with visible labels.
    + If you must include a meaningful graphical interface element without a label, alt text is required to describe the function of this element.
+ Alternative text (alt text) is provided for meaningful content images and graphical interface elements.
  + Meaningful graphical interface elements can be things that aren't actually images, such as font icons, image-like unicode (e.g. emoji), or stylized CSS.
  + Alt text for meaningful content images should be provided by Editorial.
  + Decorative images do not need alt text.
  + [Alt Text Basics](https://webaim.org/techniques/alttext/#basics)
  + [Accessibility: Image Alt text best practices](https://support.siteimprove.com/hc/en-gb/articles/115000013031-Accessibility-Image-Alt-text-best-practices)

### Annotations
+ **Documentation Reference** - Reference the [ARIA Authoring Practices](https://www.w3.org/TR/wai-aria-practices-1.1/#intro) for known design patterns. These guidelines includes descriptive annotations for keyboard interaction, roles, and states.
  + Confirm that keyboard, touch, and mouse are supported to provide users multiple ways to interact with the interface.
  + E.g. In a list of accordions, the user can open an accordion with by touch, click, or keypress of enter. User can navigate to other accordions by pressing arrow up / down.
+ **Aria-live**- Annotate screen reader interactions for live content such as expected data values, instructions, or required fields. Examples available here: [MDN - ARIA Live Regions](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Live_Regions)
+ **Focus Indication** - Design Focus States to help users navigate and understand where they are.
  + Is "Skip to Content" available and first in the tab order?
  + Tab order is identified and properly managed on the page and in modal windows.
  + Video: [a11ycasts Focus Ring!](https://www.youtube.com/watch?v=ilj2P5-5CjI)
+ Annotate using the appropriate [HTML semantic elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
  + Indicate headings (`h1`, `h2`, `h3`, etc.)
    + E.g. "Document title H1"
  + Annotate the semantic [Input Types.](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input) Examples: [Checkbox, email, password, button.](https://codepen.io/sh0ji/pen/VebrBM)
  * Buttons perform an action such as "Save" or “Apply.”
  * Links cause change of focus: Opens a page in a new tab or takes you to an anchor elsewhere on the page.
+ Indicate [Landmarks](https://www.w3.org/TR/wai-aria-1.1/#landmark) — [General Principles of Landmark Design](https://www.w3.org/TR/wai-aria-practices-1.1/#general-principles-of-landmark-design)
  + Always define the [main](https://www.w3.org/TR/wai-aria-practices-1.1/#aria_lh_main) content container if it exists.
  + Define [other landmark regions](https://www.w3.org/TR/wai-aria-practices-1.1/#landmark-roles) in your wireframes wherever possible.
      + Main landmark should have an h1 (can be placed in banner)
      + navigation landmarks should have an h2 (can be offscreen)
      + footer should have an h2 (can be offscreen)
      + Each aside landmark should have an h2 (can be offscreen)
      + Each region landmark should have an h2 – h6 (can be offscreen)

## 🎓 Information

### 📚 Reading & Documentation
Good reference for annotating specific components in your design.
+ Known Design Patterns: [WAI-ARIA Authoring Practices 1.1](https://www.w3.org/TR/wai-aria-practices-1.1/#intro)
+ [Vox Accessibility Guidelines](http://accessibility.voxmedia.com/)
+ [Material Design Accessibility Implementation](https://material.io/guidelines/usability/accessibility.html#accessibility-implementation)
+ [Accessibility - Web Fundamentals - Google Developers](https://developers.google.com/web/fundamentals/accessibility/)
+ [WebAIM's WCAG 2.0 Checklist](https://webaim.org/standards/wcag/checklist)
+ [An Incomplete Guide to Inclusive Language for Startups and Tech](https://open.buffer.com/inclusive-language-tech/)
+ [http://a11y-style-guide.com/style-guide/](http://a11y-style-guide.com/style-guide/)
+ [https://developers.google.com/web/fundamentals/accessibility/focus/using-tabindex](https://developers.google.com/web/fundamentals/accessibility/focus/using-tabindex)
https://material.io/guidelines/usability/accessibility.html#accessibility-principles
+ [https://styleguide.mailchimp.com/voice-and-tone/](https://styleguide.mailchimp.com/voice-and-tone/)

### 📹 Videos
+ [Intro to Aria](https://www.youtube.com/watch?v=g9Qff0b-lHk&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)
+ [Pragmatic Accessibility – Google I/O](https://events.google.com/io/schedule/?section=may-18&track=accessibility)

## 🛠 Tools
### 🎨 Color
+ [Colorable](http://jxnblk.com/colorable/demos/text/?background=%23342324&foreground=%23EFFFA8)
+ [Material Design - Color Tool](https://material.io/color/#!/?view.left=0&view.right=0)

### 🖥 Extensions
+ [Chrome Lens](https://chrome.google.com/webstore/detail/chromelens/idikgljglpfilbhaboonnpnnincjhjkd?hl=en)
+ [Funkify](http://www.funkify.org/)
+ [Tota11y](https://chrome.google.com/webstore/detail/tota11y-plugin-from-khan/oedofneiplgibimfkccchnimiadcmhpe?hl=en)
+ [Wave Chrome Tools](https://chrome.google.com/webstore/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh?hl=en-US)


### 🤓 Command Line
+ [aXe cli](https://github.com/dequelabs/axe-cli) Command Line accessibility check

[license-image]: https://img.shields.io/badge/license-ISC-blue.svg
[license-url]: https://github.com/patcartelli/ui-accessibility/blob/master/LICENSE
[travis-image]: https://travis-ci.org/patcartelli/ui-accessibility.svg?branch=master
[travis-url]: https://travis-ci.org/patcartelli/ui-accessibility
[dependencyci-image]: https://dependencyci.com/github/patcartelli/ui-accessibility/badge
[dependencyci-url]: https://dependencyci.com/github/patcartelli/ui-accessibility
