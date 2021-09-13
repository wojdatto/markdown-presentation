# Markdown presentation

A presentation on Markdown written in Markdown.

## Build

### VS Code

You need to install [marp
extension](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode),
and it enables you to export the presentation using _Export Slide Deck_
command.

However, you need to set `"markdown.marp.breaks": "off"` to render the
presentation correctly.

### marp-cli

To build from CLI, [marp-cli](https://github.com/marp-team/marp-cli)
needs to be installed (e.g. you can use one of the released [standalone
executables](https://github.com/marp-team/marp-cli/releases)).

You need to execute export command from the repo root for the [config
file](.marprc.yaml) to be automatically found. Or use a [`--config-file`
option](https://github.com/marp-team/marp-cli#configuration-file)
instead.

Without the config file, the presentation won't render correctly. I wrap
lines at 72 characters and, by default, marp creates a `<br>` when
breaking a line. The config file turns this off.

To export a PDF:

    marp --pdf --allow-local-files src/main.md

Without `--allow-local-files`,
[markdown-logo.svg](src/img/markdown-logo.svg) image won't be embedded
in the PDF. This option has its security concerns, more on that
[here](https://github.com/marp-team/marp-cli/pull/10#user-content-security).
Marp team generally recommends using online image hosting and providing
URLs for images rather than placing the image files in the repo.

HTML export is the default option:

    marp src/main.md

A single HTML file will be created, and unlike PDF images won't be
included in the export. In this presentation, I use GitHub CDN for the
image hosting (excluding
[markdown-logo.svg](src/img/markdown-logo.svg)), so HTML version will
display images as long as you have a connection to the internet.
[markdown-logo.svg](src/img/markdown-logo.svg) will not display, if you
change the relative path to the image (i.e. you move the file to a
different folder).

HTML supports animations for bullet points and a presenter window, so it
might be a better choice.

## License

> Copyright 2021 Tomasz Wojdat
>
> This work is licensed under a Creative Commons Attribution 4.0
> International License.
>
> You should have received a copy of the license along with this work.
> If not, see <http://creativecommons.org/licenses/by/4.0/>.
