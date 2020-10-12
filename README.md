# hugo-module-img-srcset
A Hugo module to modify image Markdown tags to support srcsets

This module turns your normal image shortcode into a srcset:

```markdown
![Text](image/map.jpg)
```
gets rendered into

```html
<p class="md__image">
<picture>
  <source media="(min-width:500px)" srcset="/.../images/foo_500x0_resize_q75_box.jpg">
  <source media="(min-width:800px)" srcset="/.../images/foo_800x0_resize_q75_box.jpg">
  <source media="(min-width:1200px)" srcset="/.../images/foo_1200x0_resize_q75_box.jpg">
  <source media="(min-width:1500px)" srcset="/.../images/foo_1500x0_resize_q75_box.jpg">
  <img src="images/foo.jpg" alt="Flowers" style="width:auto;">
</picture>
</p>
```

## Usage

and add the module to your `config.toml` :
```toml
...
theme = [ "github.com/jan-xyz/hugo-module-img-srcset"]
...
```

## Example

[github.com/jan-xyz/blog](github.com/jan-xyz/blog)
