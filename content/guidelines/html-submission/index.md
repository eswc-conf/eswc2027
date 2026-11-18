---
title: "HTML Submission Guide"
---

ESWC 2027 welcomes research articles employing the Open Web Platform. This document provides guidance to authors who wish to make their contributions available in HTML and related technology stack.

## General Guidance

Contributions in HTML should be shared in EasyChair as a ZIP archive that contains the complete and self-contained content of the article. It should include a main “index.html” and all used resources (like media, scripts) to guarantee a correct visualization of the document on common desktop and mobile Web browsers. Please note the following key requirements:

- HTML template: any tooling or process can be used to produce the HTML.
- Content: the full content of the article must be human-readable with HTML alone. The use of CSS and JavaScript is encouraged, but should not interfere with the accessibility of the content.
- Offline-friendly: there must not be any external dependencies (e.g., a network connection) to retrieve, to render, or to manipulate the content of the article.
- Privacy: scripts must not be used to identify or track readers.
- View: the rendered article (HTML+CSS) should have the “look and feel” of the LNCS authoring guidelines. Pixel-perfection is not expected. This is to ensure visual consistency of the proceedings as well as to have comparative page limits with the print-based publication. The HTML article has to be compliant with the page limit constraint.

It should be possible to read the HTML contributions on an average desktop computer or mobile computer that is equipped with a reasonably current, Javascript-enabled Web browser (e.g., Firefox, Chrome/Chromium, Brave, Safari). We encourage authors to make their articles as accessible as possible (for reading and interacting) because different consumers (in this case initially the reviewers and chairs) may have different environments and abilities.

## Final (“camera-ready”) version

Formatting requirements for the *final version* differ by call.

