# Testing Relative Paths as links in Markdown

This repository is a test to see if using relative paths in markdown links
gets followed correctly when the destination of the link is within the same
Github repository. 

This is mostly a test of Github's markdown parsing.

## The Experiment

This test involves creating a git repository hosted on Github ( This 
repository ).

This repository contains the following structure:
```
.
├── directory01
│   └── README.md
└── directory02
    └── README.md
```

`directory02/README.md` contains a link to `directory01/README.md`.
```
[Link](./directory01/README.md)
```

This is a relative link, as is evident.

## Hypothesis

When pushed to Github, Github should translate this relative link into a full
link `https://github.com/AnurupDey/markdown-link-test/blob/main/directory01/README.md`.

## Result

It was observed that Github indeed does translate relative paths to files in 
the same repository to full hyperlinks when rendering markdown files.
