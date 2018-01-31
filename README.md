# yannesposito.com Source code

I use Hakyll to generate my website.

If you want to use this blog for you.

# INSTALL

1. Clone from my repository.
   The `--depth=1` is highly recommended to make the download far shorter.

        git clone -b empty http://github.com/yogsototh/yblog --depth=1

2. Configure your languages in `Config.hs`
3. Install [`stack`](https://haskellstack.org)
4. Install [`nix`](https://nixos.org/nix/)
5. Start `nix-shell` (only the first time)
6. compile and launch preview

        ./auto-update

## Content Initialization

1. Add an avatar.png image in `Scratch/img/about`
2. You might want to change `Multilang.lhs` inside `trads` to put your own translation.
3. You might want to specify your own abbreviations in `Abbreviations.lhs`.
4. You should remove all my content:

~~~
rm -rf multi/*
rm -rf content/*
~~~

## Adding articles

Create your own entries in `multi` (if you use different languages)
or directly inside Scratch/

Inside multi, the line of your files are filtered the following way.
If you work with three languages (say fr, en and de), then

        This line will appear in all languages
        fr: This line only in French
        en: This line only in English
        de: This line only in Deutch

## Third services configuration

### Google Analytics

Modify the identifier `UA-0000000-1` in `Scratch/js/index.js`

### Disqus

Modify the `disqus_shortname` value in `templates/post.html`.

### Publish to github pages

To publish to github pages, modify the github conf inside `publish.sh` and `fastpublish.sh`.

# Workflow

1. Open a terminal and type `./tools/auto-update`
2. edit content inside Scratch or multi
3. Once happy, `./tools/publish.sh`.
