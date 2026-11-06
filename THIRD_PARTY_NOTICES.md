# Third-Party Notices — TabViewer

Last updated: 1 November 2026

TabViewer is freeware by jayusop. This document lists every third-party
component, data source and trademark involved in TabViewer, and states under
which terms each one is used. It forms part of the TabViewer documentation and
is shipped with every release.

**Summary**

| Item | Included in the app? | Terms |
|---|---|---|
| Steinberg VST® 3 SDK (hosting sources) | Yes — compiled into the app | MIT License (full text below) |
| Apple macOS frameworks | No — part of macOS | Apple's macOS license |
| macOS General MIDI sound bank, Apple Symbols font | No — read from macOS at run time | Apple's macOS license |
| Audio Unit / VST 3 plug-ins you install | No | Each plug-in maker's license |
| Fonts on the documentation website | No — loaded from Google Fonts | SIL Open Font License 1.1 |

Everything else in TabViewer — the score parsers and writer, the layout and
rendering engine, the playback engine, the user interface and the app icon — was
written for this project. No code was copied from other programs or libraries.
TabViewer contains no third-party fonts, sound samples or score files.

---

## 1. Components included in TabViewer

### Steinberg VST® 3 SDK

- Purpose: loading and playing VST 3 instrument plug-ins installed on your Mac.
- Parts used: the hosting sources of the SDK (`pluginterfaces`, `public.sdk/source/common`,
  `public.sdk/source/vst/hosting`, `public.sdk/source/vst/utility`), compiled into the app.
  VSTGUI and the SDK samples are not used.
- Where the notice appears: this document and the app's **About TabViewer** window
  (full MIT License text).
- Version: VST SDK 3.8.1 (build 84), included as a Git submodule of the source repository
- Source: https://github.com/steinbergmedia/vst3sdk
- License: MIT License

    MIT License

    Copyright (c) 2026, Steinberg Media Technologies GmbH

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.

The MIT License above applies only to the Steinberg VST 3 SDK. It does not apply
to TabViewer as a whole, which is licensed under the TabViewer Freeware License
(see `LICENSE`). Nothing in the TabViewer Freeware License — including its
restriction on reverse engineering — limits any right you have under the MIT
License with respect to the Steinberg VST 3 SDK.

"VST is a registered trademark of Steinberg Media Technologies GmbH."

---

## 2. Components used at run time but not included

TabViewer uses the following parts of macOS while it runs. They are installed
with macOS, are not copied into or distributed with TabViewer, and are used
under the terms of Apple's macOS software license.

- **System frameworks**: SwiftUI, AppKit, Foundation, AVFoundation, AudioToolbox,
  CoreAudioKit, CoreGraphics, PDFKit, Compression, UniformTypeIdentifiers, Observation.
  (ZIP/DEFLATE data in `.gp` files is decompressed with Apple's Compression framework.)
- **General MIDI sound bank**: the built-in macOS sound bank
  (`gs_instruments.dls`) is used for the default playback sound.
- **System font**: Apple Symbols is used to draw some music symbols.

## 3. Plug-ins you install yourself

TabViewer can play scores through Audio Unit (AUv2/AUv3) and VST 3 instrument
plug-ins that you have installed on your Mac. TabViewer does not include,
distribute or license any plug-in, sound library or preset. Each plug-in, and
any sounds or licensing service it uses (for example iLok/PACE), is governed
solely by its own maker's license and privacy policy. Plug-ins run inside the
TabViewer process; some may connect to the internet for their own purposes,
such as license activation.

**Score sync with Tablarion.** Tablarion is a plug-in that plays Guitar Pro
files with its own engine. It is made by the same author as TabViewer (jayusop)
and is developed and distributed separately on GitHub:
https://github.com/jayusop/Tablarion

When Tablarion is selected as the instrument, TabViewer can place the open
score into the plug-in's state and supply playback position and tempo the way a
DAW does. Tablarion is a separate program with its own license, published in
its repository; it is not included in or distributed with TabViewer and must be
installed separately. TabViewer contains no code from Tablarion or from the
framework it is built with (JUCE).

## 4. Guitar Pro file format

TabViewer opens Guitar Pro files (`.gp`, `.gpx`, `.gp5`, `.gp4`, `.gp3`) and saves
`.gp5` files so that you can use score files you already have (interoperability).
The reading and writing code was written independently for TabViewer; it does
not contain code or resources from Guitar Pro or from any other software.

## 5. Score files

Scores you open, create or export belong to their respective rights holders.
TabViewer does not include any score files and does not add copyright notices
to your files. You are responsible for having the right to use the scores you
open or share.

## 6. Trademarks

- Guitar Pro is a trademark of Arobas Music. TabViewer is not affiliated with,
  endorsed by or sponsored by Arobas Music.
- VST is a registered trademark of Steinberg Media Technologies GmbH.
- Apple, Mac, macOS, Audio Unit and Apple Symbols are trademarks of Apple Inc.,
  registered in the U.S. and other countries. TabViewer is not affiliated with Apple Inc.
- JUCE and other product and company names are trademarks of their respective
  owners.

Trademarks are used only to describe compatibility, not to suggest endorsement.

## 7. Documentation website

The TabViewer website (`docs/index.html`, served by GitHub Pages) is part of the
documentation, not of the app.

- Fonts: Noto Sans KR and JetBrains Mono, licensed under the SIL Open Font
  License 1.1, are loaded from Google Fonts (fonts.googleapis.com /
  fonts.gstatic.com) and are not redistributed in this repository. When you visit
  the site, your browser connects to Google's servers to download them.
- README badges are images served by shields.io.
- The site is hosted by GitHub (GitHub Pages) and is subject to GitHub's terms
  and privacy statement.

## 8. Contact

Questions about this document: jayusop@gmail.com ·
https://github.com/jayusop/Tab-Viewer/issues

Translations of this document are provided for convenience. If a translation
differs from this English text, this English text prevails.
