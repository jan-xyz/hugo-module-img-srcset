# hugo-module-img-srcset

A [Hugo](https://gohugo.io) module to modify image Markdown tags to support [srcsets](https://www.w3schools.com/tags/att_source_srcset.asp)

This module turns your normal image shortcode into a srcset:

```markdown
![I wonder where I have to go](image/map.jpg "a map of the universe")
```

resizes the image to support multiple view port sizes and renderes the
appropriate HTML source set:

```html
<p class="md__image">
<picture>
  <source media="(min-width:500px)" srcset="/.../image/map_800x0_resize_q75_box.jpg">
  <source media="(min-width:800px)" srcset="/.../image/map_1200x0_resize_q75_box.jpg">
  <source media="(min-width:1200px)" srcset="/.../image/map_1500x0_resize_q75_box.jpg">
  <source media="(min-width:1500px)" srcset="image/map.jpg">
  <img src="/.../image/map_500x0_resize_q75_box.jpg" alt="a map of the universe" title="a map of the universe" style="width:auto;">
</picture>
</p>
```

## Installation

1. Install as a Git submodule:

```bash
git submodule add https://github.com/jan-xyz/hugo-module-img-srcset.git themes/hugo-module-img-srcset
```

2. Register as a [theme component](https://gohugo.io/hugo-modules/theme-components/) in `config.toml`:

```toml
theme = [ "your-current-theme", "hugo-module-img-srcset"]
```

## Example

[github.com/jan-xyz/blog](https://github.com/jan-xyz/blog)
