# Changelog

## [1.0.5] - 2024-02-19
### Fixed
- SUPPORT_... deprecation warning on startup: https://github.com/docBliny/ha-mysmartblinds/issues/8 Thanks https://github.com/RedsGT !

## [1.0.4] - 2023-06-22

### Changed
- Update smartblinds-client to `v0.7.1`
### Fixed
- Library update fixes functionality

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
