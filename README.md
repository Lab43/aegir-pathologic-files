Aegir Pathologic Files
======================

A tiny Drupal Module to simplify file paths in content. This helps prevent broken images when the site directory name changes. Requires an apache rewrite rule to point /files to /sites/example.com/files, which [Aegir](http://www.aegirproject.org/ "Aegir") provides by default.

/sites/example.com/files/example.jpg is changed to /files/example.jpg

Rewriting is handled by the [Pathologic](http://drupal.org/project/pathologic "Pathologic") and happens when content is rendered. The original path is not changed in the content.


## Why

This module solves a common problem in developing Drupal websites with Aegir. When a site's url changes (such as when moving from staging to development) Aegir changes the name of the site's directory. Aegir does a good job of rewriting urls in file and image fields, but it doesn't change urls in body content. With this module, it's irrelevant if the site directory name is wrong because it gets stripped out.


## Caching

Drupal caches the output of input filters like Pathologic. It may be necessary to clear the caches to ensure that paths are being rewritten. See [this page](http://drupal.org/node/257026 "Pathologic Documentation") for more details on caching.