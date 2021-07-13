## Program Notes written for the University of Rochester Orchestras

[Index](./docs/index.html) 

---
### Workflow
1. `git mv ../notes/Chavez_Toccata.txt Chavez_Toccata.md`
2. vim Chavez_Toccata.md (see notes below)
3. vim index.md
4. git add index.md Chavez_Toccata.md
5. git commit -m"Chavez"
6. git push

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
* vim :set fileencoding=utf-8
* `bundle exec jekyll serve` to check for build fails due to non-replaced unicode characters.
* see site at https://jsundram.github.io/program-notes/

### Unsolved
* having some problems getting &rcarom; to render properly; ended up using `&#345;` instead. added `kramdown: input: GFM` to _config.yml didn't seem to make a difference, even with `gfm_quirks: [no_auto_typographic]`

---
You can use the [editor on GitHub](https://github.com/jsundram/program-notes/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

---
### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/jsundram/program-notes/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
