---
layout: default
title: TinyMCE 5.2
title_nav: TinyMCE 5.2
description: Release notes for TinyMCE 5.2
keywords: releasenotes bugfixes
---

These release notes provide an overview of the changes for {{site.productname}} 5.2, including:

- [New features and enhancements](#newfeaturesandenhancements)
- [Premium Plugin changes](#premiumpluginchanges)
- [General bug fixes](#generalbugfixes)
- [Deprecated features](#deprecatedfeatures)
- [Known issues](#knownissues)
- [Upgrading to the latest version of TinyMCE 5](#upgradingtothelatestversionoftinymce5)

> This is the {{site.cloudname}} and {{site.enterpriseversion}} release notes. For information on the latest community version of {{site.productname}}, see: [{{site.productname}} Changelog]({{site.baseurl}}/changelog/).

## New features and enhancements

The following new features and enhancements were added for the {{site.productname}} 5.2 release.

### Alternative toolbar and menu bar placement with the `toolbar_location` setting

The `toolbar_location` option is used to position the toolbar and menu bar. Setting this option to `bottom` positions the toolbar and menu bar below the content area.

For information on using the `toolbar_location` setting, see: [User interface options - `toolbar_location`]({{ site.baseurl }}/configure/editor-appearance/#toolbar_location).

### A new placeholder setting

The new `placeholder` option adds placeholder content that will be shown when the editor is empty.

For information on using the `placeholder` setting, see: [User interface options - `placeholder`]({{ site.baseurl }}/configure/editor-appearance/#placeholder).

### Modify the Quick Image toolbar using the `quickbars_image_toolbar` setting

The **quickbars_image_toolbar** option configures the Quick Image toolbar provided by the [quickbars plugin]({{ site.baseurl }}/plugins/quickbars). To change the buttons on the Quick Image toolbar, provide a space-separated string of [toolbar button names]({{ site.baseurl }}/advanced/editor-control-identifiers/#toolbarcontrols). To disable the Quick Image toolbar, set `quickbars_image_toolbar` to `false`.

For information on using the `quickbars_image_toolbar` setting, see: [Quick Toolbars plugin - `quickbars_image_toolbar`]({{ site.baseurl }}/plugins/quickbars/#quickbars_image_toolbar).

### New `tinymce.dom.TextSeeker` API

The TextSeeker class is used for walking across text nodes to match a predicate.

For information on using the `TextSeeker` API, see: [{{site.productname}} APIs - tinymce.dom.TextSeeker]({{ site.baseurl }}/api/tinymce.dom/tinymce.dom.textseeker/).

### renamed toolbar_drawer to toolbar_mode and changed the default to wrap instead of false (both are the same, just wrap is more self explanatory)

### new addGroupToolbarButton API

### Updated the table icons

### Updated the colorinput component visual appearance --- updated color swatches in input fields

### Missing resize_img_proportional setting

This controls how images are resized. It requires a boolean value and the default is true (ie images will resize proportionally).

## Premium Plugin changes

The following premium plugins have been updated for {{site.productname}} 5.2.

### Page Embed

The {{site.productname}} 5.2 release includes **Page Embed** 1.1.0.

**Page Embed** 1.1.0 includes:

* adds a new tiny_pageembed_inline_styles setting to inline the styles in the content (similar to the media embed functionality)

### Permanent Pen

The {{site.productname}} 5.2 release includes **Permanent Pen** 1.1.0.

**Permanent Pen** 1.1.0 adds support for working with [input method editors (IMEs)](https://www.w3.org/TR/ime-api/#IME), which are used for inserting non-ascii characters.

### Premium Skins and Icon Packs

The {{site.productname}} 5.2 release includes **Premium Skins and Icon Packs** 1.2.

**Premium Skins and Icon Packs** 1.2 includes:

* 3 new skins available: 'snow', 'naked' and 'outside'
* 1 new icon pack available: 'thin'

### Spellchecker Pro

The {{site.productname}} 5.2 release includes **Spellchecker Pro** 2.0.

**Spellchecker Pro** 2.0 includes:

* New functionality allowspell check the document in multiple languages
* there's a number of new menu items/buttons

## General bug fixes

{{site.productname}} 5.2 provides fixes for the following bugs:

- 

## Deprecated features


## Known issues

This section describes issues that users of {{site.productname}} 5.2 may encounter, as well as possible workarounds for these issues.

{% assign enterprise = true %}

{% include install/upgrading-info.md %}

{% assign enterprise = false %}