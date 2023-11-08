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
directory `fonts/Figtree`, and
[Bitstream Vera 1.10](https://download.gnome.org/sources/ttf-bitstream-vera/),
found in the directory `fonts/ttf-bitstream-vera-1.10`, retrieved in November,
2023. See `LICENSE.txt` for information about their licensing.

This package also includes elements of KTH's visual identity. These are stored
in the `kthpq-files/figs` directory.

Other files
-----------

This software is meant to be accessible via the
[Overleaf gallery](https://www.overleaf.com/gallery/tagged/kth), where it is
accompanied by the `.tex` file `sample.tex`.

This software also includes the file `documentation.tex`, along with its
compiled output `documentation.pdf`, which serves as the documentation of the
software.

How to use
----------

### On Overleaf

Use the [Overleaf template](does not exist yet) or copy the file
`beamertemplatekthpq.sty` and the folder `kthpq-files` to your project.

### On your computer

Put this repository somewhere accessible by TeX (the simplest is to put the
files in your working directory)

### In both cases

Add `\usetheme{kthpq}` to your preamble, probably towards the end. There are
two options you can add when loading the theme:
- `engine=lualatex` or `engine=latex`. The default and recommended engine for
  compiling with `kthpq` is `lualatex`, which is the only way to get the
  recommended fonts Figtree and Georgia. The option `latex` should be faster,
  but uses Helvetica and Bitstream Charter.
- `mathshape=sf` or `rm`. This determines the shape used for math. The default
  is `sf`, sans-serif, and `rm` corresponds to serif.