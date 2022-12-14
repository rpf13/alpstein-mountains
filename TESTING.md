## Testing

This part covers all the testing sections in order to proof proper functionality.

---

### User Testing

I have tested the site on various devices and different browsers. Furthermore friends and family did check it out and no one reported an issue.

### User Stories Testing

- As a visiting user, I would like to be immediately attracted by a stunning big picture of the Alpstein Mountains

    ![Alpstein Mountains Main Site - Hero Image](docs/testing/01-navbar_hero.png)

- As a visiting user, I would like to gain informations about the Alpstein Mountains

    ![Facts & History](docs/testing/01-facts_history.png)

- As a visiting user, I would like to see a video, showing the beautiful area

    ![YouTube Drone Video](docs/testing/01-youtube.png)

- As a visiting user, I would like to enjoy a minimalistic web design, where the beautifulness of the mountains, shown via the pictures, speaks for itself
    - The Am I Responsive snapshot gives a good view on the sleek and minimalistic design, keeping the beautiful images as the main attraction.

    ![Sleek Design - Am I responsive snapshot](docs/testing/amiresponsive.png)

- As a visiting user, I would like to see a gallery of pictures to get an impression of the landscape

    ![Gallery Site](docs/testing/02-gallery.png)

- As a visiting user, I would like to get some information about recommended tours
    - Some generic info about the tours is given in the "Explore the Alpstein" section, but even more info can be gathered from the tour options and their links behind.

    ![Tours Section](docs/testing/03-awesome_tours.png)

- As a visiting user, I would like to have a contact form to get more informations

    ![Contact Form](docs/testing/03-contactform.png)

- As a visiting user, I would like to get a confirmation, that sending the contact form was successful

    ![Confirmation Site](docs/testing/04-confirmation.png)

- As a visiting user, I would like to see a map of the area, in order to understand, where these mountains are located

    ![Google Maps w. Alpstein Area](docs/testing/03-gmaps.png)

### Browser Testing

The project has been developed on a Mac with Firefox as main browser. Safari has been used for cross checking, while developing. I have tested the site on all possible browsers, also under Windows.

- Firefox

    ![Firefox Browser](docs/testing/firefox.png)

- Safari

    ![Safari Browser](docs/testing/safari.png)

- Chrome

    ![Chrome Browser](docs/testing/chrome.png)

- Edge

    ![Edge Browser](docs/testing/edge.png)

### Responsiveness Testing

Thoroughout the projec,t I did always verify responsiveness via the developer tools in the browser. However, as mentioned in the development section of the [README](README.md) file, the project was developed with a minimal screen size in a mobiel first approach. This has helped me to always be responsive, also when increasing the screen sizes.
However, here some snapshots taken on an iPhone 12 Pro:

- iPhone

    ![iPhone1](docs/testing/iphone1.png)

    ![iPhone2](docs/testing/iphone2.png)

    ![iPhone3](docs/testing/iphone3.png)

    ![iPhone4](docs/testing/iphone5.png)

    ![iPhone5](docs/testing/iphone6.png)

- iPad

    ![iPad](docs/testing/ipad.png)

- Desktop

    - Firefox

        ![Firefox Browser](docs/testing/firefox.png)

    - Safari

        ![Safari Browser](docs/testing/safari.png)

    - Chrome

        ![Chrome Browser](docs/testing/chrome.png)

    - Edge

        ![Edge Browser](docs/testing/edge.png)

---

## Bugs

### Known Bugs

While doing the CSS part and styling, I did use a regular expression in order to summary the hero image part, which is shared among all of the hero images. It worked fine, however, there seems to be a but, that the background-size attribute get's ignored. I could not make it to work, while I had this property in the regex, therefore I had to specify under each id selector.

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

### Fixed Bugs

- **Main Site:** After running the w3c html validator over the main site, I got 2 errors in the YouTube Video section. I did clean them up, removed the unnecessary frameborder attribute and swaped the section to a div element, since I did not plan to have any headings in that part.

    ![w3c validation main](docs/testing/w3c_validation_errors_main.png)

