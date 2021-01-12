# Coursera Notes Converter

Simple tool to convert notes taken in a Coursera course to CSV or JSON formats.

## Getting started

1. Open the Coursera course, go to the ''Notes'' section and save the page as a complete HTML using any browser.
2. Select a section from the selection box . By default is not allowed to convert all notes (`All notes` option).
3. Run: `./courseranotesconverter -i input.html -o output.json`

## Usage

```text
 usage: courseranotesconverter [-h] --input INPUT --output OUTPUT [--tags TAGS]
                               [--reference REFERENCE] [--force_all_notes]
                               [--no_location_field] [--format FORMAT]
 
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
   --no_location_field   Exclude 'location' field (default: False)
   --format FORMAT       Output format (json or csv) (default: json)
```

## JSON format

```json
[
{
"title": "<Course topic>: <Lesson name> <Note 1 location>",
"tags" : "<--tags option value>",
"text" : "<Note 1>",
"original-text" : "<Highlighted text from the lesson>",
"reference" : "<--reference option value>",
"location-topic" : "<Course topic>",
"location-lesson" : "<Lesson name>",
"location-mark" : "<Note 1 location mark>",
"location-full" : "<Course topic>: <Lesson name> <Note 1 location mark>",
"location" : "[[<Course topic>: <Lesson name> <Note 1 location mark>]]"
},
{
"title": "<Course topic>: <Lesson name> <Note 2 location>",
"tags" : "<--tags option value>",
"text" : "<Note 2>",
"original-text" : "<Highlighted text from the lesson>",
"reference" : "<--reference option value>",
"location-topic" : "<Course topic>",
"location-lesson" : "<Lesson name>",
"location-mark" : "<Note 2 location mark>",
"location-full" : "<Course topic>: <Lesson name> <Note 2 location mark>",
"location" : "[[<Course topic>: <Lesson name> <Note 2 location mark>]]"
},
{
"title": "<Course topic>: <Lesson name> <Note 3 location>",
"tags" : "<--tags option value>",
"text" : "<Note 3>",
"original-text" : "<Highlighted text from the lesson>",
"reference" : "<--reference option value>",
"location-topic" : "<Course topic>",
"location-lesson" : "<Lesson name>",
"location-mark" : "<Note 3 location mark>",
"location-full" : "<Course topic>: <Lesson name> <Note 3 location mark>",
"location" : "[[<Course topic>: <Lesson name> <Note 3 location mark>]]"
}
]
```

## Using to import Coursera notes into TiddlyWiki5

1. Generate a JSON file following the "Getting Started" steps. Optionally add `--tags` option to add tags to the tiddlers.
2. Import the generated JSON using TiddlyWiki importer.
