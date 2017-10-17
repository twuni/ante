# Ante

Ante is an educational bootstrapping tool for applications and libraries.

> An **ante**, in poker, is a bet that everyone in the game must make in order
> to stay at the table.

We believe in universal standards for software quality. No matter which language
the software is written in, and no matter which platform it is designed to run on,
there are common practices and tools we consider to be **essential**. This is what
we call the "ante".

These essential tools and practices can often be quite difficult to integrate,
and there is little education on their purpose or benefits. The Ante team aims
to close this gap, enabling software professionals veteran and inexperienced
alike to learn (or re-learn) the basics of shipping quality software.

## Our Vision

 * We focus on **aspects** of a healthy project, rather than on specific tools or patterns.

 * We provide **choices** where there are alternative approaches to solving the same problem.

 * We provide **education** on the rationale for each aspect and choice.

 * We provide **unbiased** comparisons when alternatives are available.

## Universal Standards

Ante bootstraps and teaches workflows for many aspects of a software project.

### Build Toolchain

A straight-forward build process is essential to would-be contributors of a project,
and has a direct impact on the day-to-day experience of building software. The build
process should be:

 * **Usable**: Performing a build should be a single command that feels natural.

 * **Predictable**: A build should produce identical artifacts when given identical input, every time.

 * **Lean**: Only perform the necessary tasks to produce working software.

### Dependency Management

All projects either expose some modules for reuse by other projects, consume
modules from other projects, or both. Therefore, it is important to understand
*how* projects integrate in this ecosystem, both as publishers and consumers.

Some important decisions to make include:

 * Will this project have dependencies?
 * What is the process for introducing a new dependency into this project?
   * Are there quality metrics you want to take into consideration?
     * Licensing: Does the project have a license more restrictive than your project? Will it introduce new legal constraints?
     * Documentation: Does the project have useful documentation? How thorough does it need to be?
     * Support: Does the project have a track record of providing its users with good support?
     * Community: Does the project have an active community of contributors? Is it just one person? How many is good enough?
     * Code Quality: Does the code appear to be well structured and readable?
     * Code Quantity: Is the size, on disk, of the project within an acceptable threshold? How much is too large?
     * Test Coverage: Does the project follow healthy automated testing practices? How much coverage is good enough?
     * Reputation: Does the project have a good reputation? How good does it need to be?
     * Popularity: Is the project used by lots of people? How many people is enough?
     * Stability: Does the project change its API rapidly? Will it be difficult to keep up?
 * What is the process for updating an existing dependency in this project?
   * How will you know when updates are available?
   * How will you know what the contents of these updates are?
   * How will you know whether an update will require additional changes in your project?
   * How will you know *when* you should perform the update?
     * Bug fixes and security fixes, for example, should be applied as soon as possible.
     * Additive changes, for example, are not necessary until/unless the additional features are needed.
     * Destructive changes, for example, may not be desired without further refactoring.
 * How will versions of this project be released?
   * A versioning strategy can communicate, to some degree, the *nature* of changes introduced in a release.
   * Release notes and/or change logs can describe the *details* of changes in a release.
   * Cryptographic signing can help others verify the *authenticity* of a release.
   * Cryptographic hashes can help others verify the *integrity* of a release.
   * Publishing the project such that it can be consumed as a dependency in the
     same way that it would consume dependencies, itself, provides *consistency*
     across dependency consumption within the ecosystem.

### Documentation

Documentation enables others to understand a system.

#### API Reference

API reference documentation helps developers understand how to work with a system at a code-level.

#### User Manual

A user manual provides natural-language documentation on how to use a system as an end-user.

### Testing

Tests provide **proof of working software**.

#### Integration Tests

Integration tests assert that two units of a system are compatible with one another.

#### Unit Tests

Unit tests assert that an individual unit of a system behaves as intended.

#### Code Coverage

Code coverage tools help to identify untested behavior within a system.

### Static Analysis

Static analysis is an essential part of any build toolchain.

#### Potential Errors

Static analysis can identify many errors that even code review might miss.

#### Code Style

Static analysis can identify inconsistent code style within a project, and can often even automatically reformat the code to adhere to convention.

> **Note:** We consider code style enforcement to be **non-essential**, but is a highly desired *feature* in many projects.

#### Security

Static analysis can identify potential security vulnerabilities that even code review might miss. If static analysis can find a vulnerability in your code, a human researcher certainly can.

### Vulnerability Scanning / Monitoring

Monitoring or scanning dependencies for known vulnerabilities is an important aspect of security hygiene.

### Publication

A strategy for how a project is published, whether internally or publicly, is important to define early.

### Versioning

A versioning strategy (like [semantic versioning](http://semver.org/)) can provide users of your library or application with a compatibility contract.

### Branching Strategy

Defining a strategy for how branches (in source code management tools like `git`) are managed for a project is very important to define early. This strategy will need to support the team's workflow for integrating their work, and also to support the project's publication/versioning strategy.

### Continuous Build / Integration (CI)

Continuous automated builds of a project provide a universal source of truth for the health of a project.

### Contribution Guidelines

Defining clear guidelines for contribution can help others to contribute more effectively to your project, as well as to provide clear unbiased judgment on whether a contribution (or contributor) is within accordance of these guidelines.

### Code of Conduct

Defining a code of conduct for a project helps the team to work together more effectively, and provide a process for how complaints regarding conduct are handled.

### Licensing

Defining a license for how a system can be used is necessary before others can legally use it.
