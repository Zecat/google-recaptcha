# \<google-recaptcha\>

A Polymer element for google recaptcha V2 and invisible.

## Install
```
  bower install -S polymer-google-recaptcha
```

## Examples
```html
  <google-recaptcha
    sitekey="YOUR_KEY"
    value="{{token}}"
  ></google-recaptcha>

  <google-recaptcha
    sitekey="YOUR_KEY"
    theme="dark"
    type="video"
    size="compact"
    on-google-recaptcha-response="_handleRecaptchaResponse"
  ></google-recaptcha>

  <!-- Call the method `execute` on this element when you want a token -->
  <google-recaptcha
    sitekey="YOUR_KEY"
    invisible
    badge="inline"
  ></google-recaptcha>

  <!-- Using prevent-auto-render, call the method `render` when you want to
  display the recaptcha, then call `execute` to get a token -->
  <google-recaptcha
    sitekey="YOUR_KEY"
    invisible
    prevent-auto-render
  ></google-recaptcha>
```
