# TiddlyWiki Static Site Publishing

A set of scripts designed to work with Github Actions for Static Site Publishing for TiddlyWiki.

## Overview

Update a single file TiddlyWiki and check it into git, and the Github Action here will generate a static version of the site.

This static site will have your default home page at `index.html` (at the root of your site) and all of the tiddlers will be at `YOURNAME.github.io/REPO/my-tiddler.html`, or `example.com/my-tiddler.html` if you have mapped a custom domain.

## Instructions

1. Fork this repo
2. Edit the shadow tiddler `$:/core/templates/static.template.html` to remove the `static/` prefix in the macro tv-wikilink-template
3. Check in your own single file wiki -- the default `build.sh` expects it to be named `index.html` but you can call it whatever you like
4. Add a `gh-pages` branch -- can be empty, it is overwritten on publish
5. Set Github Pages settings to publish from the `gh-pages` branch 

If you set up your single file wiki with a Github Git saver, whenever you save, a new version of your site will automatically be built and published.

## Acknowledgements

Thanks to @saqimtiaz for the build script and general support and good energy!

Uses [JamesIves/github-pages-deploy-action](https://github.com/JamesIves/github-pages-deploy-action) as the final step in the action, inspired by [pengx17/logseq-publish](https://github.com/pengx17/logseq-publish).

## Examples

* [bmann/twgroceries](https://github.com/bmann/twgroceries) - https://foodwiki.bmann.ca

## Discussion

Extended discussion on the [Talk TW forum »](https://talk.tiddlywiki.org/t/rfi-github-actions-static-publishing-script/5203)