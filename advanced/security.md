---
layout: default
title: Security
title_nav: Security
description_short: A statement on security.
description: A statement on security.
keywords: security xss scripting vulnerability hack hacker
---

## Q: Is TinyMCE protected against XSS vulnerabilities?

{{site.productname}} filters out some of the more common XSS content like scripts from the content since it is common that the editor is used in a single page application. For additional security, consider passing it through server-side filters like [HTMLPurifier](http://htmlpurifier.org/).

## Q: How do I setup Content Security Policy (CSP) with TinyMCE?

{{site.productname}} can be used with a [CSP](https://content-security-policy.com/) header. When using a CSP, the following directives are **required** for {{site.productname}} to function:

| Directives | Requirements |
|------------|--------------|
| script-src 'self' *.tinymce.com *.tiny.cloud;          | Scripts are sometimes loaded as script element with an src attribute.
| connect-src 'self' *.tinymce.com *.tiny.cloud blob:;         | XMLHttpRequest are required by some services such as spellchecking and PowerPaste.
| img-src 'self' *.tinymce.com *.tiny.cloud data: blob:; | Images within the editor are sometimes base64 encoded, blob URLs, or proxied through the {{site.cloudname}} service.
| style-src 'self' 'unsafe-inline' *.tinymce.com *.tiny.cloud;        | Styles are used for inline formatting (such as underline, font colors, etc.) and the positioning of user interface elements.
| font-src 'self' *.tinymce.com *.tiny.cloud;            | Fonts are used for icons in the UI and is loaded from external files.

> **Important**: These directives will prevent all content loading from external sources.
> To allow content from specific sources, add the source domains to the relevant directives. For example, to allow YouTube videos:
>  ```html
>  media-src 'self' *.youtube.com;
>  ```
>  To allow content from any source, use the (&#42;) wildcard. Allowing all sources (using &#42;) negates the security policy for the source type. For example:
>  ```html
>  media-src *;
>  ```
> For information on Content Security Policies, see: [MDN Web Docs - Content Security Policy (CSP)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP).

When using the {{site.cloudname}}, use this CSP header :

```html
<meta http-equiv="Content-Security-Policy" content="default-src 'none'; script-src 'self' *.tinymce.com *.tiny.cloud; connect-src 'self' *.tinymce.com *.tiny.cloud blob:; img-src 'self' *.tinymce.com *.tiny.cloud data: blob:; style-src 'self' 'unsafe-inline' *.tinymce.com *.tiny.cloud; font-src 'self' *.tinymce.com *.tiny.cloud;" />
```

When self-hosting {{site.productname}} from a local domain, use this CSP header (excludes the &#42;.tiny.cloud domain):

```html
<meta http-equiv="Content-Security-Policy" content="default-src 'none'; script-src 'self'; connect-src 'self' blob:; img-src 'self' data: blob:; style-src 'self' 'unsafe-inline'; font-src 'self';" />
```
