## Features

- Podcast group management
- Playlists support
- Sleep timer / speed setting
- OPML file export and import
- Auto-syncing in the background
- Listening and subscription history record
- Dark mode / accent color
- Download for offline play
- Auto-download new episodes / auto-delete outdated downloads
- Settings backup
- Skip silence
- Boost volume

More to come...

## Preview

| Podcast                 | Episode                 | Dark Mode                |
| ----------------------- | ----------------------- | ------------------------ |
| ![][podcast screenshot] | ![][episode screenshot] | ![][darkmode screenshot] |

## Architecture

### Plugins

- Local storage
  - sqflite
  - shared_preferences
- Audio
  - just_audio
  - audio_service
- State management
  - provider
- Download
  - flutter_downloader
- Background task
  - workmanager

### Directory Structure

```
UI
src
└──home
   ├──home.dart [Homepage]
   ├──searc_podcast.dart [Search Page]
   └──playlist.dart [Playlist Page]
└──podcasts
   ├──podcast_manage.dart [Group Page]
   └──podcast_detail.dart [Podcast Page]
└──episodes
   └──episode_detail.dart [Episode Page]
└──settings
   └──setting.dart [Setting Page]

STATE
src
└──state
   ├──audio_state.dart [Audio State]
   ├──download_state.dart [Episode Download]
   ├──podcast_group.dart [Podcast Groups]
   ├──refresh_podcast.dart [Episode Refresh]
   └──setting_state.dart [Setting]

Service
src
└──service
   ├──api_service.dart [Podcast Search]
   ├──gpodder_api.dart [Gpodder intergate]
   └──ompl_builde.dart [OMPL export]
```

## Known Issue

- Playlist is unstable

[homepage screenshot]: https://raw.githubusercontent.com/stonega/tsacdop/master/preview/1585893838840.png
[group screenshot]: https://raw.githubusercontent.com/stonega/tsacdop/master/preview/1585894051734.png
[podcast screenshot]: https://raw.githubusercontent.com/stonega/tsacdop/master/preview/1585893877702.png
[episode screenshot]: https://raw.githubusercontent.com/stonega/tsacdop/master/preview/1585896237809.png
[darkmode screenshot]: https://raw.githubusercontent.com/stonega/tsacdop/master/preview/1585893920721.png
