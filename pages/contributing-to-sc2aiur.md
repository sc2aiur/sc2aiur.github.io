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

This will cover the basic, browser-based interface. I personally do something

## Editing posts

To edit a post, ensure you're logged in; then head to
https://github.com/sc2aiur/sc2aiur.github.io/ and locate the post or page you'd
like to edit.

Let's assume you want to edit
[blog/src/pages/pvp.md](https://github.com/sc2aiur/sc2aiur.github.io/blob/src/pages/pvp.md) . In the
upper right, there is an Edit button that takes you to
[edit/src/pages/pvp.md](https://github.com/sc2aiur/sc2aiur.github.io/edit/src/pages/pvp.md)
(note that "blob" changed to "edit" in the URL.

You'll first be asked to **fork** the repository - in other words, to create
your own copy of the main repository. That's the one you can freely change, but
it won't get published automatically.

Once you've forked the repository, change whatever you want, then head down.
Describe the changes you've made and submit the **pull request**. This is
GitHub's mechanism through which you'll allow others to review your changes
before they're merged into the main repository.

There may be some back and forth before the changes are accepted.
By default, you'll get e-mail notifications on any new messages.

## Creating new posts

To create a new post/page, first open up [the content template](https://raw.githubusercontent.com/sc2aiur/sc2aiur.github.io/src/CONTENT_TEMPLATE.md) .
Then, head over to to the [posts
directory](https://github.com/sc2aiur/sc2aiur.github.io/tree/src/posts) and hit
the [add file
button](https://github.com/sc2aiur/sc2aiur.github.io/new/src/posts). Copy the raw template to the new file you're creating.
The part at the top is the Nikola metadata that identifies each post.

* `title` is the long title of the post.
* `slug` is the URL bit, such as `pvp`.
* `date` should be the day on which you're putting the post up, so things can be sorted by date.
* `tags`, separated with commas, let people easily access all content on e.g. PvP or early game play.
* `link` should lead to the original source material, if there is one and only one post you're referring to.

Remember to **embed** YouTube videos (go to Share -> Embed).

## Automated checks

Pull requests made to the repository go through two automated checks, which
show up at the bottom of the pull request's page:

* `ci/cirleci: build-website` ensures that any changes you make don't break the website hard enough that it won't even build. If that errors out, look through the logs to find the cause (or ask!).
* `website` offers a preview of the website as it would look when built including your new and awesome changes. Click on `details` to see the preview.
    * Note that **links get broken on the preview**, but there is a workaround: links like https://90-280468856-gh.circle-artifacts.com/0/output/posts/ will display an "Artifact not found" error, but if you manually append `index.html` [like this](https://90-280468856-gh.circle-artifacts.com/0/output/posts/index.html), the link should work.


