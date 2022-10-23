## Testing

This part covers all the testing sections in order to proof proper functionality.

### User Testing

I have tested the site on various devices and different browsers. Furthermore friends and family did check it out and no one reported an issue.

### User Stories Testing



### Known Bugs

While doing the CSS part and styling, I did use a regular expression in order to summary the hero image part, which is shared among all of the hero images. It worked fine, however, there seems to be a gut that the baground-size attribute get's ignored. I could not make it to run, once I had this property in the regex, I had to specify under each id selector.

```css
[id^=hero-image-]{
    height: 100%;
    background-size: cover;
    animation-name: hero-image-zoom;
    animation-duration: 5s;
    animation-fill-mode: forwards;
}

/* background size property did not work inside above's regex, therefore individually set like: */

#hero-image-main {
    background: url('../images/p10_aescher.webp') no-repeat center right;
    background-size: cover;
}
```


### Validator Testing

#### W3C Validator


#### W3C Jigsaw Validator


#### Lighthouse Testing