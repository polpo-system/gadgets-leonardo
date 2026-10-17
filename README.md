# gadgets-leonardo

Leonardo for the gadgets of [polpo](https://github.com/polpo-system/polpo): a drawing editor for
structured graphics: rectangles, ellipses, lines, arcs, Bezier curves, splines, captions and images,
with pens, layers, groups and transformations, drawn with Gfx (the package gfx) on the screen and
exported as PostScript (gfx-ps).

```
portia.Install gadgets-leonardo
```

## Using

    Desktops.OpenDoc Leonardo.Panel    the tools
    Desktops.OpenDoc Leonardo.Fig      an example figure (.Fig files open as Leonardo documents)
    Desktops.OpenDoc Leonardo.Text     the guide

The panel has a button for Vinci, a language for drawing with Leonardo, which is a package of its
own. Draw graphics (.Graph) open with gadgets-leodraw.

## What is here

    src/Leonardo.Mod                 figures, shapes, layers
    src/LeoPens.Mod, LeoPaths.Mod, LeoOutliners.Mod, LeoBasic.Mod, LeoSplines.Mod, LeoCaptions.Mod,
        LeoImages.Mod                pens and shapes
    src/LeoFrames.Mod, OLR.LeoTools.Mod, LeoDocs.Mod, OLR.LeoPanels.Mod, OLR.LeoLists.Mod
                                     frames, tools, documents, panels
    src/LeoPenEditors.Mod, LeoPathEditors.Mod, LeoBasicEditors.Mod, LeoCaptionEditors.Mod,
        LeoImageEditors.Mod, LeoSplineEditors.Mod    the editors of the shapes
    share/Leonardo.Panel, Leonardo.Lib, Leonardo.Text, Leonardo.Fig
    tools/Leonardo.Tool
    test/LeonardoTest.Mod

Leonardo is by Erich Oswald. The sources come from ETH Linux Oberon (OLR, 2017-06-18), converted from Oberon texts to plain
text; the first commit has them unchanged. They compile unchanged with all five of polpo's compilers
(x86, ARM, ARMv7, RISC-V, MIPS).

## Tests

    LeonardoTest.Run      4 checks: a figure and a frame made, Leonardo.Fig loaded, the panel
                          opened; it needs the desktop's display

The license is GPL-3 (`LICENSE`); the code comes from ETH Oberon, whose license (`LICENSE.ETH`)
asks to keep its copyright notice and conditions, which `LICENSE.ETH` does.
