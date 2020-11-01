<a href="https://photon-platform.net/">
    <img src="https://photon-platform.net/user/images/photon-logo-banner.png" alt="photon" title="photon" align="right" height="120" />
</a>


# photon ✴ Search

## 0.1.0

---


> extension of TNT search

- [configuration](#configuration)
- [templates](#templates)
- [scaffolds](#scaffolds)
- [scss](#scss)
- [assets](#assets)
- [languages](#languages)

# configuration
blueprints.yaml

fields:
- enabled
- built_in_css
- built_in_js

Before configuring this plugin, you should copy the `user/plugins/photon-search/photon-search.yaml` to `user/config/plugins/photon-search.yaml` and only edit that copy.

Here is the default configuration and an explanation of available options:

```yaml
enabled: true
built_in_css: true
built_in_js: true

description: Custom Text added by the **photon-search** plugin (disable plugin to remove)
```

Note that if you use the admin plugin, a file with your configuration, and named photon-search.yaml will be saved in the `user/config/plugins/` folder once the configuration is saved in the admin.


# blueprints

```sh
blueprints
├── search.yaml
└── taxonomy.yaml
```

### Taxonomy
taxonomy.yaml
extends: article
fields:
- taxonomy
  - header.content.items

### Search
search.yaml
extends: article
fields:
- header.search
  - .notes

# templates

```sh
templates
├── _articles
│   ├── categories.html.twig
│   ├── tags.html.twig
│   └── taxonomy.html.twig
├── search
│   ├── tntquery-ajax.html.twig
│   └── tntsearch.html.twig
├── categories.html.twig
├── search-2.html.twig
├── search.html.twig
├── tags.html.twig
├── taxonomy.html.twig
└── tntquery-ajax.html.twig
```

# scss

```sh
scss
├── articles
│   └── _search.scss
├── templates
│   ├── _search.scss
│   └── _taxonomy.scss
└── search.scss
```

# assets

```sh
assets
├── search.css
├── search.css.map
├── search.js
├── tntsearch.css
└── tntsearch.js
```

# languages

```sh
languages
└── en.yaml
```


## Installation

- all photon plugins are installed as git submodules. More on that later.



## Configuration


## Usage

Select template type when creating a new page

## Credits


## To Do

- [ ] Future plans, if any


copyright &copy; 2020
