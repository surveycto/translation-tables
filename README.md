# Translation tables for SurveyCTO

This repo contains translations for SurveyCTO components. Each table contains the strings that can appear in the UI, translated into a particular language. Each language needs its own table.

## Table structure

Each translation table is stored as a UTF-8 .csv file with 5 columns:

|Term|Translation|Context|Reference|Comment|
|---|---|---|---|---|
|This is the term ID. This is what is referenced in the code to identify the term, so it must match exactly, and cannot be changed.|This is the translated version of the term. I.e., this is how the text should appear in the current language.|A note to help give more information about where/when this particular term shows up.|We use English as the reference language, so this column will usually contain the English translation of the term (just for reference).|Any other comments that might be helpful.|

## Creating your own tables

If you wish to create your translation table in a new language, here are a few things to keep in mind:

* The only two columns that are required for a valid translation are the first and second columns. When uploading your table to SurveyCTO, the server will check the first column (the *Term* column) to see if it's a valid term ID. If a valid term ID is found, the server will  use the contents of the second column (the *Translation* column) as the translated version of that term.
* The rest of the columns (*Context*, *Reference*, and *Comment*) are provided for convenience to help you while you are creating the translations. You can create as many additional columns as you wish, and they will not cause any issues with SurveyCTO.
* You may re-order the rows as you wish. The row order doesn't matter, as long as your translation remains in the same row as the corresponding term ID.
* It is recommended (but not required) to provide a translation for every single term. If you leave the second column blank for a term, when rendering that term in the UI, SurveyCTO will fall back to using whichever language is set as the default for missing strings.
* Make sure you save your .csv file with UTF-8 encoding. If you're using Microsoft Excel, in the *Save as* dialog box, select "*CSV-UTF-8 (Comma-delimited) (.csv)*" as the file format.
