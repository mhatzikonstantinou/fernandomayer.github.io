# Academic personal pages

This repository hosts the source code to build an academic personal page
based on the [academic theme][1] for [Hugo][2]. The pages are created
with Rmarkdown (`.Rmd`) files and converted to markdown (`.md`) with the
R package [**knitr**][3].

# Usage

## Installation requirements

You must have Hugo installed on your system. In most Linux
distributions, it may already be available through your package manager.
If it is not, follow the instructions on the Hugo website.

You will also need the latest version of R and the latest version of
knitr, which can be installed as follows:


```r
library(devtools)
install_github("yihui/knitr")
```

## Building from scratch

To build a site from scratch with Hugo, you can simply run:


```sh
hugo new site <mysite>
```

where `<mysite>` will be the container of the source files for your
site. Then `cd mysite`. By default there will be no theme preloaded, so
you will have to pick one from [here][4]. As we are using the academic
theme, the "installation" would be done by cloning the git repository of
the theme:


```sh
git clone https://github.com/gcushen/hugo-academic.git themes/academic
```

To have an example structure of a complete webpage, simply copy the
`exampleSite` folder:


```sh
cp -av themes/academic/exampleSite/* .
```

Then start Hugo server with


```sh
hugo server --watch
```

and open your browser at `localhost:1313` to see the website. Every time
you edit and save a file from this structure, the pega is automaticaly
refreshed.

## Forking this repository

You may jump all the steps above by forking this repository and editing
the content as you need.
