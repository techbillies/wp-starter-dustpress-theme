# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.0.0] - 2017-08-28

### Added

- No additions.

### Changed

- Rename _fonts.scss to _font-face.scss.
- Fix indentation errors from PHP files.
- Add comments to style files.

### Removed 

- Delete duplicate changelog file.

## [0.0.2] - 2017-08-24

### Added

- Add admin styles and scripts to the theme
- Add a [Modernizr](https://modernizr.com/) config to the theme
- Add acf-fields folder under lib. This is for all acf custom fields that are not component related.
- Add acf-json folder under lib/acf-fields. This is for manually exported json files if someone wants to use them in the admin editor.
- Add pre-commit linting to the theme. This can be commented out from the package.json file. If you want to use the feature, you have to have the needed npm utilities installed globally. 

### Changed

- Modify lib/images to include a sample function that adds and modifies image sizes.
- Modify lib/setup to no longer include the whole style file in to the admin. Instead use the added admin style file.
- Modify style assets to simplify the theme structure.
- Fixed coding style errors from all theme files.

### Removed 

- Remove unnecessary style files and join the style declarations to simplify the assets.
- Remove scss-lint file because the new linter should be the npm package sass-lint.

## [0.0.1] - 2017-07-21

### Added

- All script classes can be accessed statically via the `Theme` instance.
 - For example the global `Common` class is accessible by calling `Theme.Common`.
 - This enables running static functions within script classes!
- A global and static event stopping function under the `Common` class.
 - To stop the default event on event listener callbacks run `Theme.Common.stop(e);`.
- The `Theme` class now runs a function called `init` for all the global scripts and the currently defined template scripts after all scripts are instantiated.
- `$` and `$1` helper functions into the `Common` class. These are neat wrappers for `querySelectorAll` and `querySelector`.
- This awesome CHANGELOD.md file!

### Changed

- The `Theme` class is now required first in the `main.js` file.
 - `Theme` is globally accessible in any scipt file and in inline scipts.
 - For example you can use the `documentHasClass` function globally by calling `Theme.documentHasClass('class-name')`.
- Script files no longer need to be required with the class name in `main.js`.
- Updated documentation for JavaScript development.
