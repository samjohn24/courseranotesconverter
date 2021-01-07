# Coursera Notes Converter

Simple tool to convert notes taken in a Coursera course to CSV or JSON formats.

## Usage

1. Open the Coursera course, go to the ''Notes'' section and save the page as a complete HTML using any browser.
2. Select a section from the selection box . By default is not allowed to convert all notes (`All notes` option).
3. Run: `./courseranotesconverter -i input.html -o output.json`

## More options

```text
 usage: courseranotesconverter [-h] --input INPUT --output OUTPUT [--tags TAGS]
                               [--reference REFERENCE] [--force_all_notes]
                               [--no_location_brackets] [--format FORMAT]
 
 optional arguments:
   -h, --help            show this help message and exit
   --input INPUT, -i INPUT
                         Input file (.html) (default: None)
   --output OUTPUT, -o OUTPUT
                         Output file (.json) (default: None)
   --tags TAGS, -t TAGS  String to be added to the field 'tags' (default: None)
   --reference REFERENCE, -r REFERENCE
                         String to be added to the field 'reference' (default:
                         None)
   --force_all_notes     Force 'All notes' conversion (default: False)
   --no_location_brackets
                         Remove brackets in 'location' field (default: False)
   --format FORMAT       Output format (json or csv) (default: json)
```



