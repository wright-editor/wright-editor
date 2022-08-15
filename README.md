# wright-editor: A modern extendible editor for text and other things.
The goal of this project is to create an editor that is extendible in many different languages. This editor will consider graphical features and user friendlyness a priority. This editor is inspired by emacs, visual studio code, and neovim.


## Extending
wright-editor should have a very minimal core, almost everything (including graphical frontend) should be an extension. Extensions should be created using Panlang languages or Rust. These extensions canbe compiled and loaded as dlls or equivalent. 

A database of extenstions should be created, hosted on github (or other git hosting site). I hope to have compilation available through a github action, enabling quick download and execution. Security will be a concern for extensions, so proper vetting and testing must be done.

## Documentation
In a way similar to emacs, functions and objects will document themselves and this documentation will be easiliy avavilible through a set of core functions.

## Graphics manager
One of the core features of wright-editor will be its graphics manager. This should be a frontend agnostic tool, essentially equivalent to a window manager. The manager will contain a graphical toolkit that supports multiple frontends. 

For example, a widget could be created with a web frontend and a TUI frontend (crossterm). Widgets can then be called from a Panlang configuration language. Not all frontends must exist for every widget. It is up to extension creators to provide frontend support. Multiple frontends should be able to be used simultaniously in a way resembling the emacs daemon.

## First Frontends
I hope to support TUI (crossterm) and web (possibly tao or webrender) frontends. Other frontends may be added (GTK, QT), but probably won't be nessesary. All extensions created or supported by the wright-editor organization should support at least the web and TUI frontends.

## Crossplatform
This editor should support all 3 major desktop platforms, with mobile platforms being low priority.

## Themes
The look and feel of a widget depends on the frontend code; however, the colorscheme will depend on a set of 24 colors (base24). These 24 colors will be set by the graphics manager and passed to the frontend. 

