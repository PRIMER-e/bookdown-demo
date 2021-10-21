[![Build Status](https://travis-ci.com/rstudio/bookdown-demo.svg?branch=master)](https://travis-ci.com/rstudio/bookdown-demo)

This is a minimal example of a book based on R Markdown and **bookdown** (https://github.com/rstudio/bookdown). Please see the page "[Get Started](https://bookdown.org/yihui/bookdown/get-started.html)" at https://bookdown.org/yihui/bookdown/ for how to compile this example into HTML. You may generate a copy of the book in `bookdown::pdf_book` format by calling `bookdown::render_book('index.Rmd', 'bookdown::pdf_book')`. More detailed instructions are available here https://bookdown.org/yihui/bookdown/build-the-book.html.

You can find the preview of this example at https://bookdown.org/yihui/bookdown-demo/.

# Record of Changes

  - Run `install.packages("bookdown")` to install the bookdown R package.
  - Run `install.packages(c("bslib", "downlit"))` to allow for epub builds.
  - Run `install.packages("usethis") for some nice utilities.

## GitHub Actions Publishing

Follow the instructions at: <https://orchid00.github.io/actions_sandbox/websites-using-pkgdown-bookdown-and-blogdown.html#deploy-bookdown>

  - Create an empty gh-pages branch.
  - Add a Github Secret EMAIL to the repo conatining a verified email address.
  - Run `usethis::use_github_action(url = "https://raw.githubusercontent.com/ropenscilabs/actions_sandbox/master/.github/workflows/deploy_bookdown.yml")` to create a GitHub action that will build and deploy the site to the gh-pages branch.

  - Change the trigger branch name in "deploy_bookdown.yml" from "master" to "main".
  - Push a commit to trigger the new action.
