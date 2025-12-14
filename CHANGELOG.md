# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.1.2] - 2025-12-14

### Fixed

* Fixed a command injection vulnerability via the `manifest-path` input parameter.

    The code was using GitHub action templates to inject the value directly into the shell command, which does not perform the necessary escaping.
    For fixing the issue, the value is passed via an environment variable, which performs the proper escaping.
    This is only an issue if the `manifest-path` parameter was set from some other untrusted source.
    Using a static string to call the action is safe.

    Thanks to @mleblebici for reporting and fixing the issue.

## [1.1.1] - 2024-10-01

### Fixed

* Parse the new rustfmt file and line number format

    The format changed in https://github.com/rust-lang/rustfmt/pull/5971

    Thanks to @0xcypher02 for pointing out the problem.

## [1.1.0] - 2022-11-21

### Added

* Add the input `manifest-path` to set the `--manifest-path` argument of rustfmt. #1
    This allows formatting any cargo project in the repository independent of the location.

## [1.0.1] - 2022-10-13

### Changed

* Switch from set-output to $GITHUB_OUTPUT to avoid warning
    https://github.blog/changelog/2022-10-11-github-actions-deprecating-save-state-and-set-output-commands/

## [1.0.0] - 2022-07-19

Initial Version
