[![Build Status](https://dev.azure.com/chefcorp-partnerengineering/Chef%20Base%20Plans/_apis/build/status/chef-base-plans.flex?branchName=master)](https://dev.azure.com/chefcorp-partnerengineering/Chef%20Base%20Plans/_build/latest?definitionId=69&branchName=master)

# flex

Flex is a fast lexical analyser generator. It is a tool for generating programs that perform pattern-matching on text.  See [documentation](https://github.com/westes/flex)

## Maintainers

* The Core Planners: <chef-core-planners@chef.io>

## Type of Package

Binary package

### Use as Dependency

Binary packages can be set as runtime or build time dependencies. See [Defining your dependencies](https://www.habitat.sh/docs/developing-packages/developing-packages/#sts=Define%20Your%20Dependencies) for more information.

To add core/flex as a dependency, you can add one of the following to your plan file.

##### Buildtime Dependency

> pkg_build_deps=(core/flex)

##### Runtime dependency

> pkg_deps=(core/flex)

### Use as Tool

#### Installation

To install this plan, you should run the following commands to first install, and then link the binaries this plan creates.

``hab pkg install core/flex --binlink``

will add the following binaries to the PATH:

* /bin/lex
* /bin/flex
* /bin/flex++

#### Using an example binary

You can now use the binary as normal.  For example:

``/bin/flex --help`` or ``flex --help``

```bash
$ flex --help
Usage: flex [OPTIONS] [FILE]...
Generates programs that perform pattern-matching on text.

Table Compression:
  -Ca, --align      trade off larger tables for better memory alignment
  -Ce, --ecs        construct equivalence classes
  -Cf               do not compress tables; use -f representation
...
...
```
