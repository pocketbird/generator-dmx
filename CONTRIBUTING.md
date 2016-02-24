# Contributing to dmx

### Get Started
1. Clone the repository
2. Make your changes in a topic branch
3. Rebase against `origin/master`, submit a pull request


### Linking dmx
In order to see and test the changes you've made to dmx, you'll need to [uninstall](https://www.npmjs.org/doc/cli/npm-uninstall.html) any previously installed versions of dmx and [link](https://www.npmjs.org/doc/cli/npm-link.html) your local dmx.

1. `npm uninstall -g generator-dmx`
2. `cd path/to/dmx/repo`
3. `npm link`
4. `cd path/to/desired/location`
5. `yo dmx`

The resulting dmx generator will be referencing your local copy of the dmx respository rather than an installed published release.


### Git Commit Messages
- Capitalize your commit messages.
- Start your message with a verb.
- Use present tense.
- Refer to the issue/PR number in your squashed commit message.


### Tagging and Publishing Releases
1. Update the [package version](https://github.com/centresource/generator-dmx/blob/master/package.json#L3) in `package.json`. This should match the version number that you are publishing to [npmjs.org](https://www.npmjs.org/package/generator-dmx).
2. Commit your version bump: `git commit -am "Version bump."`
3. Create an [annoted git tag](http://git-scm.com/book/en/Git-Basics-Tagging#Annotated-Tags) for the release: `git tag -a v#.#.# -m "Version #.#.#"`
4. Push master/tags: `git push origin master --tags`
5. Publish to npm: `npm publish`

**NOTE**: dmx is using [semver](http://semver.org/). Do not break this pattern.
