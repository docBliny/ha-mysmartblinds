# Changelog

## [1.0.3] - 2023-01-27

### Fixed
- Fix login issue due to new My Smart Blinds server change

### Changed
- Bump `mysmartblinds-client` to `0.7.0` and pull from new fork on GitHub (https://github.com/docBliny/smartblinds-client)
- Add depedencies from `mysmartblinds-client` to manifest or Home Assistant won't install the correctly

## [1.0.2] - 2021-12-23
### Fixed
- Added (hacky) check to verify entity has been added to Home Assistant before attempting to update state.

## [1.0.1] - 2021-12-19
### Changed
- (Re-)Added support for `cover.open_cover` and `cover.close_cover` to make it easier to script open/close events
