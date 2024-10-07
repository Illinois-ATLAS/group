# Illinois ATLAS Group Webpage

## Overview

This is the source for the Illinois ATLAS Group Website. The website is built with the [Hugo](https://gohugo.io) static website engine and the [Blowfish theme](https://blowfish.page).

### Directory Layout

The directory layout follows the usual Hugo scheme. The most important directories are:

- `content` holds the text content for the site, mostly in [markdown](https://en.wikipedia.org/wiki/Markdown), which is a very simple markup language
  - The subdirectory structure in the `content` directory maps to ´website URLs
- `assets` has content that will be processed by Hugo when building the website - particular images and icons; it also contains any customisation to the CSS styles
- `static` has content that will be available, but is not processed, e.g., PDFs
- `config` contains the files that configure Hugo and Blowfish, in particular the `menus.yaml` file defines the top bar and footer menus

These should be the only directories that you care about if you want to add or update content on the site. If you wish to do some deeper customisation of the site then the `layouts` directory has page templates and Hugo shortcode files.

### Modifying and Adding Content

#### Setup

You will need to [install Hugo](https://gohugo.io/installation) and checkout the code for the website from [GitHub](https://github.com/Illinois-ATLAS/group) (actually, it's recommended that you *fork* the project and work on your own copy if you plan to contribute).

```sh
git clone --recursive https://github.com/Illinois-ATLAS/group.git
```

(The `--recursive` is needed to get the Blowfish theme submodule.)

Assuming you intent to contribute your changes back to the main website, it's best to now create a branch with a meaningful name, from which you will later make a pull request.

#### Edit

If you want to modify the content of a page, simply open the relevant markdown file and update it. Usual markdown syntax is, of course, supported. You will see use of some special Hugo *shortcodes* that can do some things that markdown cannot (e.g., the `figure` shortcode for more image handling options, the `flex-columns` shortcode for multi-column layouts; Blowish also has [bunch of nice shortcodes](https://blowfish.page/docs/shortcodes) to make badges, buttons, alerts, etc.).

To add new content:

- Create a new markdown file as it would appear in the website hierarchy. E.g., `content/about/wombats.md` would create a page that would get rendered, when deployed, to `https://Illinois-ATLAS/group/about/wombats/`.
- If necessary, add a menu item for the new page in `config/menus.yaml`

#### Preview Changes

Run `hugo serve` in the base directory of your check that the changes work as you expect.

#### Pull Request

When you are happy, push the changes to your fork, then make a pull request back to the main EVERSE repository.

## Problems? Issues?

If you see something wrong with the site, or you want to suggest a change, please open a [GitHub Issue](https://github.com/Illinois-ATLAS/group/issues/new).

## Help

Mark (msn@illinois.edu) can try and help you if you get stuck.
