<p align="center">
   <img src="https://raw.githubusercontent.com/vinayak-mehta/present/master/docs/_static/present.png" width="200">
</p>

# present

A terminal-based presentation tool.

<p align="center">
   <img src="https://raw.githubusercontent.com/vinayak-mehta/present/master/docs/_static/demo.gif" width="800">
</p>

## Installation

You can simply use pip to install `present`:

```bash
$ pip install present
```

## Usage

```bash
$ present sample.md
```

You can navigate between slides using the arrow keys and quit the presentation with `q`. At the end, you can use `r` to restart the presentation.

## Syntax guide

You can check out the [sample slides](https://github.com/vinayak-mehta/present/blob/master/examples/sample.md) for reference.

**Note:** Some things aren't supported yet.
- Emphasis, inline code, links, blockquotes, tables and strikethroughs.
- Effects and foreground / background colors on the same slide.
- Effects and code on the same slide.

### Slide separator

Each slide can be separated with a `---`.

```
Slide 1

---

Slide 2
```

### Slide style

Each slide can be styled with foreground / background colors and effects. By default, slides are black on white with no effects. You can add style to a slide by adding an HTML comment at the beginning of the slide (after the slide separator):

```
Slide 1

---
<!-- fg=black bg=yellow -->

Slide 2

---
<!-- effect=explosions -->

Slide 3
```

### Text

```
Slide 1

---

Slide 2
```

### Headers

Level 1 headings become figlets, level 2 headings get underlined with `-` and level 3 headings are treated as normal text for now.

```
# Heading 1

## Heading 2

### Heading 3
```

### Lists

Ordered lists become unordered lists automatically.

```
- Item 1
    - Item 1a
    - Item 1b
    - Item 1c
- Item 2
    - Item 2a
```

### Images

Image paths are relative to the directory where you slides are kept and where you invoke `present`.

```
![RC](images/recurse.png)
```

### Code blocks

<pre>
```
import os

os.getcwd()
```
</pre>

## Versioning

`present` uses [Semantic Versioning](https://semver.org/). For the available versions, see the tags on the GitHub repository.

## License

This project is licensed under the Apache License, see the [LICENSE](https://github.com/vinayak-mehta/present/blob/master/LICENSE) file for details.
