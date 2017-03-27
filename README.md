# CSS Element Queries

A spec for a container-style element query syntax in CSS

**Read online:** [element-queries.html](https://tomhodgins.github.io/element-queries-spec/element-queries.html)

## What is this about?

This spec aims to define a syntax for scoped styles and element queries in a container query style, as well as the related selectors, functions, and units that make scoped styles and element queries versatile and powerful way to write layout-independent responsive conditions for elements in CSS.

## Proposed Syntax

```css
/* Scoped Style */
@element div {
  $this {
    background: lime;
  }
}

/* Element Query */
@element div and (min-width: 500px) {
  $this {
    background: lime;
  }
}

/* Container Query */
@element div and (min-width: 500px) {
  $this {
    background: lime;
  }
  html {
    background: red;
  }
}

/* Multiple Selectors */
@element #example-1, #example-2 {
  $this {
    background: lime;
  }
}

/* Multiple Conditions */
@element div and (min-width: 500px) and (min-characters: 5) {
  $this {
    background: lime;
  }
}
```

**View Syntax Example:** [styles.css](example/styles.css)

## Plugin & Demo

As a reference for the syntax described in the spec, I have included a JavaScript plugin that reads the proposed syntax and displays the desired behaviour of the proposed functionality.

**View Plugin:** [element-queries.js](plugin/element-queries.js)

**View Demo:** [demo.html](demo.html)

## Related Projects

There are a few projects currently working with the syntax described in this spec:

- [EQCSS](https://github.com/eqcss/eqcss) Element Query CSS browser plugin
- [eqcss-compiler](https://github.com/tomhodgins/eqcss-compiler) an EQCSS to JavaScript compiler

## Further Examples

More examples of this syntax can be found on Codepen by searching for "EQCSS".

**Search Codepen for EQCSS:** [Codepen Search](http://codepen.io/search/pens?q=eqcss&limit=all&type=type-pens)

## Who am I?

I'm an independent web developer, not affiliated with any major companies. The research & development contained in this spec is my own.

## How you can help

At this stage the work on this spec is focused on taking the existing EQCSS syntax for element queries as implemented by the EQCSS project and defining them in a more formal way so that other plugin builders could design plugins or tools that work with the EQCSS syntax as implemented by EQCSS.js

In the future once the first version of this document is complete, there will be an opportunity to extend the features described.

For now, the most productive way to provide input would be by contributing to the conversation in the [Gitter chat room for the EQCSS project](https://gitter.im/eqcss/eqcss)


## Further Reading

- [How Style Scoping Works with Element Queries](http://codepen.io/tomhodgins/post/how-style-scoping-works-with-element-queries)
- [What the Heck are Element Queries & Container Queries?](http://codepen.io/tomhodgins/post/what-the-heck-are-element-queries-container-queries)
- [Writing Element Queries Today Using EQCSS](https://www.sitepoint.com/eqcss-a-javascript-plugin-to-write-element-queries/)
- [The Search For The Holy Grail: How I Ended Up With Element Queries, And How You Can Use Them Today](https://www.smashingmagazine.com/2016/07/how-i-ended-up-with-element-queries-and-how-you-can-use-them-today/)
