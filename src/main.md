---
marp: true
---
<!-- theme: gaia
backgroundColor: #ffffff
backgroundImage: url(https://user-images.githubusercontent.com/49607727/162590298-a59bf401-052f-407a-b2e9-0f561bf12e72.jpg)
paginate: true
_paginate: false # don't paginate the first slide
_class: lead
 -->

![bg left:30% 70%](img/markdown-logo.svg)

# **Markdown**

## Lightweight markup language

Tomasz Wojdat

September 2021

---

# Motivation

* It's hard to organize knowledge in a structured, well-organized, and
  portable way that promotes easy access, sharing, and collaboration.

* Plaintext vs. binary files for storing information.

* Simple doesn't mean less powerful.

* (Sort of) Unix philosophy in knowledge management.

---

# Solution?

* Limit using __closed__, __proprietary__ __binary__ or __web-based__
  formats for storing information if you will need it in the future.

* Prefer using __open__, __lightweight__, and __popular__ __plaintext__
  formats.

* If collaborating with others, __use version control__.

* Popular and open formats have big communities that create a lot of
  useful tools around these formats.

* This can be achieved with the help of a __markup language__.

---

# What is a markup?

* Text added to the data of a document to convey information about the
  document.

* Used to structure, index, and determine the desired look of text
  content.

* The term comes from the printing industry: the editor annotated text
  with colored annotations. The process was known as _marking up_ the
  document, and the annotations were referred to as _markup_.

* Some of us might have even invented our own _note-taking markup_.

---

![bg 90%](
https://user-images.githubusercontent.com/49607727/162590206-775ddc9e-9fa5-4ec2-8785-34fe68043e9e.jpg
)

![bg 65%](
https://user-images.githubusercontent.com/49607727/162590217-960e03ed-821d-4c7e-ac41-02726a3e4bf9.jpg
)

---

# What is a markup language?

* A text-formatting language designed to transform raw text into
  structured documents.

* The data describes either:

  * __Presentation__ of the text in a __procedural__ manner\
    (e.g. `<b>some text</b>`) or

  * __Structure__ of the text in a __descriptive__ manner\
    (e.g. `<blockquote>some text</blockquote>`).

---

# How does markup language work?

* The data describing the text is hidden at the moment of presentation
  and impacts the outlook of the output.

* E.g. <b>bold text</b> becomes __bold text__ in your web browser.

---

# Separation of content and presentation

* _Some_ markup languages try to separate the document content from its
  presentation.

* It's desired in the knowledge management because we can split the
  process of formulating our thoughts from tweaking the final outlook of
  the document.

* It promotes portability, as we can present the same information in
  different ways _(almost)_ without modifying the content.

---

![bg 40%](
https://user-images.githubusercontent.com/49607727/162590224-411e6741-8b31-4e51-ad72-7ae7e73bb6e9.jpg
)

---

![bg fit](
https://user-images.githubusercontent.com/49607727/162590230-69b9d854-ce5e-43e2-85b1-b7a9eec13562.jpg
)

---

# Types of markup

* We can distinguish two types of markup:

  * Procedural (logical, structural)
  * Descriptive (physical, presentational)

* Most modern markup languages use both of these types.

---

# Procedural markup

* Text + procedural instructions how to process it.

* E.g. some HTML tags like `<b>`, troff (used by Linux man-pages) or
  TeX.

  ```tex
  \begin{center}
  \huge{Document title}
  \large{Detailed document description with more details and example use cases}
  \end{center}[2]
  ```

---

# Descriptive markup

* Text with labels describing what _are_ the parts of the document,
  rather than _how_ they should be processed.

* E.g. most HTML tags like `<strong>` or `<h1>`, $\LaTeX$ (TeX with
  descriptive macros).

  ```xml
  <title>Document title</title>
  <desc>Detailed document description with more details and example use cases</desc>
  ```

---

# Reality

* In modern word-processing systems, presentational markup is often
  saved in descriptive-markup-oriented systems such as XML, and then
  processed procedurally by implementations.

---

# Markdown

* Markdown is a lightweight markup language that focuses on portability
  and legibility of its source code form. It uses minimal syntax, and
  it's very easy to edit it with any text editor of choice.

* It's commonly used for writing _READMEs_ and _documentation_.

---

# Markdown vs. others

* Markdown isn't the only lightweight markup language. In fact, it's one
  of many. However, it's by far the most popular one. It should be the
  best choice for _most_ of use cases.

---
<!-- _footer: https://en.wikipedia.org/wiki/Lightweight_markup_language
 -->

![bg 95%](
https://user-images.githubusercontent.com/49607727/162590246-012e29cd-923e-4b6a-aac0-e82fb5ed809d.png
)

---

# Basic Markdown syntax

```markdown
# This is an <h1>
## This is an <h2>
### This is an <h3>
```

# This is an <h1>
## This is an <h2>
### This is an <h3>

---

```markdown
*This text is in italics.*
_And so is this text._

**This text is in bold.**
__And so is this text.__

***This text is in both.***
~~And this text is rendered with strikethrough.~~
```

*This text is in italics.* _And so is this text._

**This text is in bold.** __And so is this text.__

***This text is in both.*** ~~And this text is rendered with
strikethrough.~~

---

```markdown
This is a paragraph. I'm typing in a paragraph, isn't this fun?

<!-- This is a comment. It won't be rendered. -->

Now I'm in paragraph 2.
I'm still in paragraph 2 too! But I can use _backslash_ to break a line.\
Hi there! I'm on a new line.
```

This is a paragraph. I'm typing in a paragraph, isn't this fun?

<!-- This is a comment. It won't be rendered. -->

Now I'm in paragraph 2. I'm still in paragraph 2 too! But I can use
_backslash_ to break a line.\
Hi there! I'm on a new line.

---

Unordered lists are easy:

```markdown
* Item 1
* Item 2
* Item 3
```

Instead of `*`, you can also use `-` or `+`.

* Item 1
* Item 2

---

Ordered lists are cool, too:

```markdown
1. First item
2. Second item

Markdown will count for us, so this works the same (but don't do it, please):

1. First item
1. Second item
```

1. First item
2. Second item

---

We can make it a bit more complicated:

```markdown
1. Item one
2. Item two
    * Sub-item
      * Sub-item
3. Item three
```

1. Item one
2. Item two
    * Sub-item
      * Sub-item
3. Item three

---

```markdown
Use \` to write inline code. `Like this`.

With three of these you can do multiline block and specify a language:

```python
def hello(name: str) -> str: return f"Hello, {name}"
'``
```

Use \` to write inline code. `Like this`.

With three of these you can do multiline block and specify a language:

```python
def hello(name: str) -> str:
    return f"Hello, {name}"
```

---

```markdown
<!-- Links are straightforward -->
[Click me!](http://example.com/)

[Relative link](img/markdown-logo.svg)

<!-- Use exclamation mark for linking images -->
![This is alt text](img/markdown-logo.svg "Pretty neat, huh")
```

[Click me!](http://example.com/)

[Relative link](img/markdown-logo.svg)

<!-- Use exclamation mark for linking images -->
![This is alt text](img/markdown-logo.svg "Pretty neat, huh")

---

# Markdown tools

The power of Markdown lies in the tools that support it. It's very easy
to use Markdown to build a __webpage__, create a __presentation__, or
generate a __PDF__ document from it. Popular repository hosting sites
like _GitHub_ or _Bitbucket_ support rendering of Markdown documents.

---

# Pandoc

* Free and open-source state-of-the-art command-line document converter
  written in Haskell.

* Pandoc can convert between numerous markup and word processing
  formats, including, but not limited to, various flavors of
  __Markdown__, __HTML__, __LaTeX__ and Word __docx__. Pandoc can also
  produce __PDF__ output.

* Pandoc’s enhanced version of Markdown includes syntax for tables,
  definition lists, metadata blocks, footnotes, citations, math and
  more.

---

# GitHub

* GitHub is one of the main reasons of the current Markdown popularity.
  It supports it's own flavor of Markdown and you can use it as a
  convenient viewer for _.md_ files that are a part of any git
  repository.

* Some [use
  it](https://github.com/antlr/antlr4/blob/master/doc/index.md) for easy
  hosting of docs without the need of any external provider.

* Others [keep](https://github.com/rwxrob/zet/) personal notes in it, as
  GitHub makes it very easy to search through them.

---

# Jekyll

<https://jekyllrb.com/>

Static site generator written in Ruby that powers GitHub Pages.

# Hugo

<https://gohugo.io/>

Static site generator written in Go. More powerful and faster than
Jekyll, but with a higher learning curve. [Let's
Encrypt](https://letsencrypt.org/) webpage is based on Hugo.

---

# MkDocs

<https://www.mkdocs.org/>

MkDocs is a fast and simple static site generator that's geared towards
building project documentation. Documentation source files are written
in Markdown, and configured with a single YAML configuration file.

---

# HackMD

<https://hackmd.io/>

* Real-time collaboration in Markdown (similar to Google Docs). It can
  be used as an online hosting of Markdown documents when we don't want
  to store sensitive information.

* The notes can be synced with GitHub to keep them up-to-date and
  backed-up. They can be shared publicly, to a given group of people, or
  accessible only for the owner.

---

# HedgeDoc

<https://hedgedoc.org/>

* Open-source fork of HackMD that supports self-hosting.

* The true history is a bit more complicated: HedgeDoc is the
  community-driven fork of CodiMD, which is the open source counterpart
  to HackMD. More on that [here](https://hedgedoc.org/history/).

---

# Marp

<https://marp.app/>

* Markdown presentation ecosystem that enables creating PDF or HTML
  presentations from pure Markdown with some custom syntax.

* This very presentation was created using it.

---

# Mermaid: diagrams and visualizations

<https://mermaid-js.github.io/mermaid/#/>

![height:400](
https://user-images.githubusercontent.com/49607727/162590278-d81907c4-5026-48d1-8222-feef1032ba1a.png
)

---

# Markmap: mindmap from Markdown

<https://markmap.js.org/>

![width:1000px](
https://user-images.githubusercontent.com/49607727/162590288-2078ccb5-3fd1-43c8-8e07-c18c4bdd05c5.png
)

---
<!-- _header: _Access 2021-09-17_
 -->

# Further reading and useful links

1. [CommonMark Markdown syntax](https://commonmark.org/help/)

2. [Learn Markdown in Y
   minutes](https://learnxinyminutes.com/docs/markdown/)

3. [Markdown Google style
   guide](https://google.github.io/styleguide/docguide/style.html)

4. [Diagrams with Markdown: tools
   overview](https://gist.github.com/blackcater/1701e845a963216541591106c1bb9d3b)

5. [Markdown linter for VS
   Code](https://github.com/DavidAnson/vscode-markdownlint)

---
<!-- _class: lead
_paginate: false
-->

# __Thank you!__
