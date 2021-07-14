## Program Notes written for the University of Rochester Orchestras

[Index](./docs/index.html) 

---

### Workflow

1. `git mv ../notes/Chavez_Toccata.txt Chavez_Toccata.md`
2. vim -p Chavez_Toccata.md index.md (see notes below)
3. git add index.md Chavez_Toccata.md
4. git commit -m"Chavez"
5. git push

### Notes:
* index.md - link to .html files (they don't exist but will be created).
* two spaces at end of line to get a line break
* convert unicode to entities 
  * em-dash &mdash;
  * en-dash &ndash;
  * r circumflex Dvo&rcaron;&aacute;k
  * find unicode characters: `/[^\x00-\x7F]` and convert to html entities, e.g. o with umlaut &ouml;)
      * https://dev.w3.org/html5/html-author/charref)
* fix screwed up apostrophes in vim `:%s/\%x92/\'/g` (from [here](https://stackoverflow.com/questions/430554/vim-how-do-i-search-for-a-xx-single-byte-representation))
* move italics from `<I></I>` to markdown syntax: `:%s#<I>#\*#g` and `:%s#</I>#\*#g`
* vim `:set fileencoding=utf-8`
* `bundle exec jekyll serve` to check for build fails due to non-replaced unicode characters.
* preview site locally http://localhost:4000/docs/
* look at final result (once pushed and built) at https://jsundram.github.io/program-notes/

### Unsolved
* having some problems getting &rcarom; to render properly; ended up using `&#345;` instead. added `kramdown: input: GFM` to _config.yml didn't seem to make a difference, even with `gfm_quirks: [no_auto_typographic]`