- Articles accepted in the Research, In-Use, and Resources tracks will be published by Springer in the printed conference proceedings, as a part of the Lecture Notes in Computer Science (LNCS) series. Springer requires the sources of articles that have been accepted for publication in [LaTeX or Word format](https://www.springer.com/us/computer-science/lncs/conference-proceedings-guidelines). If an article submitted in HTML is accepted, the authors can choose to do this step manually or using tool support as outlined below.
- Articles accepted in the Posters & Demos track, in the PhD Symposium, and in the Industry track will be published by Springer in the supplementary (satellite) proceedings, also in the LNCS series. The same source requirements apply.

## Recommendations

We recommend that authors take the following steps independently of the general process:

Before sharing your article with ESWC, self-publish your HTML version, eg. at a repository, personal or institution website that's publicly accessible and archivable from a URL.

Include the URL of your self-published article along the lines of: “Identifier: [http://example.org/article](http://example.org/article)” after the list of authors and/or include the URL in the abstract of your article. Make sure to preserve this information in your camera-ready version.

Consider using a [Creative Commons](https://creativecommons.org/) license like [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) on the self-published version.

Create multiple archived copies of the self-published version using on-demand free archive services like [archive.org](https://web.archive.org/), [archive.is](https://archive.is/).

If you intend to also publish the “Author’s Accepted Manuscript” version following peer-review, note Springer’s [self-archiving policy](https://www.springer.com/gb/open-access/authors-rights/self-archiving-policy/2124).

Send a notification about your original self-published article to the [Linked Open Research Cloud](https://linkedresearch.org/) (LORC) to improve the discoverability of your article.

For additional help, authors are welcome to [join the public chat](https://gitter.im/linkedresearch/chat) on [Linked Research](https://linkedresearch.org/). Please note that this is not an official communication channel of the conference. It is an open community for scholarly communication and people passionate about the Web.

Authors are encouraged to use tooling and processes that work best for them.

### dokieli

[dokieli](https://dokie.li/) is a client-side editor for decentralized article publishing in HTML+RDF annotations, notifications, and social interactions. It implements W3C Recommendations like the [Web Annotation model](https://www.w3.org/TR/annotation-model/), [Linked Data Notifications](https://www.w3.org/TR/ldn/), and [ActivityPub](https://www.w3.org/TR/activitypub/).

The [LNCS author guidelines](https://dokie.li/lncs-splnproc) can be used as template. There is a list of [examples in the wild](https://github.com/linkeddata/dokieli/wiki#examples-in-the-wild).

Authors that would like to self-publish can use any HTTP server. Authors, reviewers, and readers can use their own [WebID](https://www.w3.org/2005/Incubator/webid/spec/) and Linked Data based personal storages, eg. [Solid](https://github.com/solid/node-solid-server/), with dokieli. [Join the chat](https://gitter.im/linkeddata/dokieli) if you need help.

### RASH

The [Research Articles in Simplified HTML (RASH) format](https://github.com/essepuntato/rash) allows one to easily prepare a scientific paper in HTML format (example: [online](https://sparontologies.github.io/article/spar-iswc2018/)). It is composed by a few of the available HTML tags and allows one to [add RDF annotations](https://github.com/essepuntato/rash/blob/master/documentation/index.html#rdfa) by means of Turtle, JSON-LD, RDF/XML, and RDFa.

Although one could directly write the HTML/RASH syntax ([see documentation](https://github.com/essepuntato/rash/blob/master/documentation/index.html)), one can create an Open Office Writer (ODT) or Microsoft Word (DOCX) document, and then convert it to HTML/RASH using the ROCS conversion tool. In summary:

- Prepare your article in Open Office Writer (ODT) or Microsoft Word (DOCX), following the simple RASH guidelines for [ODT](https://github.com/essepuntato/rash/blob/master/documentation/rash-in-odt-simplified.odt) and [DOCX](https://github.com/essepuntato/rash/blob/master/documentation/rash-in-docx-simplified.docx).
- Use [ROCS](https://github.com/essepuntato/rash/tree/master/tools/rocs) to convert your ODT or DOCX document to RASH. This tool will produce a ZIP file with the RASH conversion of your paper (it also includes an LNCS-conforming LaTeX version of the article). This ZIP file can be directly submitted to EasyChair.
- Optionally, if you want to extend the metadata of the paper, [add RDF annotations](https://github.com/essepuntato/rash/blob/master/documentation/index.html#rdfa) to the HTML code.

If you choose to write HTML/RASH manually (which makes sense when collaborating with your co-authors in a source code repository), note that the above-mentioned [ROCS](https://github.com/essepuntato/rash/tree/master/tools/rocs) can actually convert *any* RASH markup to LaTeX.

### ScholarMarkdown

[ScholarMarkdown](https://github.com/rubensworks/ScholarMarkdown) is a framework for writing articles in the lightweight Markdown syntax, with automatic translation into HTML+RDFa, and the option to output [PDF](https://github.com/rubensworks/ScholarMarkdown/wiki/PDF-Compilation). It provides syntactic sugar to easily perform common tasks such as [citing articles](https://github.com/rubensworks/ScholarMarkdown/wiki/Snippets#citations), writing [math equations](https://github.com/rubensworks/ScholarMarkdown/wiki/Snippets#math-equations), and [more](https://github.com/rubensworks/ScholarMarkdown/wiki/Snippets).

Note: ScholarMarkdown requires [Ruby](https://www.ruby-lang.org/en/documentation/installation/) to be installed.

The Markdown-based source files enables straightforward versioning and collaborative editing with version-control systems such as git, and integrates nicely with automated [self-publishing via solutions such as GitHub pages](https://github.com/rubensworks/ScholarMarkdown/wiki/Self-publishing), as demonstrated by the [examples in the wild](https://github.com/rubensworks/ScholarMarkdown/wiki/Examples).

To get started, follow the [quick start guide](https://github.com/rubensworks/ScholarMarkdown#quick-start), which will provide you with the required LNCS template in Markdown. After [compiling your Markdown files to HTML](https://github.com/rubensworks/ScholarMarkdown#3-compile-your-article), an `output/` directory will be created. This `output/` folder contains a standalone version of your article in HTML, and this is the folder that must be submitted on EasyChair. Further details on ScholarMarkdown can be found on the [wiki](https://github.com/rubensworks/ScholarMarkdown/wiki).

## Acknowledgements

*This page is adapted from the [ISWC 2026 HTML Submission Guide](https://iswc2026.semanticweb.org/#/guidelines/html-submission), building on the [ESWC 2025 HTML Submission Guide](https://2025.eswc-conferences.org/html-submission-guide/). We would like to thank [Sarven Capadisli](http://csarven.ca/#i) for his valuable contributions to these guidelines.*
