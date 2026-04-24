# Changelog

### Discord https://discord.gg/CwkVahJQb2

### Downloader code 5781040

## v0.5.4-beta

### New Features
- Google Home Integration: Nearby devices like Google Nest displays and the Google Home app now show and control what's playing, and Google Home speakers can control playback by voice ("Hey Google, pause")

### Added
- Option for back button to scroll to first poster/card in row instead of navigation drawer (new setting)
- Ability to reorder catalogs within hubs
- New streaming services
- Setting to control whether newly aired episodes show in continue watching
- Brazilian Portuguese added to subtitle languages
- Ability to play random episodes of a series
- Setting to control the size of landscape cards and poster cards

### Changed
- All player controls are now dimmed to match subtitles when in HDR mode
- In-player modals now hide the rest of the player controls on open
- Player screen now shows logo instead of text title (new setting)
- Updated Dutch translation
- Dates are now localized based on the user's language region
- If you close the app while in the player screen, it is no longer reset to the detail screen when you open it again
- Updated nav menu item styles for higher visibility

### Fixed
- Error message was displayed for slow-loading catalogs from third-party addons on the discover screen
- Long pressing the play button for too long to display the stream picker would automatically select the first stream
- Metadata would not show for titles with a TMDB ID but no IMDB ID
- Exiting the app from the nav drawer would cause the nav drawer to be open when you opened the app again
- Newly aired episodes were jumping to the front of continue watching even if other titles had been watched since the episode aired
- Android 7 devices could not use the in-app updater
- Remote volume buttons did not control Bluetooth soundbars and some other audio devices while the app was in the foreground

## v0.5.3-beta

### Added
- Localization for genre hub cards and hub detail screen catalog titles
- Added support for TV addons (not IPTV)
- Trakt-style drop show feature that removes a show from the continue watching row and the upcoming schedule row
- Stream information on the player screen: resolution, Dolby Vision/HDR, audio codec, and avg bitrate
- New streaming services: AsianCrush, BBC iPlayer, BritBox, Kocowa, OnDemandKorea, Viu, Watcha
- Added unwatched episodes batch to continue watching cards (new setting)

### Changed
- P2P/torrent streams are now filtered from the streams list so they do not appear
- Upcoming schedule row now shows all series with watch progress instead of only series from lists
- Back button during playback now exits the player immediately; if the OSD is showing, back hides it instead (matches convention of major streaming apps)
- RTL progress bars and player controls updated to LTR to match industry conventions

### Fixed
- Episodes were being marked as watched in WuPlay but not in Trakt
- Watching a previously watched episode did not save progress
- Error message could be displayed over top of a video while it is playing
- Inaccurate scrobble state sent to Trakt when fast forwarding or rewinding while paused
- Preset catalogs only showing 20 items on the discover screen
- TMDB id based search catalogs showing stale metadata

## v0.5.2-beta

### New Features
- Ratings poster feature (new setting)
- RTL support app-wide
- Upcoming schedule row on home screen (new setting)

### Added
- Localization support for Hindi, Tamil, Telugu, Bengali, Marathi, Arabic (RTL), and Hebrew (RTL)
- Time remaining on the player screen
- Release date on future release movies on poster card and detail screen (new setting)
- Profile-scoped language setting
- Ability to add multiple instances of the same addon

### Changed
- Updated list indicator and watched indicator on poster cards to use theme color
- Made refinements to the Trakt recommendations implementation
- SDH subtitle clean up now handles speaker labels
- New episodes of currently airing series now show on continue watching row
- Stream addon results now show in the same order in the stream picker as they do in the web configurator

### Fixed
- Frame rate matching did not work as expected when resuming a title
- Crash in the stream picker when many stream addons are installed

## v0.5.1-beta

### Added
- Experimental - Aspect ratio control button in player (remove black bars)
- Recommendations to Trakt sync
- 13 new streaming services (US, CA, IN)
- Setting to clean up SDH subtitles
- Episodes inside the player screen
- Ability to modify hub items in the layout configurator without having to remove the hub and add it back
- Number of seasons and series status on the series detail screen

