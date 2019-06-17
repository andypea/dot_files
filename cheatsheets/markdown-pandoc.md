---
title: 'Markdown (Pandoc Style) Cheatsheet'
author:
- Andrew Jon Punnett
- Adam Nathan Other 
keywords: [nothing, nothingness]
abstract: |
  This is the abstract.
  It consists of two paragraphs.
toc: yes
numbersections: yes
bibliography: ./data/bibliography.bib
link-citations: true
csl: ./data/harvard-cite-them-right.csl 
---

``` {.bash}
pandoc --standalone --filter=pandoc-citeproc --output markdown.md.pdf markdown.md
```

## Paragraphs {#section-paragraphs}

Single line-breaks are treated as a space, 
so this text will appear on the same line.

The blank line denotes the start of a new paragraph.

Here is some formatted text: 
a **bold** word, 
an *italic* word,
some ~~strike through~~,
some ~subscript~ and ^superscript^,
and `some verbatim text`.

## Verbatim (code) Blocks

``` {#code-qsort .haskell .numberLines startFrom="100"}
qsort [] = []
qsort (x:xs) = qsort (filter (< x) xs) ++ [x] ++
qsort (filter (>= x) xs)
```

## Line Blocks

These preserve formatting

| The limerick packs laughs anatomical
| In space that is quite economical.
|    But the good ones I've seen
|    So seldom are clean
| And the clean ones so seldom are comical

## Lists

### Unordered

  * fruits
    + apples
        - macintosh
        - red delicious
    + pears
    + peaches
  * vegetables
    + broccoli
    + chard

### Ordered

  #. One
  #. Two

## Definition Lists

Term 1

: Definition 1

Term 2 with *inline markup*

: Definition 2

## Horizontal Rule

---

## Tables

The original table text does not need to be aligned, but it's a good idea.

| Right   | Left   | Default   | Center   |
| ------: | :----- | --------- | :------: |
| 12      | 12     | 12        | 12       |
| 123     | 123    | 123       | 123      |
| 1       | 1      | 1         | 1        |

## Math

It's a good idea to restrict yourself to the commands and environments supplied by MathJax.

Here is some inline math: $y = ax^2 + bx + c$.

Here is some display math:

$$
\begin{aligned}
y &= ax^2 + bx + c  \\ 
  &= (x + d) (x + e)
\end{aligned}
$$

## Links

Text enclosed by angle-brackets automatically gets rendered as a link: <http://google.com>.

To use link text the longer syntax must be used [Duck Duck Go!](https:/duckduckgo.com).

Email addresses need to be made explicit [eMail me](mailto:andrew.punnett@gmail.com).

Links can also be defined elsewhere in the document, see [link label] or [new link label][link label].

<!-- Link specifications -->
[link label]: <https://duckduckgo.com> 'link title'

Internal links also work: jump back to the [Paragraph Section](#section-paragraphs)


## Images

An inline image ![Image caption](https://upload.wikimedia.org/wikipedia/commons/f/f0/10BlackBuck.jpg)

## Footnotes

Here is a footnote reference ^[Why am I stuck in a footnote?]

## Citations

Here is a nice paper [@whittaker1973niche].

Citations require the `--filter pandoc-citeproc` option to be passed when compiling the document.
The `link-citations: true` option in the YAML is also really nice.
The citation style is controlled by the `csl` YAML option and the bibliography file is specified by the `bibliography` option.

# References

