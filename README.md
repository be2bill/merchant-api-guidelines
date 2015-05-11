# Be2bill Merchant API guidelines

This document reference the guidelines to implement and package Be2bill API in different languages

#### Table of Contents

1. [Code] (#code)
2. [Tests] (#tests)
3. [Documentation] (#documentation)
4. [Packaging] (#packaging)
5. [Security] (#security)
5. [Contact] (#contact)

## Code
The implementation shall remain as close as possible that the PHP one for the public method API. See: [PHP Merchant API] (http://github.com/be2bill/php-merchant-api)
  This point will ensure an easily documentation process for the Be2bill team.

Some programming languages will sometime have restrictions (hard typage, non object paradigm ...). These restrictions should be
  managed case by case. You should contact the [technical team] (#contact) to debate on the best compromises.

The implemented code shall remain as clean and readable as possible. Please try to respect your programming language's
 best practices and paradigms.

Some programming languages use to propose some kind of formalism (RFV). It is a good practice to follow the popular RFC in term of source code formatting and packaging.

## Tests

It is a required and very important point to deliver an automated test suite with the implementation.
Ideally, they should be at least two kinds of test suite: unit tests and more functional tests.

- Unit tests will respect the unit testing rules: [A set of unit testing rules] (http://www.artima.com/weblogs/viewpost.jsp?thread=126923)
- Functional tests should be implemented on the Be2bill's sandbox environment to prove that the implementation is really working.

Please consider using TDD while implementing the unit test part.

__Note: do not include your production or sandbox credentials into your package__

## Documentation

Your implementation should be documented.
The required documentation should be composed of
- a main documentation page with some using examples
- some in code documentation (like javadoc, phpdoc or your programming language documentation system)

This documentation should be kept up to date and at least cover the public interface of your implementation.

## Packaging

The packaging shall contains the following things :

- Installation / compilation / configuration / deployment notes
- Guidelines to run the test suite
- Code examples (at least a form and a directlink transaction)
- A packaging system ([composer] (https://getcomposer.org/), [pypy] (http://pypy.org), ...)
  or a description of the package dependencies (test suite tools, libraries)
- A license file
- A contact information for some eventual bug/security issues (see [security] (#security) section)

## Security

As a payment library, security should be considered with attention.
__Do not store on any mechanism (storage, database, cache ...) any sensible data.__
 See [https://pcisecuritystandards.org/minisite/en/] for more information.
 As a rule of thumb, you should never log, store (...) the card number, cryptogram or expiration date.

You have to provide a technical contact able to fix some eventual security issues.

Note: in order to be integrated in the official Be2bill repository, an exhaustive code review will be made by our technical team

__Note: Do not include your production or sandbox credentials in the repository__

## Contact

In case of any questions please contact developers@be2bill.com