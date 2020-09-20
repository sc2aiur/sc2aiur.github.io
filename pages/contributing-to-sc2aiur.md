<!--
.. title: Contributing to SC2Aiur
.. slug: contributing
.. date: 2020-09-20 16:52:38 UTC
.. tags: sc2aiur
.. category: 
.. link: 
.. description: A guide for contributing to SC2Aiur
.. type: text
.. author: Perfi
-->

*So, you want to contribute to our little Protoss content hub?*

First of all, **thank you!** This website is what it is thanks to people like
you.

Now that you know you're appreciated, let's get to it!

# How the site works

The site is built mostly on top of free resources that are accessible to everyone.

We use the [Nikola static site generator](https://getnikola.com/) to turn
[markdown (`.md`) files such as these](https://github.com/sc2aiur/sc2aiur.github.io/tree/src/pages) or [these](https://github.com/sc2aiur/sc2aiur.github.io/tree/src/posts)
into HTML pages [such as this one](https://sc2aiur.github.io/posts/blinkdisruptor-era-pvp/). We store the markdown files in our [GitHub repository](https://github.com/sc2aiur/sc2aiur.github.io/).
We then take those HTML pages and display them using [GitHub Pages](https://pages.github.com/). Each modification of the markdown (or any other) files triggers a rebuild of the website using [GitHub Actions](https://github.com/sc2aiur/sc2aiur.github.io/actions).

## Why GitHub?

We wanted to have something fulfilling these criteria:

* **can be modified by anyone who wants to.**
   * Openness is important to us. We want this site to be owned by the community, for the community.
* **can't be modified** freely, **without someone checking** the changes.
    * That's the problem with a publicly available google doc: you can't really stop spam.
* can be **automated** to allow easy rebuilds without anyone in particular knowing the necesary ~~magic incantations~~ bash commands.
    * This is done so that if any contributor decides to quit StarCraft overnight and become an Among Us progamer, or gets hit by a bus, or anything, the project doesn't suddenly die.

# How to do stuff?

## Editing posts

To edit a post, TODO

## Creating new posts


# The pull request interface

## Automated checks
