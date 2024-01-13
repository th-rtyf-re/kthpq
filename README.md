KTH-PQ: a beamer template for KTH Royal Institute of Technology
===============================================================

General information
-------------------

This software provides a LuaLaTeX beamer template following KTH's
[Brand guidelines](https://intra.kth.se/en/administration/kommunikation/varumarke/grafiskprofil/kth-s-grafiska-profil-1.844676)
published in October 2023. This package is not directly supported by KTH or
its communications department.

External files
--------------

The files `beamer...themekthpq.sty` and the file `documentation.tex` are
distributed under the MIT license. See `LICENSE.txt` for more details. This is
only relevant if you plan on distributing the software. If you are just
using the template for a presentation, there is no need to worry about this :)

This software includes parts of
[Figtree](https://github.com/erikdkennedy/figtree/tree/master), found in the
directory `fonts/Figtree`.

This package also includes elements of KTH's visual identity. These are stored
in the `kthpq-files/figs` directory.

Other files
-----------

This software is meant to be accessible via the
[Overleaf gallery](https://www.overleaf.com/gallery/tagged/kth), where it is
accompanied by the `.tex` file `sample.tex`.

How to use
----------

See the [documentation](https://github.com/th-rtyf-re/kthpq-docs) for a more
detailed presentation of the template.

### On Overleaf

Use the [Overleaf template](https://www.overleaf.com/latex/templates/kthpq-a-kth-beamer-template/ntqfkcrrsbhf)
or copy this repository to your project.

### On your computer

Put this repository somewhere accessible by TeX (the simplest is to put the
files in your working directory).

### In both cases

Your preamble should look something like this:
    
    \documentclass[17pt, t, lualatex]{beamer}
    
    ...
    
    \usetheme[...]{kthpq}
    
    \begin{document}

Regarding the document class options:
- `17pt` and `14pt` look pretty good, but the template is designed for 17pt and
  the given slide size (254 x 143mm).
- `t` aligns slides to the top, which is closer to the PowerPoint template
  provided by KTH.
- `lualatex` is used when using `kthpq` with the `LuaLaTeX` engine, see options
  below.

The following options are available when loading the theme:
- `engine=lualatex` or `pdflatex`. The default and recommended engine
  for compiling with `kthpq` is `lualatex`, which is the only way to get the
  recommended fonts Figtree and Georgia. The option `pdflatex` should be
  faster, but uses Helvetica and Bitstream Charter.
- `mathshape=sf`, `rm`, or `custom`. This determines the shape used for math.
  The default is `sf`, sans-serif. `rm` corresponds to serif and `custom`
  means that no new math font is loaded (in case you want to load your own
  font).
- `fontdir=<directory>` or `auto`. Provide the directory path (relative or
  absolute) to the Figtree font files. The path used on Overleaf is provided
  in `sample.tex`. For local setups, use the option `auto` when `fontspec` can
  find the font by itself.
