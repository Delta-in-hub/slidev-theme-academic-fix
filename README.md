# slidev-theme-academic [![demo website status](https://img.shields.io/website?down_color=red&up_color=green&label=demo&url=https%3A%2F%2Fslidev-theme-academic.alex-eble.de)](https://slidev-theme-academic.alex-eble.de) [![npm](https://img.shields.io/npm/v/slidev-theme-academic?color=blue)](https://www.npmjs.com/package/slidev-theme-academic) [![https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://www.conventionalcommits.org/)

Simplifies creating academic presentations with [Slidev](https://github.com/slidevjs/slidev) by providing the necessary components and layouts.

## Install

Add the following frontmatter to your `slides.md`. Start Slidev then it will prompt you to install the theme automatically.

```
---
theme: academic
---
```

Learn more about [how to use a theme](https://sli.dev/themes/use).

## Layouts

### cover

| **Parameter name**    | **Type** | **Default**                       | **Notes**                                                                         |
| --------------------- | -------- | --------------------------------- | --------------------------------------------------------------------------------- |
| `author`              | String   | `undefined`                       | -                                                                                 |
| `authorUrl`           | String   | `undefined`                       | -                                                                                 |
| `backgroundUrl`       | String   | `undefined`                       | Adapt the text color with the built-in `class` attribute in the same frontmatter. |
| `backgroundSource`    | String   | `undefined`                       | -                                                                                 |
| `backgroundSourceUrl` | String   | `undefined`                       | -                                                                                 |
| `date`                | String   | `new Date().toLocaleDateString()` | -                                                                                 |

![cover](https://user-images.githubusercontent.com/35292572/156066647-8c38b9f9-745f-4b24-9210-275da430115d.png)

### table-of-contents

`table-of-contents` puts custom content above the table of contents. This defaults to `<h1>Table of Contents</h1>` if none is given.

![table-of-contents](https://user-images.githubusercontent.com/35292572/156066655-86472854-d618-4802-ad5b-1712b22ad17b.png)

### figure

| **Parameter name**       | **Type** | **Default** | **Notes**                |
| ------------------------ | -------- | ----------- | ------------------------ |
| `figureCaption`          | String   | `undefined` | -                        |
| `figureFootnoteNumber`   | Number   | `undefined` | Align with a `Footnote`. |
| `figureUrl`<sup>\*</sup> | String   | `undefined` | -                        |

![figure](https://user-images.githubusercontent.com/35292572/156066665-85553da4-410c-4704-a3d5-a43f465e8fec.png)

### figure-side

| **Parameter name**       | **Type** | **Values**   | **Default** | **Notes**                |
| ------------------------ | -------- | ------------ | ----------- | ------------------------ |
| `figureCaption`          | String   | -            | `undefined` | -                        |
| `figureFootnoteNumber`   | Number   | -            | `undefined` | Align with a `Footnote`. |
| `figureUrl`<sup>\*</sup> | String   | -            | `undefined` | -                        |
| `figureX`                | String   | `'l'`, `'r'` | `'r'`       | -                        |

![04](https://user-images.githubusercontent.com/35292572/156252099-12a05678-d315-4b86-9540-c5668c4d8335.png)

## Components

### Footnotes

`Footnotes` is to be used as parent of `Footnote` children.

| **Parameter name** | **Type** | **Values**      | **Default** |
| ------------------ | -------- | --------------- | ----------- |
| `footnotesX`       | String   | `'l'`, `'r'`    | `'r'`       |
| `separator`        | Boolean  | `true`, `false` | `false`     |

### Footnote

`Footnote` is to be used as children of a `Footnotes` parent.

| **Parameter name** | **Type** | **Notes**                                         |
| ------------------ | -------- | ------------------------------------------------- |
| `number`           | Number   | Align with an attribution in the slides' content. |

![Footnotes & Footnote](https://user-images.githubusercontent.com/35292572/156066705-28c687f0-7d1c-4acb-bfdc-f267d397e7c2.png)

### Pagination

`Pagination` is rendered globally by default. It is configurable inside the `themeConfig` block in the frontmatter of the first slide.

| **Parameter name** | **Type** | **Values**   | **Default** | **Notes**                                                                                                                                          |
| ------------------ | -------- | ------------ | ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `paginationX`      | String   | `'l'`, `'r'` | `'r'`       | To disable global default rending, set both `paginationX` and `paginationY` to `undefined`. `Pagination` can then still be used on selected pages. |
| `paginationY`      | String   | `'b'`, `'t'` | `'t'`       | To disable global default rending, set both `paginationX` and `paginationY` to `undefined`. `Pagination` can then still be used on selected pages. |

![Pagination](https://user-images.githubusercontent.com/35292572/156066719-86209c2c-c3d3-41d7-ad5a-ced806f7ac46.png)

## Contributing

- `npm install`
- `npm run dev` to start theme preview of `example.md`
- Edit the `example.md` and style to see the changes
- `npm run export` to generate the preview PDF
- `npm run screenshot` to generate the preview PNG
