# Be2bill Merchant API guidelines

This document references the guidelines to implement and package the Be2bill API in different programming languages.

#### Table of Contents

1. [Code] (#code)
2. [Tests] (#tests)
3. [Documentation] (#documentation)
4. [Packaging] (#packaging)
5. [Security] (#security)
5. [Contact] (#contact)

## Code
The implementation should remain as close as possible to the PHP one for the public method API.
See: [PHP Merchant API] (http://github.com/be2bill/php-merchant-api).

This point will ensure an easy documentation process for the Be2bill team.
This is not a mandatory point but to keep a good consistency between all implementations, it would be great to have some similar-looking cross-languages API.

Some programming languages will sometime have restrictions (hard types, non-object paradigm ...). These restrictions should be
  managed on a case by case basis.
You should contact the [technical team] (#contact) to debate on the best compromises.

The implemented code shall remain as clean and readable as possible. Please try to respect your programming language's
 best practices and paradigms.

Some programming languages are used to propose some kind of formalism (RFC). It is a good practice to follow the popular RFC in terms of source code formatting and packaging.

The code has to be written in English.

## Tests

It is a required and very important point to deliver an automated test suite with the implementation.
Ideally, there should be at least two kinds of test suite: unit tests and more functional tests.

- Unit tests will respect the unit testing rules: [A set of unit testing rules] (http://www.artima.com/weblogs/viewpost.jsp?thread=126923)
- Functional tests should be implemented on the Be2bill's sandbox environment to prove that the implementation actually works.

Please consider using TDD while implementing the unit test part.

__Note: Do not include your production or sandbox credentials in the repository (please keep in mind that if you
  committed them once, they may still be tracked in the git history)__
## Documentation

Your implementation should be documented.

The required documentation should be composed of:

- A main documentation page (how to deploy, how to use, limitations ...)
- In-code documentation (like javadoc, phpdoc or your programming language documentation system)
- Code examples (a simple directlink payment, a form payment, a refund ...)


This documentation should be kept up to date and at least cover the public interface of your implementation.

The documentation and the commit messages have to be written in English.

## Packaging

The packaging shall contain the following :

- Installation / compilation / configuration / deployment notes
- Guidelines to run the test suite
- Code examples (at least a form and a directlink transaction) see [documentation] (#documentation)
- A packaging system ([composer] (https://getcomposer.org/), [pypy] (http://pypy.org), ...)
  or a description of the package dependencies (test suite tools, libraries)
- A licence file
- A contact information for some eventual bug/security issues (see [security] (#security) section)

## Security

As a payment library, security should be considered with attention.

__Note: Do not store on any mechanism (storage, database, cache ...) any sensible data.__

See [the PCI-DSS standard] (https://pcisecuritystandards.org/minisite/en/) for more information.

As a rule of thumb, you should never log, store (...) the card number, cryptogram or expiration date.

You have to provide a technical contact able to fix some potential security issues.

Note: in order to be integrated in the official Be2bill repository, an exhaustive code review will be made by our technical team

__Note: Do not include your production or sandbox credentials in the repository (please keep in mind that if you
  committed them once, they may be still tracked in the git history)__

## Contact

For any questions, please contact developers@be2bill.com