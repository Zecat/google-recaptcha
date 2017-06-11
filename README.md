[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/Zecat/google-recaptcha)

# \<google-recaptcha\>

A Polymer element for google recaptcha V2 and invisible.

<!--
```
<custom-element-demo>
<template>
<link rel="import" href="google-recaptcha.html">
<link rel="import" href="../promise-polyfill/promise-polyfill-lite.html">
<next-code-block></next-code-block>
</template>
</custom-element-demo>
```
-->
```html
<dom-bind>
  <template is="dom-bind">
    <google-recaptcha
      force-in-body
      value="{{token}}"
      sitekey="6LdHISEUAAAAAN0FxtC5OBGQv-zrtj1tQ1Z_KUWf"
    ></google-recaptcha>
    <span>[[token]]</span>
  </template>
</dom-bind>
```

## Install
```
  bower install -S Zecat/google-recaptcha
```

## Notes

- Promise polyfill is a dev dependency.
- Visit [https://www.google.com/recaptcha/admin](https://www.google.com/recaptcha/admin) to get a sitekey.

## Shadow DOM work-around

By-design, the google recaptcha doesn't work inside shadow dom, so we detect
when it has a ShadowRoot parent and if so, the recaptcha is placed in a
container light DOM, which sync its size and screen position with its original
\<google-recaptcha\> parent, and the container is moved into the body.
The container is refit every time the user scroll or the \<google-recaptcha\> is
notified of resize. This is an expensive task but the only solution so far.
