# Contributing

Contributions are always welcome. Before contributing please read the
[code of conduct](https://github.com/newrelic/.github/blob/main/CODE_OF_CONDUCT.md) and [search the issue tracker](issues); your issue may have already been discussed or fixed in `main`. To contribute,
[fork](https://help.github.com/articles/fork-a-repo/) this repository, commit your changes, and [send a Pull Request](https://help.github.com/articles/using-pull-requests/).

Note that our [code of conduct](https://github.com/newrelic/.github/blob/main/CODE_OF_CONDUCT.md) applies to all platforms and venues related to this project; please follow it in all your interactions with the project and its participants.

## Feature Requests

Feature requests should be submitted in the [Issue tracker](../../issues), with a description of the expected behavior & use case, where they’ll remain closed until sufficient interest, [e.g. :+1: reactions](https://help.github.com/articles/about-discussions-in-issues-and-pull-requests/), has been [shown by the community](../../issues?q=label%3A%22votes+needed%22+sort%3Areactions-%2B1-desc).
Before submitting an Issue, please search for similar ones in the
[closed issues](../../issues?q=is%3Aissue+is%3Aclosed+label%3Aenhancement).

## Pull Requests

1. Ensure any install or build dependencies are removed before the end of the layer when doing a build.
2. Increase the version numbers in any examples files and the README.md to the new version that this Pull Request would represent. The versioning scheme we use is [SemVer](http://semver.org/).
3. You may merge the Pull Request in once you have the sign-off of two other developers, or if you do not have permission to do that, you may request the second reviewer to merge it for you.

## Contributor License Agreement

Keep in mind that when you submit your Pull Request, you'll need to sign the CLA via the click-through using CLA-Assistant. If you'd like to execute our corporate CLA, or if you have any questions, please drop us an email at opensource@newrelic.com.

For more information about CLAs, please check out Alex Russell’s excellent post,
[“Why Do I Need to Sign This?”](https://infrequently.org/2008/06/why-do-i-need-to-sign-this/).

Contributions are always welcome. Before contributing please read the
[code of conduct](https://github.com/newrelic/.github/blob/main/CODE_OF_CONDUCT.md) and [search the issue tracker](issues); your issue may have already been discussed or fixed in `main`. To contribute,
[fork](https://help.github.com/articles/fork-a-repo/) this repository, commit your changes, and [send a Pull Request](https://help.github.com/articles/using-pull-requests/).

Note that our [code of conduct](https://github.com/newrelic/.github/blob/main/CODE_OF_CONDUCT.md) applies to all platforms and venues related to this project; please follow it in all your interactions with the project and its participants.


## Slack

We host a public Slack with a dedicated channel for contributors and maintainers of open source projects hosted by New Relic.  If you are contributing to this project, you're welcome to request access to the #oss-contributors channel in the newrelicusers.slack.com workspace.  To request access, see https://newrelicusers-signup.herokuapp.com/.

## Testing
### Functional Testing
The plugin includes a suite of functional tests which should be used to
verify your changes don't break existing functionality.

Functional tests are stored in the `test` directory.

Running the test suite is simple.  Just invoke:
```
    npm install
    npm test
```

This will run the tests in standalone mode, executing the test suite.
### Unit Testing
The plugin includes unit testing that is stored in the `tests` directory. 

Our testing makes use of [cordova-paramedic](https://github.com/apache/cordova-paramedic) to run our tests in a test app in an emulator. The npm version of cordova-paramedic is out of date, so it is preferred to install it using GitHub. To install it, run:
```
    npm install -g github:apache/cordova-paramedic
```
Once it is installed, you will be able to run tests for each individual platform.
```
    npm run test:android
    npm run test:ios
```
If you run into issues on iOS side, you might have to restart your emulator. 


### Writing Tests

For most contributions it is strongly recommended to add additional tests which
exercise your changes.

This helps us efficiently incorporate your changes into our mainline codebase
and provides a safeguard that your change won't be broken by future development.

There are some rare cases where code changes do not result in changed
functionality (e.g. a performance optimization) and new tests are not required.
In general, including tests with your pull request dramatically increases the
chances it will be accepted.