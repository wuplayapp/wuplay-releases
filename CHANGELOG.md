# Changelog

Please consider donating to the project :-)

https://ko-fi.com/wuplaydev

Discord https://discord.gg/PvZjHVGtE9

Downloader code 5781040

GitHub https://github.com/wuplayapp/wuplay-releases

## v0.7.2-beta

This update contains some key terminology changes (you'll live, I promise)

### Added
- Long press on backspace clears entire search query (native search screen)
- New keyword catalog type. Web Configurator > Layout > Add
- Include/exclude keywords in TMDB native catalogs
- Exclude keywords and genres in content filters (formerly catalog filters)
- "Copy url" drawer option for mdblist and trakt based catalogs in the layout tab
- Avg runtime to show detail page

### Changed
- App-wide terminlogy changes: Series > Shows, My Lists > My Stuff, Catalog Filters > Content Filters
- More polish and refinements to the native search screen
- Deprecated the filmography min votes setting, uses global content filters min votes instead
- DV7 to HDR conversion forced when setting is enabled even if device advertises support

### Fixed
- Another Fire TV bug that prevented users from doing multiple voice searches without navigating away from the search screen then back again 
- Filmography row edge case bug that caused app crash
- Edge case where playback would get stuck and required an additional dpad left/right tap to get unstuck
- Mbps was not displayed in player screen when resuming from cached link


## v0.7.1-beta

### New Feature

### Added
- Long press poster menu on native search screen

### Changed
- Search history chips no longer auto fetch results, use remote enter instead
- Polish and refinements to the new native search screen

### Fixed
- Stream picker addon chips not scrolling properly
- Several focus system bugs on new native search screen 

## v0.7.0-beta

The headline for this release is the new native search feature. This is the initial release of a major feature so you can expect minor changes over the coming of weeks.

### New Feature
- Native search, no addons required

### Added
- New adult titles catalog filter (Web Config > Settings > Catalog Filters > General)

### Changed
- Web config: Privacy & Data tab moved to Settings
- UI: Narrower sidebar and less padding. The result is a wider content area.

### Fixed
- Croatian (and other Serbo-Croatian, Indonesian, and Norwegian) subtitles and audio tracks not being detected or auto-selected when tagged with combined language codes
- Subtitles button sometimes not displayed in player


## v0.6.7-beta

Hotfix release — bug fixes only.

### Fixed
- Wrong episode playing when advancing to next episode or manually choosing an episode
- Error message when trying to advance to the next episode

## v0.6.6-beta

### Added
- Español (México) and "Português (Portugal) languages
- AMC+ to Streaming Services

### Changed
- Reduced time-to-first-frame when resuming a stream
- Episode card will show series background when episode background is unavailable
- Episodes auto load on season chip change instead of having to press enter (detail screen)

### Fixed
- Some series weren't correctly showing in watch history
- Poster row scrolling could be laggy on some devices
- Hub logos sometimes showed as white rectangles

## v0.6.5-beta

### New Feature
- Don't Show Again: the ability to hide titles in catalogs app-wide (new long press menu item)
- Are You Still Watching? (new setting, default 3 episodes)

### Added
- Search history
- Bulk-add addon catalogs to home/discover screens (web config > layout)
- Bulk-remove catalogs from home/discover screens (web config > layout)

### Changed
- Audio track picker now includes technical details
- Subtitle min. size reduced from 50% to 25%
- Subtitle max. offset increased from 30% to 95%

### Fixed
- Skipping forward/backward in player could trigger some addons to hit rate limits
- Some addons with valid streams were throwing 403 errors


## v0.6.4-beta

### New Feature
- Autoplay trailers (new setting, disabled by default)

### Added
- View Details and View Trailer added to poster long-press menu
- Ability to change addon names
- Option to disable stream auto fallback (new setting)
- Adjustable stream auto fallback delay (new setting)
- New global catalog filters: digital release only, min vote, min rating (Webconfig > Settings > Catalog Filters)

### Changed
- Last played stream now tracked on filename instead of result index
- You can now mark a movie watched/unwatched without first clearing the current watch progress

### Fixed
- My Lists based rows in Discover screen were showing blank posters.
- Tunneled playback would get stuck on loading screen
- Race issue that would cause continue watching items from one profile to appear in another profile on the same device.
- Keyboard would take a long time to display on search screen when many or slow search addons were installed
- Playback could get stuck on flashing logo screen when seeking forward/backward
- Preferred audio language of original language was not always honored when played from continue watching row. 

## v0.6.3-beta

### Added
- Dolby Vision profile 7 to HDR fallback (new setting, enabled by default)
- Catalog filters now apply to hubs, presets, mdblist, and trakt native catalogs (set in web config > settings > catalog filters)
- Gujarati and Marathi languages to catalog filters

### Changed
- New trailer implementation that will hopefully fix the random issues some users have reported as well as increase quality and speed
- Removed Import Data option in web config privacy & data tab (may return in future)
- Information-based stream cards now show in the stream picker. (ie aioratings, stremshare)
- Webconfig change: added Settings > Catalog Filters. Global filters, currently only language and country but more will be added
- Re-designed add/edit addon UI in web config
- Some anime series now display both relative and absolute episode numbering (ie hunter x hunter, one piece)

### Fixed
- More anime fixes (damn you one piece)

## v0.6.2-beta

### New Features
- IntroDB integration: skip intro, recap, outro when available

### Added
- Subtitle track ID to subtitle picker (if present)
- Vietnamese language localization. 

### Changed
- Series level cast and crew now shows directors and producers as well as episode count for all cast and crew (make take up to 7 days to fully propagate, immediate with clear app cache)
- Switched positions of the random episode button and the trailer button for series on the detail screen
- Total episodes displayed on detail screen in addition to total seasons
- Added an original language option to preferred audio language settings
- Option to show indicators on unfocused posters (new setting)
- Removed cancel button from next episode popup (use back button instead)
- Upcoming Schedule now requires at least one fully watched episode for a show to appear (matches trakt Up Next logic)
- Organized interface settings screen into sections
- Option to only show next episode on upcoming schedule instead of all future episodes. (new setting)

### Fixed
- "Coming Soon" was not being displayed on the collection and search screens for unreleased upcoming movies
- Poster ratings did not show correctly for search results and filmography (person screen)
- Some third-party addon catalogs were showing as empty
- Episode cards were not being blurred in player screen episode list (when blurred setting is enabled)
- Age restrictions: setting max age to young child (0-7) was letting US PG rated movies slip through (users with age restricted profiles should clear app cache, not needed for non age restricted users)
- Badly behaving addons that mark series incorrectly as movies
- Some poster images and backdrops were not being updated properly
- Edge case where a dropped show would later reappear in the upcoming schedule 

## v0.6.1-beta

### Added
- New native TMDB catalogs with 10 filters (unlimited custom catalog options)
- Bulgarian language option for subtitles
- Ability to filter MDBList, Trakt, and My Lists based catalogs by type (mixed, movies only, series only)
- Settings for catalog languages and catalog countries to filter native catalogs
- Saved collections can now be added to home and discover screens
- New permission in Profile Manager to hide profile key and QR code in Android TV app

### Changed
- Added filtering to latest release catalogs in Hubs to produce higher quality results
- When the stream picker is open, D-pad left and right now cycles through the individual addon chips
- Person page now loads faster for non-age restricted profiles

### Fixed
- Hero content was rendered on the search screen even if all results were filtered out by age restrictions
- Some anime seasons were not being divided properly
- Advancing to the next episode would show the previous episode's subtitles
- Season 0 episodes no longer show in upcoming schedule row.
- Upcoming schedule card would show the wrong number of days in the count down badge for some time zones. (hopefully finally fixed)

## v0.6.0-beta

### New Features
- Profile Manager: new web configurator feature for managing multiple profiles from a single interface (new menu tab)
- Age Restrictions: Set age restrictions per profile in web configurator settings screen (new menu tab)

### Added
- Sinhala language to preferred subtitle languages
- Hungarian language localization

### Changed
- Moved episodes button under the play button on the detail screen
- Increased localization coverage for app UI elements
- You can now update your profile display name, avatar, theme color and pin from the web configurator settings screen (new menu tab). 
- More detailed error messages on stream failover

### Fixed
- Subtitle color could not be set in RTL language mode
- Some unsupported streams that previously failed over quickly were getting stuck and causing long delays before failover to next stream
- Enter button on some third-party remotes was not working 
- Long press button release could accidentally select first item in context menu for some third-party remotes.
- More formatting cleanup of .ass subtitles (proper .ass support in future update)
- Some specialty anime addon catalogs were not showing as expected. 
- Upcoming schedule card would show the wrong number of days in the count down badge for some time zones. 
- Switching episodes in player screen did not always honor autoplay first stream setting
- Some series were not showing episodes on detail screen when using a kitsu id instead of imdb id or tmdb id

## v0.5.5-beta

### Added
- New 16:9 launch icon - shoutout @Branding_Brevity on discord (android tv device reboot required to see new version)
- Setting to enable tunneled playback
- Setting to show today's airing episode in Continue Watching instead of Upcoming Schedule
- New subtitle style settings
- Subtitle style settings in player screen with preview
- Trakt icon on recommended movies and recommended series catalogs
- New streaming services

### Changed
- In Continue Watching and Upcoming Schedule, focusing on an episode now shows the episode information in the hero area instead of the series information (new setting)
- Consolidated several settings screens into a new Configuration settings screen
- Continue Watching row now shows episode thumbnails instead of series-level thumbnails (new setting)
- Show embedded subtitle track names (e.g. "English — Signs / Songs", "English — Dialogue") so multiple same-language tracks are distinguishable in the picker
- Stream picker now honors line breaks in description
- Discover screen now shows chips for media types that are not movie or series

### Fixed
- Videos would start in a paused state on some Android TV devices when frame rate matching is enabled
- Future episodes with no release date were showing in the upcoming schedule and continue watching
- Third-party addon catalog pagination getting stuck on discover screen
- Cleaned up .ass subtitles that were displaying gibberish
- Movie catalogs were showing on series and series catalogs were showing on movies in the Discover screen
- Stream timeout setting greater than 45 seconds was not being honored

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
