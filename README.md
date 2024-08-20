# js-levenshtein

A slight modification of a very efficient JS implementation calculating the Levenshtein distance, i.e. the difference between two strings, modified for use in the browser.

Based on Wagner-Fischer dynamic programming algorithm, optimized for speed and memory
 - use a single distance vector instead of a matrix
 - loop unrolling on the outer loop
 - remove common prefixes/postfixes from the calculation
 - minimize the number of comparisons
 - always allocate a new distance vector in order to not leak memory
 
## Install

Download the JS file, and place it into the source files of your website. I might try to get this added to some CDNs.

## Usage

```html
<script>
import levenshtein from "/path/to/levenshtein.js";
levenshtein('kitten', 'sitting');
//=> 3
</script>
```

## License

MIT © Steve0Greatness
