# Apple Keynote Slide Deck re-created using GitPitch

In this repository you will find a number of sample GitPitch slide decks. Each deck takes a slightly different approach to re-creating the original [ElixirCodeBeam.key](ElixirCodeBeam.key) Apple Keynote presentation.

1. [The new GitPitch Slide Deck mimicking the original Keynote Deck](#the-new-gitpitch-slide-deck-mimicking-the-original-keynote-deck)
1. [The new GitPitch Modular Slide Deck](#the-new-gitpitch-modular-slide-deck)
1. [The new GitPitch Modular Slide Deck Alternative](#the-new-gitpitch-modular-slide-deck-alternative)
1. [A Quick Word on GitPitch Customization / Branding](#a-quick-word-on-gitpitch-customization--branding)
1. [GitPitch Publishing Online + Export to PDF and PowerPoint PPTX](#gitpitch-publishing-online--export-to-pdf-and-powerpoint-pptx)
1. [Some Final Observations About GitPitch for Developers](#some-final-observations-about-gitpitch-for-developers)

## The new GitPitch Slide Deck mimicking the original Keynote Deck

This basic deck is an example of the original Keynote deck re-created using a single GitPitch markdown file. 

- View the new GitPitch Slide Deck Online:
    - [https://gitpitch.com/gitpitch/demo-jv](https://gitpitch.com/gitpitch/demo-jv)
- View the new [Gitpitch Slide Deck Markdown](PITCHME.md)

The following files were used to create this slide deck:

```tree
.
├── PITCHME.md
├── PITCHME.yaml
└── assets
    ├── fonts
    │   ├── YanoneKaffeesatz-Bold.woff2
    │   ├── YanoneKaffeesatz-Medium.woff2
    │   └── YanoneKaffeesatz-Regular.woff2
    └── img
        ├── dashbit-brand.png
        ├── dashbit-logo.png
        ├── elixir-dashbit-splash.png
        ├── erlang-docs.png
        ├── test-gist-1.png
        └── test-gist-2.png
```

Note the file naming and directory layout follows conventions introduced in the [GitPitch In 60 Seconds Tutorial](https://gitpitch.com/docs/getting-started/tutorial). 

> As I didn't have access to your original images I had to create a few substitutes to complete this demo. You can of course replace my images with your own higher quality originals if needed.

## The new GitPitch Modular Slide Deck

This modular deck is the original Keynote deck re-created using GitPitch while taking advantage of [GitPitch Modular Markdown](https://gitpitch.com/docs/git). Because the sample Keynote deck was quite simple (few slides) creating a modular deck might seem like overkill. But I hope to demonstrate some powerful features that might be useful to you. Particularly if you ever need to create more extensive decks for conferences, or to deliver training materials for any of the technologies that you work on.

- View the new GitPitch Modular Slide Deck Online:
    - [https://gitpitch.com/gitpitch/demo-jv?p=talk](https://gitpitch.com/gitpitch/demo-jv?p=talk)
- View the new [GitPitch Modular Slide Deck Markdown](talk/PITCHME.md)

GitPitch modular markdown gives presentations authors many of the same advantages developers get from modular code - simplicity, flexibility, and better maintainability. But it also delivers one additional benefit - the ability to publish and share *modular presentations*. Basically each modular markdown file becomes a `mini-deck` that can be viewed or shared independently of the master deck:

- View The Complete Deck Online:
    - [https://gitpitch.com/gitpitch/demo-jv?p=talk](https://gitpitch.com/gitpitch/demo-jv?p=talk)
- View The Elixir v1.10 Module Online:
    - [https://gitpitch.com/gitpitch/demo-jv?p=talk/elixir-110](https://gitpitch.com/gitpitch/demo-jv?p=talk/elixir-110)
- View The Elixir v1.11 Module Online:
    - [https://gitpitch.com/gitpitch/demo-jv?p=talk/elixir-111](https://gitpitch.com/gitpitch/demo-jv?p=talk/elixir-111)
- View The Broadway v0.6 Module Online:
    - [https://gitpitch.com/gitpitch/demo-jv?p=talk/broadway-06](https://gitpitch.com/gitpitch/demo-jv?p=talk/broadway-06)
- View The Ecto v3.4 Module Online:
    - [https://gitpitch.com/gitpitch/demo-jv?p=talk/ecto-34](https://gitpitch.com/gitpitch/demo-jv?p=talk/ecto-34)
- View The Phoenix Module Online:
    - [https://gitpitch.com/gitpitch/demo-jv?p=talk/phoenix](https://gitpitch.com/gitpitch/demo-jv?p=talk/phoenix)

The following files were used to create this modular slide deck:

```tree
.
├── PITCHME.yaml
└── talk
    ├── PITCHME.md
    ├── broadway-06
    │   └── PITCHME.md
    ├── ecto-34
    │   └── PITCHME.md
    ├── elixir-110
    │   └── PITCHME.md
    ├── elixir-111
    │   └── PITCHME.md
    └── phoenix
        └── PITCHME.md
```

Here I have arbitrarily chosen `talk` as the top-level directory name for this deck. But of course it could be named anything. This sample deck also demonstrates a key GitPitch feature - support for unlimited slide decks within a single Git branch where decks can share common assets such as images, custom CSS styles, and [PITCHME.yaml](https://gitpitch.com/docs/settings/pitchme/) settings.

## The new GitPitch Modular Slide Deck Alternative

This modular deck is the original Keynote deck re-created using GitPitch while again taking advantage of modular markdown. But this time I'm interested in the benefits of modular markdown only, I'm not interested in publishing or sharing `mini-decks` as independent modules. 

- View the new GitPitch Modular Slide Deck Alternative Online:
    - [https://gitpitch.com/gitpitch/demo-jv?p=training](https://gitpitch.com/gitpitch/demo-jv?p=training)
- View the new [GitPitch Modular Slide Deck Alternative Markdown](training/PITCHME.md)

Whenever modular slide decks are not needed but you do want to use modular markdown you can simplify the directory structure for you deck by placing the markdown files for each topic in a single directory: 

```tree
.
├── PITCHME.yaml
└── training
    ├── PITCHME.md
    └── topics
        ├── broadway-06.md
        ├── ecto-34.md
        ├── elixir-110.md
        ├── elixir-111.md
        └── phoenix.md
```

Here I have arbitrarily chosen `training` as the top-level directory name for this deck but it could be named anything.

## A Quick Word on GitPitch Customization / Branding

I believe I have been able to create a pretty close approximation of your original Keynote template. This
was achieved by tweaking the default [GitPitch Customizable Theme](https://gitpitch.com/docs/themes/default) and activating [custom fonts](https://gitpitch.com/docs/themes/custom-fonts) to match your preferred *Yanone Kaffeesatz* font. 

> Note you can activate [Custom CSS](https://gitpitch.com/docs/themes/custom) for unlimited control over the appearance of content on your slides but it was not needed for these decks.

By convention all such customizations are activated in a settings file that sits alongside the markdown for your slide deck. For example settings, see the [PITCHME.yaml](PITCHME.yaml) for the slide decks in this repo.

## GitPitch Publishing Online + Export to PDF and PowerPoint PPTX

While [GitPitch Desktop](https://gitpitch.com/docs/work-offline/desktop) gives you a dedicated tool for developing and presenting offline you can publish GitPitch slide decks in a number of ways. Including a simple `git-push` to publish public, private, and password-protected slide deck online at gitpitch.com.

You can also use the Desktop app to export any slide deck as PDF and PPTX. I have exported your slide deck using the Desktop and included those sample documents in this repo for your perusal. Note, these documents have been exported with [slide fragment printing](https://gitpitch.com/docs/settings/print/) disabled. As the guide indicates, you can export slide decks to print individual fragments is wanted.

## Some Final Observations about GitPitch for Developers

The content in this repo is for demonstration purposes. Three different approaches to creating the same sample slide deck have been provided. All are a close approximation to your original Keynote presentation. Each approach attempts to demonstrate both the simplicity and flexibility of GitPitch. There are of course lots more delightful features that you'll find once you dig  into the [docs](https://gitpitch.com/docs).

It's also worth noting that GitPitch slides decks are 100% Git version aware. For public and private repos on GitHub, GitLab, and Bitbucket. This means you can view and/or share any slide deck from any point in time using branch names, tags names, releases names, and commit ids on the slideshow URL. This combined with modular markdown provides a uniquely powerful set of features to create, present, share, and maintain developer slide decks over time.
