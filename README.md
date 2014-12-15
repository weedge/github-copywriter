# github-copywriter
[![Build Status](https://travis-ci.org/ryanmjacobs/github-copywriter.svg?branch=master)](https://travis-ci.org/ryanmjacobs/github-copywriter)
[![Gem Version](https://badge.fury.io/rb/github-copywriter.svg)](http://badge.fury.io/rb/github-copywriter)

Updates your copyrights... so you don't have to!

`$ gem install github-copywriter`

### Update specific repos
`$ github-copywriter MyCoolRepo MyOtherCoolRepo`

### Update all repos
`$ github-copywriter --all`

### Update all repos, excluding forks
`$ github-copywriter --all --skip-forks`

### Update all repos to 2015
`$ github-copywriter --all --year 2015`

## Contributing
Please submit issues or feature requests [here](//github.com/ryanmjacobs/github-copywriter/issues).
Questions and comments are welcome as well. Checkout
[CONTRIBUTING.md](//github.com/ryanmjacobs/github-copywriter/blob/master/CONTRIBUTING.md)
for more info.

Feel free to [fork](//github.com/ryanmjacobs/github-copywriter) this project, and:

* fix bugs
* add some sweet features
* implement feature requests
* improve the docs and/or this site

## Under the hood
All GitHub API calls are made with [Octokit](//github.com/octokit/octokit.rb).

####Basic breakdown of the program's logic:
1. Authenticate to GitHub.
2. Loop through each user repo given, and:
    * Update copyrights on files: `README.md`, `LICENSE`, etc.
    * Create a local commit and push to GitHub.
