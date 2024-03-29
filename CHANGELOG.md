# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.5.0] - 2022-12-29

### Added

- Descriptions for options in types.

### Changed

- Use typings for bun v0.4.0
- Updated descriptions for options in README.md
- Will now immediately send a 404 response if the file is not found, instead of redirecting to a normalized path before.
- `handleErrors` option is now `false` by default.

## [0.4.0] - 2022-11-21

### Changed

- Use typings for Bao.js v0.2.x

## [0.3.0] - 2022-10-31

### Changed

- The package is now an ES module instead of CJS.
- The `src/` folder is now included in the npm build.

## [0.2.0] - 2022-08-04

### Added

- [BREAKING] `dotfiles` option with `deny` as default. Your dotfiles will now respond with a 403 by default! No more leaking secrets.
- `defaultMimeType` option. Defaults to `text/plain`. Files that usually responded with `application/octet-stream` will now respond with the `defaultMimeType`, instead of automatically downloading, which was quite weird.

## [0.1.4] - 2022-07-12

### Changes

- Won't look for an index file if the path is not a directory.

## [0.1.3] - 2022-07-12

### Changes

- Use `Bun.file` instead of `node:fs`.

### Removed

- `mime` dependency. Now uses `Bun.file(file).type`!
- `fileEncoding` option is gone, replaced by `charset` only.

## [0.1.1] - 2022-07-12

### Removed

- Source maps

## [0.1.0] - 2022-07-12

### Added

- Initial release
- Support for `Bun.serve`
- Support for `Bao.js`
