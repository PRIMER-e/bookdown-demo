[![renderbook](https://github.com/PRIMER-e/bookdown-demo/actions/workflows/deploy_bookdown.yml/badge.svg)](https://github.com/PRIMER-e/bookdown-demo/actions/workflows/deploy_bookdown.yml)

# Record of Changes

## Initial Setup

  - Run `install.packages("bookdown")` to install the bookdown R package.
  - Run `install.packages(c("bslib", "downlit"))` to allow for epub builds.
  - Run `install.packages("usethis") for some nice utilities.
  - Change the LICENSE.

## GitHub Actions Publishing

Follow the instructions at: <https://orchid00.github.io/actions_sandbox/websites-using-pkgdown-bookdown-and-blogdown.html#deploy-bookdown>

  - Create an empty gh-pages branch.
  - Add a Github Secret EMAIL to the repo conatining a verified email address.
  - Run `usethis::use_github_action(url = "https://raw.githubusercontent.com/ropenscilabs/actions_sandbox/master/.github/workflows/deploy_bookdown.yml")` to create a GitHub action that will build and deploy the site to the gh-pages branch.

  - Change the trigger branch name in "deploy_bookdown.yml" from "master" to "main".
  - Add a "build_dir: _book" option to "deploy_bookdown.yml".
  - Rename the GH_TOKEN env variable in "deploy_bookdown.yml" to GITHUB_TOKEN.
  - Move the email setting in "deploy_bookdown.yml" from the "env:" to "with:"
  - Push a commit to trigger the new action.
  - Remove the Travis-CI config files:
    - .travis.yml
    - _build.sh
    - _deploy.sh
    - Dockerfile
    
## Tweaks

  - Remove the unused "_publish.R" re-styling file.
  - Tweak the GitHub Action so it uses the bs4_book output format, including the additional dependencies.
  - Replace the build status badge with one from the GitHub Action.
