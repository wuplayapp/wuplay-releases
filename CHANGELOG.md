# Changelog

### Note: Discord is up at https://discord.gg/CwkVahJQb2

## v0.2.2-beta

### Added
- Voice search support for non-Gboard keyboard users
- Redesigned My Lists screen with a setting to switch back to the original design
- Frame rate matching — automatically switches the display refresh rate to match video content (configurable in Playback settings)
- Episode information on continue watching row for series

### Fixed
- Titles were updating their last watched timestamp prematurely

## v0.2.1-beta

### Added
- Subtitle and Audio track preferred language support for Telugu, Croatian, Serbian and Bosnian languages (user requested)
- Long-press menu item on episode cards to start over an episode that is currently in progress
- Ability to change subtitle size and vertical position
- Long-press menu item on episode cards to manually select a stream when autoplay is enabled
- Setting to bypass or show the "Who's Watching" screen on app start
- Default watch list (Favorites) created on new profile creation

### Changed
- Remote back button out of navigation drawer now directly exits the app instead of dropping into the "Who's Watching" screen
- Internal scrobbling system changes to more accurately track TV series
- Restructured parts of the settings screen
- Refactored portions of the focus system to eliminate occasional focus loss experienced by some users

### Fixed
- Play progress was being inaccurately created for titles that were never actually played
- Completed series were still showing in the continue watching row

## v0.2.0-beta

### Added
- Continue watching row now bypasses the detail screen and goes straight to the player which then honors autoplay setting behavior
- Meta caching for library items to reduce calls to meta addons
- Clear progress option in episode card long-press context menu
- Long-press on Play, Resume, and Start Over buttons to display the stream picker even when autoplay is enabled
- Enhanced support for TMDB addon
- Localization support for English, Spanish, Portuguese, French, German, Italian, Russian, Dutch, Polish, Turkish, and Hindi — more languages available on request

### Changed
- Returning to the app after exiting with the back button now skips the "Who's Watching" screen and goes directly to the home screen for the last active profile
- Refactored home screen catalog loading to improve speed for slow meta addons
- Creating a new profile now drops you into the home screen instead of the "Who's Watching" screen

### Fixed
- Accidentally exiting the app when pressing D-pad left
- HTML-encoded characters not displaying properly

## v0.1.3-beta

### Added
- Skip forward and skip back buttons on supported remotes

### Changed
- Minor UI adjustments

### Fixed
- Pin protection could be bypassed on app resume
- Several bugs related to non-English subtitles
- App crash when watching series with a large number of seasons
- Subtitle selection now persists across stream restarts
- Episodes and seasons could not be marked as unwatched

## v0.1.2-beta

### Added
- Support for Android TV 9 (Pie) and above (previously required Android TV 11+)

### Changed
- Poster rows use skeleton cards as loading indicators and to prevent screen jumping

### Fixed
- Non-English metadata was displayed as English
- Cast and crew returned no results
- Misc focusing system issues
- Black screen when trying to exit the app with the remote back button

## v0.1.1-beta

### Added
- In-app updates
- Cinemeta as default addon — provides default catalogs, meta, and search (can be disabled in configurator)

### Fixed
- Back button not exiting the app
- Search catalogs not returning results for some addons
- 403 error when trying to add certain addons
- Several meta-related bugs

## v0.1.0-beta

- Initial beta release
