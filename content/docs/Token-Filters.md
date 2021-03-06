+++
author = ["Marty Schoch"]
date = "2015-06-23T10:25:38-04:00"
title = "Token Filters"
[menu.docs]
weight = 30
parent = 'analysis'

+++

### Apostrophe

The Apostrophe Token Filter removes all characters after an apostrophe.

### CLD2

The CLD2 Token Filter will take the text from each token and pass it to the [Compact Language Detection 2](https://code.google.com/p/cld2/) library.  Each token is replaced with a new token corresponding to the ISO 639 language code detected.  Input text should already be converted to lower case.

### Edge n-gram

The edge n-gram token filter will compute n-grams just like the n-gram token filter, but all the computed n-grams are rooted at one side (either the front or the back).

### Elision

The elision filter identifies and removes articles prefixing a term and separated by an apostrophe.

For example, in French `l'avion` becomes `avion`.

The elision filter is configured with a reference to a token map containing the articles.

### Keyword Marker

The keyword marker filter will identify keywords and mark them as such.  Keywords are then ignored by any downstream stemmer.

The keyword marker filter is configured with a token map containing the keywords.

### Length

The length filter identifies tokens which are either too long or too short.  There are two parameters, the minimum token length and the maximum token length.  Tokens that are either too long or too short are removed from the token stream.

### Lowercase

The Lowercase Token Filter will examine each input token and map all Unicode letters to their lower case.

### n-gram

The n-gram token filter computes n-grams from each input token.  There are two parameters, the minimum and maximum n-gram length.

### Stemmer

The stemmer token filter takes input terms and applies a [stemming](http://en.wikipedia.org/wiki/Stemming) process to them.

This implementation uses [libstemmer](http://snowball.tartarus.org/).

The supported languages are:

* Danish
* Dutch
* English
* Finnish
* French
* German
* Hungarian
* Italian 
* Norwegian
* Porter
* Portuguese
* Romanian
* Russian
* Spanish
* Swedish
* Turkish

### Stop Token

The Stop Token Filter is configured with a map of tokens that should be removed from the token stream.

### Truncate Token

The truncate token filter truncates each input token to a maximum token length.

### Unicode Normalize

The Unicode normalization filter converts the input terms into the specified [Unicode Normalization Form](http://unicode.org/reports/tr15/).

The supported forms are:

* nfc
* nfd
* nfkc
* nfkd