<p align="center">
<img width="60%" src="https://raw.githubusercontent.com/mdzk-rs/mdzk/main/public/mdzk_logo.png">
</p>

<h2 align="center">A lovingly designed system and static publishing tool for your plain text Zettelkasten</h2>

<p align="center"><a href="https://mdzk.app">Homepage</a> - <a href="https://mdzk.app/docs/Installation">Installation</a> - <a href="https://mdzk.app/docs">Documentation (WIP)</a></p>

mdzk is a plain text Zettelkasten system that is based on the mdBook API. It consists of specialized preprocessors for handling key features such as wikilinks, backlinks and front matter, all tied together in the mdzk CLI. mdzk allows you to use whatever text editor you prefer - be it Obsidian, Vim, Visual Studio Code or even Notepad. You can view your notes with live updating as you edit them, have them automatically published to GitHub Pages on push and much more.

<!-- Keeping this for future reference -->
<!-- These characters are disallowed in note filenames: `=`, <code>\`</code>, `^`, `#`, `|`, `:`, `/`, `[` and `]`. -->

## Include-only builds

This fork has been hacked up (by someone who doesn't know Rust, no less) to only include files in the build that are explicitly listed in `mdzk.toml`.

So, if you have an `mdzk.toml` like this:

    [mdzk]
    authors = ["Jim Kang"]
    ignore = []
    include = [
      "Unrar",
      "Tengen",
      "web-layout"
    ]
    language = "en"
    multilingual = false
    src = "."
    title = "Omniwiki"

It will only make html files for `Unrar.md`, `Tengen.md`, and `web-layout.md`. It will automatically ignore all of the other files in the Markdown source root dir.
