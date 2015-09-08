# csv-locales

This module creates json files with [i18n locales](https://developer.chrome.com/extensions/i18n) for Google Chrome extensions and applications from a CSV file.


## Installation

    npm install --save csv-locales


## Usage

To create locales use a CSV file which generated from a spreadsheet with [this structure](https://docs.google.com/spreadsheets/d/1ONVyE5iwe7Hjg74eUQ5WdJjQ7i8kWNcbfXI-uh3bvdc/edit?usp=sharing).

You can use it as a [grunt task](https://www.npmjs.com/package/grunt-csv-locales) or as in example below:

    var csvLocales = require('csv-locales');
    
    var params = {
      csvPath: '/absolute/path/to/the/file/locales.csv',
      dirPath: '/absolute/path/to/the/target/dir/_locales',
      csvParse: {/* CSV parser option or null */}
    };
    
    csvLocales(params, function (err) {
      if (err) {
        throw err;
      }
      
      // All done!
    });

### Params available

* `csvPath` - an absolute path to the CSV file with locales.
* `dirPath` - an absolute path to the target directory. If it doesn't exist, it will be created.
* `csvParse` — a list of options for the [CSV parser](http://csv.adaltas.com/parse/).


License
-------

[MIT](LICENSE)
