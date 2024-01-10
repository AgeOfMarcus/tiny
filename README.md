# What is [tiny](https://tiny.marcusj.org)

Everything in a tiny site is contained **within the URL bar**.

None of the contents are sent to or stored on the server!

Instead, what you write is compressed and encoded. Tiny also supports markdown. Tiny can also be integrated in other projects to provide a "share HTML/Markdown as website link" service. Simply include the `lz-string.min.js` script on your website, and creating a link is as simple as:

```javascript
function createLink(title, body) {
    /* body can be text/markdown/html or a mix */
    const title_enc = encodeURI(title);
    const body_enc = LZString.compressToBase64(body);
    return `https://tiny.marcusj.tech/#${title_enc}/${body_enc}`;
}
```

## I can't explain well - just try it