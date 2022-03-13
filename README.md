# hugo-module-img-srcset
A Hugo module to modify image Markdown tags to support srcsets

This module turns your normal image shortcode into a srcset:

```markdown
![I wonder where I have to go](image/map.jpg "a map of the universe")
```
resizes the image to support multiple view port sizes and renderes the appropriate HTML source set:

```html
<p class="md__image">
<picture>
  <source media="(min-width:500px)" srcset="/.../image/map_500x0_resize_q75_box.jpg">
  <source media="(min-width:800px)" srcset="/.../image/map_800x0_resize_q75_box.jpg">
  <source media="(min-width:1200px)" srcset="/.../image/map_1200x0_resize_q75_box.jpg">
  <source media="(min-width:1500px)" srcset="/.../image/map_1500x0_resize_q75_box.jpg">
  <img src="image/map.jpg" alt="a map of the universe" title="a map of the universe" style="width:auto;">
  <figcaption>I wonder where I have to go</figcaption>
</picture>
</p>
```

## Usage

Add the module to your `config.toml` :
```toml
theme = [ "github.com/jan-xyz/hugo-module-img-srcset"]
```

## Example

[github.com/jan-xyz/blog](https://github.com/jan-xyz/blog)
