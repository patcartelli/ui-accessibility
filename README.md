# ui-accessibility

[![license][license-image]][license-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][dependencyci-image]][dependencyci-url]

> notes on interface accessibility.

## Design Accessibility
### Checklist & Resources - 0.3.0

+ Color is not used as the sole method of conveying content or distinguishing visual elements.
+ Text meets AA (4.5:1) color contrast requirements.
  + [Check your Color Contrast!](http://jxnblk.com/colorable/demos/text/)
+ Provide Alternative Text (Alt Text) for meaningful graphical interface elements.
  + [Alt Text Basics](https://webaim.org/techniques/alttext/#basics)
  + [Accessibility: Image Alt text best practices](https://support.siteimprove.com/hc/en-gb/articles/115000013031-Accessibility-Image-Alt-text-best-practices)
+ Use labels or a call to action for controls (buttons, forms).
  + Design as much as possible with visible labels.
 + Do not rely on visuals or sound to indicate important instructions for operating content.
+ Annotate known design patterns. (Keyboard Interaction, Roles, States, Properties)
  + [Aria authoring](https://www.w3.org/TR/wai-aria-practices-1.1/#intro) includes notes on keyboard interaction, roles, states, properties for known patterns.
+ Confirm that you have multiple ways for users to interact with the interface.
  + Are keyboard, touch, and mouse supported?
  + There is a list of accordions. User can open an accordion with by touch, click, or keypress of enter. User can navigate to other tabs by pressing arrow up / down.
+ Annotate Screen Reader Interactions for [live content](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Live_Regions) such as expected data values, instructions, or required fields. Examples:
    + Assignment displays grade. Student answers a question and the grade updates. Grade element set to `aria-live="polite"`
    + User encounters a warning modal. Warning set to `aria-live="alert"`
+ Design Focus States to help users navigate and understand where they are on the page.
  + Is “Skip to Content” available and first in the tab order?
  + Tab order is identified and properly managed on the page and in modal windows.
  + Video: [a11ycasts Focus Ring!](https://www.youtube.com/watch?v=ilj2P5-5CjI)
+ Annotate with the [HTML semantic elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
  + Indicate headings (`h1`, `h2`, `h3`, etc.)
  + Buttons perform an action: ex. Save, Done, Apply, Preview
  + Links cause change of focus: ex Open a page in a new tab or take you to an anchor somewhere else on the page.
  + Annotate the semantic [Input Types.](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input) Examples: [Checkbox, email, password, button.](https://codepen.io/sh0ji/pen/VebrBM)
+ Indicate [Landmarks](https://www.w3.org/TR/wai-aria-1.1/#landmark):
  + [General Principles of Landmark Design](https://www.w3.org/TR/wai-aria-practices-1.1/#general-principles-of-landmark-design)
  + When possible, define landmarks with HTML sectioning: `aside`, `footer`, `header`, `main`, `nav`, `section`.
  + Otherwise use appropriate aria-role
  + Main landmark should have an `h1` (can be placed in banner)
  + Each navigation landmark should have an `h2` (can be offscreen)
    + If there are more than one navigation landmarks, use `aria-labelledby` to reference the `h2`
  + `footer` / `contentinfo` should have an `h2`: [Aria & HTML5 examples](https://www.w3.org/TR/wai-aria-practices/examples/landmarks/contentinfo.html)
  + Each `aside` / `complementary` landmark should have an `h2` (can be offscreen)
    + If there are more than one `complementary` landmarks, use `aria-labelledby` to reference the `h2`. [Example](https://www.w3.org/TR/wai-aria-practices/examples/landmarks/navigation.html)
  + Each region landmark should have an `h2` – `h6` (can be offscreen)
    + If there are more than one `region` landmarks, use `aria-labelledby` to reference the heading element

## 🎓 Information

### 📚 Reading & Documentation
Good reference for annotating specific components in your design.
+ Known Design Patterns [WAI-ARIA Authoring Practices 1.1](https://www.w3.org/TR/wai-aria-practices-1.1/#intro)
+ [Vox Accessibility Guidelines](http://accessibility.voxmedia.com/)
+ [Material Design Accessibility Implementation](https://material.io/guidelines/usability/accessibility.html#accessibility-implementation)
+ [Accessibility - Web Fundamentals - Google Developers](https://developers.google.com/web/fundamentals/accessibility/)
+ [WebAIM's WCAG 2.0 Checklist](https://webaim.org/standards/wcag/checklist)
+ [An Incomplete Guide to Inclusive Language for Startups and Tech](https://open.buffer.com/inclusive-language-tech/)

### 📹 Videos
+ [Intro to Aria](https://www.youtube.com/watch?v=g9Qff0b-lHk&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)
+ [Pragmatic Accessibility – Google I/O](https://events.google.com/io/schedule/?section=may-18&track=accessibility)

## 🛠 Tools
### 🎨 Color
+ [Material Design - Color Tool](https://material.io/color/#!/?view.left=0&view.right=0)
+ [Colorable](http://jxnblk.com/colorable/demos/text/?background=%23342324&foreground=%23EFFFA8)

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
