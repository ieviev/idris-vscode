## Unreleased
### Added
### Changed
### Fixed

## 0.0.15
Identical to 0.0.14, just incremented the version to work around issue publishing 14 to to OpenVSX.

## 0.0.14
### Added
### Changed
- Bumped the back-end to 0.1.6, to handle Idris2 0.6.0. 
### Fixed
- Fixed a bug on Windows where it would fail to start the process.
- Fixed error msgs being displayed incorrectly due to a change in how they're reported in Idris2 0.6.0.

## 0.0.13
### Added
- Added the ability to specify additional arguments for the Idris process.
### Changed
### Fixed
- Fixed a bug in Idris v1 mode where it would erroneously show the workspace error message.  

## 0.0.12
### Added
- Add separate commands for :type-of and :type-at. 
### Changed
### Fixed
- Until multiple workspaces are supported, adds an error message. 

## 0.0.11
### Added
- Syntax highlighting for idris/idris2 code blocks in markdown files.
- `Idris: Activate Extension` command, to manually activate when working with non-idris files.
- Support for commands in idris2 blocks in markdown files.
- Load packages from .ipkg file in Idris 1.
### Changed
### Fixed
- Support completions for Idris 1 .lidr files.

## 0.0.10
### Added
- Adds more ide support for .lidr files: hover, diagnostics and most commands.
### Changed
- Updated the IDE process args to handle Idris2 0.4.0, specifically fixes it so it doesn't spew ansi colour codes everywhere.
### Fixed
- Fixed a bug where hover would send erroneous typecheck requests that weren't displayed, but slowed down the process.

## 0.0.9
### Added
### Changed
- Don't try to execute v2 commands if not in v2 mode, show warning instead.
- Stop passing console width flag to Idris 2 proc, as no longer needed.
### Fixed
- Fix bug where VS couldn't insert past end of document.
- Change the function_signature highlighting rule to add fewer scopes, fixing the highlighting of case statements within the signature.

## 0.0.8
### Added
- Added :generate-def command.
- Added :type-at as an option for hover behaviour.
### Changed
- Shorten Idris 2 error message to remove superfluous location information.
### Fixed
- Fix syntax highlighting of nested block comments.

## 0.0.7
### Added
### Changed
- Trim leading `?` so hover can show types of metavariables.
- Bump idris-ide-client version to 0.1.4, which has better Idris 2 support.
### Fixed
- Fix a bug where extension would prompt for reload on _any_ config change.
- Workaround a bug in Idris 2 where it would mangle messages based on a mis-inferred terminal width.

## 0.0.6
### Added
### Changed
- Added a warning when load file fails in Idris2 because of errors.

### Fixed
- Fixed a bug that could lead to incorrect paths in the diagnostic URIs.

# 0.0.5
### Added
- Added a config flag to enable Idris 2 mode.
- Added a config option to turn off the hover behaviour.
- Added a warning for trying to call Version from Idris 2.

### Changed
- Bump dev dependencies to appease our dependabot overlords

### Fixed
- Fix hover text in inappropriate contexts (https://github.com/meraymond2/idris-vscode/issues/1)
- Fixed a bug in the text-mate highlighting where it didn’t handle all of the possible bracket types after backticks.
- Fixed a bug where the diagnostics didn't work with Idris 2.
- Fixed a bug where Idris 2 wouldn't find the ipkg file, and complain about module names (https://github.com/meraymond2/idris-vscode/issues/12).

# 0.0.4
### Added
- Support for .ipkg and .lidr syntax highlighting

### Changed
- Improved the regex syntax highlighting
- Updated dev dependencies for security

### Fixed
- Fixed an invisible bug where it would try to get the type of the whole document when hovering over a space
