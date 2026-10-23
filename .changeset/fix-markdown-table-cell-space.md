---
"@biomejs/biome": patch
---

Fixed [#12542](https://github.com/biomejs/biome/issues/12542): the Markdown formatter no longer drops the space after a word in a table cell when an earlier cell ends with the same word, and no longer pads a column to the width of a column in another table. Both changed the document or gave a different result when formatted again.

```diff
- | a        | b     |
- | -------- | ----- |
- | x        | `y` z |
- | `p` z`q` | r     |
+ | a         | b     |
+ | --------- | ----- |
+ | x         | `y` z |
+ | `p` z `q` | r     |
```
