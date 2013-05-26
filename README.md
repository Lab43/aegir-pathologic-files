Aegir Pathologic Files
======================

A tiny Drupal Module to simplify paths in content that point to the files directory. This helps prevent broken images when the site directory name changes. Requires an apache rewrite rule to point /files to /sites/exmaple.com/files, which Aegir provides by default.

/sites/files/example.jpg becomes /files/example.jpg

This module solves a common problem in developing Drupal websites with Aegir. When a site's url changes (such as when moving from staging to development) Aegir changes the name of the site's directory. Aegir does a good job of rewriting urls in file and image fields, but it doesn't change urls in body content. With this module, it's irrelevant if the site directory name is wrong because it's getting stripped out.

This module requires the Pathologic module.