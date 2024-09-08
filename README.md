# Deadlock Pages

This repository demonstrates a handful of in-game pages that have been modified from Valve's XML and custom CSS to be compatible in a modern web browser.

These demonstrations are very crude. These pages are for reference and intended to be used as a learning resource and not something that you should actually use on your web page in its current form. It is highly encouraged that you simplify the HTML markup further to be more accessible as well as reduce the stylesheets to be only what is actually used.


## Methodology

[ValveResourceFormat](https://github.com/ValveResourceFormat/ValveResourceFormat) was used to extract and decompile the game layout, styles, and images using the following command:

```
Decompiler -d \
	-i Deadlock/game/citadel/pak01_dir.vpk \
	--vpk_filepath panorama/images,panorama/layout,panorama/styles \
	-o exported
```

Once these resources are extracted manual analysis of the XML and CSS files was done to create new static HTML documents with modified CSS rules that translated custom Valve CSS properties such as `wash-color` to instead be a `mask-image` with `background-color` or with `mix-blend-mode`.


## Pages

- [profile](https://niamu.github.io/deadlock-pages/pages/profile/)
- [post game](https://niamu.github.io/deadlock-pages/pages/post_game/)
- [shop](https://niamu.github.io/deadlock-pages/pages/shop/)