- **Gallery Site:** After running the w3c html validator over the gallery site, I got 1 error, since I've used a section element instead of a div element for the gallery. Since there are no headings planned, I did exchange the element type to div.

    ![w3c validation gallery](docs/testing/w3c_validation_errors_gallery.png)

- **Tours Site:** After running the w3c html validator over the tours site, I got 1 error, since I've used a section element instead of a div element for the maps part. Since there are no headings necessary, I did exchange the element type to div.

    ![w3c validation tours](docs/testing/w3c_validation_errors_tours.png)

- **Tours Site Contact Form:** During testing on Windows computer, I have figured out that the dropdown menu for the contact form was *empty* apart from the first "Make your Choice" entry. On Mac OS X, on which the site was developed, it was not the case. Further checks and research have shown, that OS X uses per default a grey background for the dropdown menu, where as on Windows it is white. Therefore I had to add a change into CSS for the text input option to turn black.

    ![dropdown menu windows issue](docs/testing/windows_dropdown_issue.png)

- **Confirmation Site:** After running the w3c html validator over the tours site, I got 1 error, I forgot the "url=" keyword in the meta tag for redirect back to the tours site.

    ![w3c validation confirmation](docs/testing/w3c_validation_errors_confirmation.png)

- **All Sites - Footer:** After running the [Wave Webaim Validator](https://wave.webaim.org/) I got a contrast error on my footer section, on the designation. After checking CSS I found out, that I had by mistake applied the smokey black background color (#222725) to the whole section, not only the part with the social media buttons. I did correct that in CSS.

    ![wave webaim footer](docs/testing/wave_error_footer.png)

---

## Validator Testing

This section covers the various testins, which were done via the official testing tools.

### HTML Validator

Test run via the official w3c html validator.

- [Main index](https://validator.w3.org/nu/?doc=https%3A%2F%2Frpf13.github.io%2Falpstein-mountains%2F) site did not show any issues, after fixing the [mentioned](#fixed-bugs) two points.

    ![w3c validation main](docs/testing/w3c_validation_main.png)

- [Gallery](https://validator.w3.org/nu/?doc=https%3A%2F%2Frpf13.github.io%2Falpstein-mountains%2Fgallery.html) site did not show any issues, after fixing the [mentioned](#fixed-bugs) issue.

    ![w3c validation gallery](docs/testing/w3c_validation_gallery.png)

- [Tours](https://validator.w3.org/nu/?doc=https%3A%2F%2Frpf13.github.io%2Falpstein-mountains%2Ftours.html) site did not show any issues, after fixing the [mentioned](#fixed-bugs) issue.

    ![w3c validation tours](docs/testing/w3c_validation_tours.png)

- [Confirmation](https://validator.w3.org/nu/?doc=https%3A%2F%2Frpf13.github.io%2Falpstein-mountains%2Fconfirmation.html) site did not show any issues, after fixing the [mentioned](#fixed-bugs) issue.

    ![w3c validation confirmation](docs/testing/w3c_validation_confirmation.png)


### CSS Validator

I did run the w3c css [jigsaw](https://jigsaw.w3.org/css-validator/) validator and no issues could be found.

![w3c css jigsaw validator](docs/testing/w3c_jigsaw_validation.png)

### Lighthouse Testing

I did verify the site in Lighthouse via Chrome browser:

![Lighthouse](docs/testing/lighthouse_main.png)

### Wave Webaim Validator

I did run the [Wave Webaim Validator](https://wave.webaim.org/) validator on all sites.

- **Main Site:** After fixing the [mentioned](#fixed-bugs) issue, no more errors were found.

    ![wave webaim main](docs/testing/wave_fix_footer.png)

- **Gallery Site:** No errors have been found.

    ![wave webaim gallery](docs/testing/wave_gallery.png)

- **Tours Site:** No errors have been found.

    ![wave webaim tours](docs/testing/wave_tours.png)

- **Confirmation Site:** No *real* errors have been found. However, since there is an automatic refresh of the site with a redirect back to the tours page, it shows an error. I took care about this warning with the fact, that I do explicitly tell the user, that a redirect will happen. This is done via the *oversized* text shown in front of the hero image.

    ![wave webaim confirmation1](docs/testing/wave_confirmation1.png) ![wave webaim confirmation2](docs/testing/wave_confirmation2.png)

---