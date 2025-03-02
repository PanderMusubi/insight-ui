# Insight UI

A Dash blockchain explorer web application service for [Dashcore Node](https://github.com/dashpay/dashcore-node) using [Insight API](https://github.com/dashpay/insight-api).

## Quick Start

Please see the guide at [https://bitcore.io/guides/full-node](https://bitcore.io/guides/full-node) for information about getting a block explorer running. This is only the front-end component of the block explorer, and is packaged together with all of the necessary components in [Dashcore](https://github.com/dashpay/dash).

## Getting Started

To manually install all of the necessary components, you can run these commands:

```bash
npm install -g @dashevo/dashcore-node
dashcore-node create mynode
cd mynode
dashcore-node install @dashevo/insight-api
dashcore-node install @dashevo/insight-ui
dashcore-node start
```

Open a web browser to `http://localhost:3001/insight/`

## Development

To run Insight UI Dash locally in development mode:

Install dependencies:

```
$ npm install
```

To download bower dependencies, compile and minify the web application's assets:

```
$ npm run build
```

There is a convenient Gruntfile.js for automation during editing the code

```
$ npm run watch
```

## Multilanguage support

Insight UI Dash uses [angular-gettext](http://angular-gettext.rocketeer.be) for multilanguage support.

To enable a text to be translated, add the ***translate*** directive to html tags. See more details [here](http://angular-gettext.rocketeer.be/dev-guide/annotate/). Then, run:

```
npm run build
```

This action will create a template.pot file in ***po/*** folder. You can open it with some PO editor ([Poedit](http://poedit.net)). Read this [guide](http://angular-gettext.rocketeer.be/dev-guide/translate/) to learn how to edit/update/import PO files from a generated POT file. PO file will be generated inside po/ folder.

If you make new changes, simply run **grunt compile** again to generate a new .pot template and the angular javascript ***js/translations.js***. Then (if use Poedit), open .po file and choose ***update from POT File*** from **Catalog** menu.

Finally changes your default language from ***public/src/js/config***

```
gettextCatalog.currentLanguage = 'es';
```

This line will take a look at any *.po files inside ***po/*** folder, e.g.
**po/es.po**, **po/nl.po**. After any change do not forget to run ***grunt
compile***.


## Note

For more details about the [Insight API](https://github.com/dashpay/insight-api) configuration and end-points, go to [Insight API GitHub repository](https://github.com/dashpay/insight-api).

## Contribute

Contributions and suggestions are welcomed at the [Insight UI Dash GitHub repository](https://github.com/dashpay/insight-ui).


## License
(The MIT License)

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
