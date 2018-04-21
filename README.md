# Mutode [![npm](https://img.shields.io/npm/v/mutode.svg)]() [![npm](https://img.shields.io/npm/dm/mutode.svg)]() [![npm](https://img.shields.io/npm/l/mutode.svg)](LICENSE)

[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com) [![Build Status](https://travis-ci.org/TheSoftwareDesignLab/mutode.svg?branch=master)](https://travis-ci.org/TheSoftwareDesignLab/mutode)  [![Coverage Status](https://coveralls.io/repos/github/TheSoftwareDesignLab/mutode/badge.svg?branch=master)](https://coveralls.io/github/TheSoftwareDesignLab/mutode?branch=master)

Mutation testing for Node.js and JavaScript.

**Mutode** generates mutants (small changes of code) and runs your tests. If the tests fail, it means the mutant was detected and **killed**; if your tests pass, it means the mutant **survived** and your tests can be improved.

Read the thesis proposal [here](https://docs.google.com/document/d/1V6U-ahLq6faCbtP0DtKukzdnsUC2ZBsL1LWEJvkqUiE/edit?usp=sharing)

> "It's like a test for your tests!" - @mappum

> "Higher order testing: automated testing for your unit tests" - @albertomiranda

**Requires Node 8+**

## Install

Globally:

```sh
npm i -g mutode
```

Locally as a dev dependency:

```sh
npm i -D mutode
```

## Use

Globally:

```sh
mutode [options] [paths]
```

Locally with `npx`:

```sh
npx mutode [options] [paths]
```

Locally with a package.json script:

```
{
  ...
  "scripts": {
    "test: "my test command",
    "mutode": "mutode [options] [paths]"
  }
  ...
}
```

**Options**:

```
Usage: mutode [options] [paths]

Options:
  --concurrency, -c  Concurrency of mutant runners         [number] [default: 4]
  --mutators, -m     Specific mutators to load (space separated)
      [array] [choices: "booleanLiterals", "conditionalsBoundary", "increments",
             "invertNegatives", "math", "negateConditionals", "numericLiterals",
              "removeArrayElements", "removeConditionals", "removeFuncCallArgs",
         "removeFuncParams", "removeFunctions", "removeLines", "removeObjProps",
                                          "removeSwitchCases", "stringLiterals"]
  -h, --help         Show help                                         [boolean]
  -v, --version      Show version number                               [boolean]
```

## Docs

- Current supported mutation operators are available [**here**](https://thesoftwaredesignlab.github.io/mutode/module-Mutators.html)
- General documentation is available [**here**](https://thesoftwaredesignlab.github.io/mutode/)

## License
MIT Copyright © Diego Rodríguez Baquero