### Changed
- Minor UI changes to detail screen
- Episode cards are now infinite scroll — no need to manually switch seasons
- Increased localization support app-wide

### Fixed
- App crash when viewing the info screen in the player
- MDBList catalogs not updating
- Adding an item to your watchlist from the home screen did not update the watchlist row until navigating away and back
- Unable to change the default filmography sort order

## v0.5.0-beta

### Added
- New Feature: Hubs (streaming services, genres, studios)
- New Feature: Layout, new way of managing content on home and discover screens
- New Feature: Native catalogs, no need for catalog addons anymore
- Automatic subtitle dimming for HDR and Dolby Vision content
- High contrast subtitle style option
- Catalog caching to improve catalog loading speed. TTL is adjustable in the layout settings screen

### Changed
- Catalogs are now part of the new Layouts feature
- Playback-related aspects of the app (play button, etc.) are no longer visible unless a valid stream addon is detected
- Increased maximum subtitle offset from 10 seconds to 180 seconds
- Increased maximum stream timeout from 120 seconds to 300 seconds

### Fixed
- Support for collection-based catalogs
- App crash when trying to play certain titles for localized users
- Certain anime series were not being divided into seasons properly
- Newly added watch list items did not show in the home screen watch list until navigating away and back

### Deprecated
- Save search results to list

## v0.4.2-beta

### Added
- Display metadata for similar titles on detail screen
- Display awards in hero and on detail screen

### Changed
- Increased memory heap size to prevent out-of-memory crashes
- Forced subtitles are now shown by default if available
- Increased robustness of localized metadata

### Fixed
- App crash on audio track selection in player
- Broken metadata fetching for anime (Kitsu, MAL) and TVDB catalogs
- Several crash sites related to the focusing system

## v0.4.1-beta

### Added
- Device-level setting to specify the maximum bitrate for streams
- Device-level setting to skip Dolby Vision streams that lack an HDR fallback
- Device-level setting for stream timeout
- Remove option added to Continue Watching long-press menu
- Ability to specify sort order for lists
- More descriptive error messages on stream playback failure
- Crash reports are now sent to the backend to help troubleshoot random app crashes
- Now supports Android SDK version down to 24

### Fixed
- Home screen crash when a single catalog contained the same item multiple times
- App crash on the person screen
- Non-HTTPS (HTTP) streams now supported
- Single remote back button press during playback no longer exits the player
- Clearing progress for an episode would mark all episodes in the entire series as unwatched

## v0.4.0-beta

### Added
- Collections — groups related titles together (e.g., Star Wars collection), powered by TMDB
- Rotten Tomatoes ratings

### Changed
- Refactored the cast button in the player to provide information about the item being watched in addition to cast
- Continue watching row now auto-plays the last played stream (enabled by default, can be turned off in settings)

### Fixed
- External subtitles were not set based on preferred subtitle language
- Miscellaneous Trakt integration fixes
- Miscellaneous fixes to increase robustness of playback

## v0.3.1-beta

### Added
- "Ends at" time on the player screen

### Changed
- Switched from displaying text titles to displaying logos
- Redesigned details screen
- Miscellaneous changes to improve the robustness of series progress tracking
- Poster progress bar now only shows when poster is focused

### Fixed
- Some streams would fail after aggressive seek forward or seek back
- Stream fallback during playback now resumes from the current position instead of starting from the beginning

## v0.3.0-beta

### Added
- Trakt integration for scrobbling, watchlist, continue watching, watch history, and personal lists
- Ability to display lists, including Trakt lists, on home and discover screens

### Changed
- Updated portions of the web configurator UI
- Redesigned the continue watching row
- Style changes to various parts of the UI
- Refactored Watchlists to Lists
- Catalog visibility and order is now managed exclusively in the web configurator

### Fixed
- "Who's Watching" screen was not being displayed as expected

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
