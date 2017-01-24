# Ruin this font!

This is a place for Type Network folk to mess around, risk-free, with GitHub. Try stuff out!

## Things to try:

* Add some new glyphs
* Add some new kern pairs
* Add a {sups} and {sinf} feature
* Add a light weight
* Save a build to the `/fonts` folder
* Open an issue and assign it to someone

## Advanced things to try

* Create a new branch
* Submit a pull request
* Fork the repository

## Process

* Install [GitHub Desktop](http://desktop.github.com)
* Hit "Clone or Download" and then "Open in Desktop"
* Select a local path for the repository
* If you cloned it a while ago, hit Sync or `cmd+s` to get the latest version.
* Make changes to the repository
* See the exact files and lines you changed appear in the "Uncommitted changes" panel
* Enter a commit message for these changes and hit "Commit to master" or `cmd+Enter`. This commits the change to your local repo, but not to the cloud.
* Once committed, sync your local repository with the one on the cloud. Push the button in the top right or hit `cmd+s`. This will pull any other updates from the cloud, and then push your updates to the cloud. If there are any discrepancies, a message will appear and tell you where they are.

## About the repository

This uses my [sample font repository](https://github.com/djrrb/sample-font-repository), based on the [Unified Font Repository v2.0](https://github.com/raphaelbastide/Unified-Font-Repository), a standard way to organize font project source files. I have expanded upon this structure to make something that generally works for me.

I have adopted this structure because it keeps my project folders organized and predictable. Knowing nothing about a font or its development, I can come to a repository and have a sense of where the latest and greatest fonts are, and what the family is like. It allows me to write scripts that can make assumptions about where the latest masters are and where the fonts should go.

This README, and other files in the repository, are in Markdown format (you might know it ias the syntax used in WriterPro). It is worth familiarizing yourself with [Markdown’s basic syntax](https://daringfireball.net/projects/markdown/syntax).

Below is a quick rundown of the contents of this repository.

## /sources

All of your UFOs go in here. The idea is to be predictable. No UFOs are stored in the main folder; all are stored in a subfolder that describes the type of source. You can add as many source categories as the project requires, but we can expect the primary data to reside in two directories, `/1-drawing` and `/2-build`. The sources folder can also contain other file formats for dealing with sources such as Superpolator files.

### /sources/1-drawing

This directory contains the "masters", namely the UFOs that you are drawing in. These sources can be somewhat "under construction", and can include scrap glyphs, double encodings, and other shortcuts that may not make it into the final fonts. 

*If I want to expand this family, this is where I will start.*

### /sources/2-build

This contains the UFOs that are used when generating font data. This will include interpolated instances, and fonts that have had scrap glyphs removed and are otherwise mastered and ready for generation.

*If I want to generate some fonts from UFO, this is where I will start.*

### /sources/features

It is not necessary to store your features in a separate file or folder, but it makes sense if your features will be shared across sources. In your UFO,

    ../features/Sample_Font.fea

## /fonts

This folder contains a copy of the most recent version of generated fonts.

*If I want to grab the latest and greatest fonts, this is where I will start.*

## /dist

This folder contains an archive of the generated fonts of major versions. While it is possible to go back in time and retrieve old files using Git, it seems to make sense to store major iterations of the font here for easy access.

## /documentation

This directory is primarily intended for documents that describe how to use the font and how to edit it. These can be written in Markdown format.

I have also been using this directory as a place to store proofs, reference files, and other secondary files that I have used in the design process and want to keep with my font files.

## /scripts

A directory of development tools that are specific to this typeface.

### README.md

A space for basic information about the typeface.

### LICENSE.txt

Either a link or the full text for the font’s license.

### FONTLOG.md

A simple space to keep track of major revisions to the font.

### METADATA.yml

This contains searchable metadata in [YAML](https://en.wikipedia.org/wiki/YAML) that we can use to tag, categorize, and search through the UFO library. I’m still figuring out the best way to use this file, but for now it has the following structure:

#### Information about the repository itself:
* unified font repository version: "0.2"
* unified font repository url: https://github.com/raphaelbastide/Unified-Font-Repository/

#### Information about the typeface family:
* name
* tags
* repository url
* project url
* project status (released, gamma, beta, alpha)
* tools (used to create the typeface)
* similar fonts
* sample text

### COPYRIGHT.md & TRADEMARK.md

Simple spaces to keep track of important of the copyright and trademark status of the typeface.
