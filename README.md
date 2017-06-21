# Detroit Ledger Coding and Project Standards

At the Ledger, we work in the open on public-good projects. Our goal is to have our projects documented so that anyone with at least beginner programming knowledge should be able to get any project here running in significantly less than a day. 

## Assumptions

We assume that most people running these projects:
* have basic knowledge of the Unix environment and are familiar with the command line
* have basic knowledge of the project's language (javasacript, python)
* have no clue about what the project does or how to get started. 

We attempt to walk through or link to details on all other concepts where possible. 

## Basics 

**License**

Use the [MIT license](https://github.com/detroitledger/codestandards/blob/master/LICENSE). 

**Readme**

Include a readme that makes it easy for most people to get started with the project quickly. [Use this template](https://github.com/detroitledger/codestandards/blob/master/README-TEMPLATE.md) to get started. Here's a [gold-standard readme](https://github.com/nprapps/liveblog) for reference.

The readme should cover:

1. A few sentences about what the project does
2. Clear, short instructions on how to run the project and what the output should look like
3. Instructions on how anyone can install the project. Be explicit about additional steps and requirements (eg how to install dependencies and where to put configuration options). The instructions should work on OSX and unix-y environments; other platform support is a good bonus.  
4. Add optional sections for developer notes about code organization, tests, and common troubleshooting solutions.

## Code quality

**Javascript**
Use the [eslint config file](https://github.com/detroitledger/codestandards/blob/master/.eslintrc.js) in this repo with [prettier](https://github.com/prettier/prettier) wherever feasible to help keep code consistent. Prettier will automatically format your code on save and alert you to any errors. Packages are available for most major editors. 

**Python**

Use [virtualenv](https://virtualenv.pypa.io/en/stable/) and [virtualenvwraper](https://virtualenvwrapper.readthedocs.io/en/latest/index.html). Start projects with the `--no-site-packages` flag to keep dependencies clean.

Follow [pep8 conventions](https://www.python.org/dev/peps/pep-0008/). Please use a linter to ensure your code looks and works well -- we recommend [pylint](https://www.pylint.org/), which has packages for most major editors. 

We write our code using modern versions whenever possible (eg Python 3.5 and ES6) and note if a tool relies on an older version than the current standard.

## Issues

We track our to-do's and bugs using Github Issues. Anyone can create new issues, suggest feature enhancements or share project-related ideas in our repositories using Issues.

If you're fixing an issue, add it's number to your commit message to automatically close it and more easily reference the solution later. Eg `git commit -m "added unit tests, fixes #3"`

## Collaboration, branches and pull requests

When a repository has multiple contributors who are working at the same time, we work on our own feature branches and then merge working code back into `master` by submitting a pull request. We review each other's pull requests and approve or suggest revisions.
