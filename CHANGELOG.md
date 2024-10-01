# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

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
