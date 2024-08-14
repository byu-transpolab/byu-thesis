# byu-thesis Format

## Installing

```bash
quarto use template byu-transpolab/byu-thesis
```
You will then be prompted to give a name for a folder that 
will install the extension and create an example directory that serves 
as a template for your thesis.

## Using

If you already have a quarto document that will serve for your thesis, you 
just need to install the extension. From inside your document folder,

```bash
quarto install byu-transpolab/byu-thesis
```

You can then add the following lines to your `_quarto.yml` file,
alongside any of the format options described below.

```yaml
format:
  byu-thesis-pdf:
    keep-tex: true
    highlight-style: arrow
```

If you encounter any difficulties, please file an issue. I am eager to help.

## Format Options

The following format options are available:

A `customtitle` appears on the second page of the thesis alongside the BYU
Engineering Logo.

```yaml
# On the custom title page, use the same title, but format as you like
customtitle: |
  Exceptional Engineering  Research that Has Taken Too Long
```

The next block defines the layout and degree options. Layout:
  - `simple` has centered text with wide margins on both sides.
  - `fancy` has a wider outside margin, with text shifted to the inside. 
  Footnotes also behave differently.

The `oneside` option will print a PDF where all content is arranged as if printed
on one side of the paper. The `twoside` option will print a thesis with both sides
printed, meaning that the margin shifts and additional blank pages are inserted
so that chapters always start on odd pages. 

Setting `phd` will label the work as a "dissertation" and set the degree to
"Doctor of Philosophy." Setting `ms` will call it a "thesis" and set the degree
to "Master of Science." Using the custom degree field gives additional
customization, for example you might say "Bachelor of Science with University
Honors" for an honors thesis.

```yaml
# Layout options are simple/fancy, oneside/twoside, and masters/phd.
# Leave options blank for defaults.
# Defaults are simple for document style, and masters for degree type.
layout: fancy, oneside, masters
# If your degree is not a PhD or MS, then you can overwrite the degree using 
# the \degree command: \degree{Bachelors of Science}
# degree: Bachelors of Science with University Honors
```

The next set of options concerns the committee and department for your thesis. Note that the `author` fields for the article YAML are not used for putting the student name in. This allows you to have the authorship of your paper be different from your committee.

```yaml
student: Cosmo Cougar
department: Civil and Construction Engineering
# list your chair and any other members of your committee
chair: Norman D. Smith
committee:
  - Mary Q. Scott
  - Steven R. Jones
  - Anna B. Hanna
```

Finally, you can provide a list of keywords and a paragraph of acknowledgments.
This is formatted like an abstract, and can be multiple paragraphs.

```yaml
# Include any keywords you would like for your thesis/dissertation
keywords: 
  - awesome stuff
  - engineering
acknowledgments: | 
  Students should acknowledge funding sources. They may also use the acknowledgment page to express appreciation for the committee members, friends or family who provided support or aided the research, writing or technical aspects of the thesis/dissertation. Acknowledgments should be simple and in good taste.
``` 


