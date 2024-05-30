# Intro Media Queries

<details>
<summary>Table of content</summary>

- [What is media queries?](#what-is-media-queries)
- [Standard Breakpoints](#standard-breakpoints)
</details>

### What is media queries?

Media queries in CSS are a way to apply styles to a web page based on the size of the given screen. We can have rather large screen, and we can also have a very small one, like a mobile phone. This is very useful for creating responsive web page designs that adapt to different screen and devices.

How to we do this then? Of course by using media queries.

Here is a basic example:

```css
@media screen and (max-width: 600px) {
  /* Styles for screens with a maxiumum width of 600px */

  nav {
    background-color: red;
  }
}

@media screen and (max-width: 400px) {
  /* Styles for screens with a maxiumum width of 400px */

  nav {
    background-color: blue;
  }
}
```

- `@media`: this is the keyword that indicates the beginning of the media query.
- `screen`: specifes that the styles withing the media query should only apply to devices with screens. _( not devices that might not have a screen, like printers )_
- `(max-width: 600px)`: this is the condition that must be true in order for the styles within the media query to be applied. In this case, the styles will only apply if the screen width is 600px or less.

There are many more ways yo can specify your condition, but in the majority of cases we use either `max-width` or something that is the opposite, called `min-width`.

Which one of these condition should you use? It depens on which approach you have, mobile or desktop first. (Explained further down in this text). But generally, if you choose to `desktop-first` approach, you should opt for the `max-width` condition. If you choose `mobile-first` you should go for the `min-width` condition.

- Desktop First => use `max-width`
- Mobile First => use `min-width`

When using the approach of Mobile-first, the default styling should always be applied to the smaller screens, and vice versa for Desktop-first. Then the default styles should be applied to large screens.

For further reading, see this link: [Media queries on W3Schools](https://www.w3schools.com/css/css_rwd_mediaqueries.asp).

[Back to top](#intro-media-queries)

### Standard Breakpoints

The size on the media query above is an arbitrary value that I just picked, but this is of course up to the developer to choose. There exist, sort of, a set of standard values in the IT business. I say sort of, because there are many variants depending on work place, technique, css framework and so on. But these different sets of standard values are roughly the same. The following, according to the responsive developing tools in `Chrome` is a good standard to follow:

- **4K**: screens larger than 2560px
- **Laptop L**: larger than 1440px
- **Laptop**: larger than 1024px
- **Tablet**: larger than 768px
- **Mobile L**: larger than 425px
- **Mobile M**: larger 375px
- **Moible S**: larger than 320px

[Back to top](#intro-media-queries)
