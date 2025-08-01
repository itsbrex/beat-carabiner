# Change Log

All notable changes to this project will be documented in this file.
This change log follows the conventions of
[keepachangelog.com](http://keepachangelog.com/).

## [Unreleased][unreleased]

Nothing so far.


## [8.0.0] - 2025-07-21

### Changed

- Works with Beat Link 8.x, to add compatibility with the Opus Quad,
  and ability to simulate multiple CDJs when working with only a
  Pioneer DJ mixer.
- Updated to lib-carabiner 1.2.0, which embeds Ableton Link 3.1.2.


## [7.3.0] - 2023-11-24

### Changed

- The major and minor versions of beat-carabiner will now track those
  of Beat Link, since that provides much of the functionality of the
  library.
- Allow negative latencies thanks to user reports of beat packets
  arriving before beats are heard.
- Swapped ordering of some activities during tempo adjustment to
  slightly tighten up timeline synchronization.
- Fixed some range checks, documentation, and log lines.
- Improved source code readability in a few places.
- Updated beat-link to 7.3.0 which adds many features and fixes,
  including support for the high-precision position packets sent by
  CDJ-3000s.


## [1.0.0] - 2022-03-07

### Changed

- Updated lib-carabiner to 1.1.6 which adds native support for Apple
  Silicon macs.
- Updated beat-link to 7.0.0, which adds many new features, such as
  support for rekordbox phrase analysis, CDJ-3000s (with up to six on
  the network), and more.
- Fixed a `NullPointerException` when calling `connect` with no
  `failure-fn` supplied if Carabiner never replies.


## [0.2.3] - 2020-12-28

### Changed

- Update lib-carabiner to 1.1.5 to get new version of Carabiner with
  Ableton Link 3.0.3.
- Update beat-link to 0.6.3 for new features and fixes.
- Update electro to 0.1.4 for new features and fixes.


## [0.2.2] - 2020-05-10

### Fixed

- Incorporates the latest release of Beat Link, for many improvements.
- Added type hints throughout so the Clojure compiler could avoid the
  use of reflection, which will improve performance.


## [0.2.1] - 2020-02-09

### Fixed

- Triggers mode in Beat Link Trigger couldn't work fully correctly (it
  would be inappropriately influenced by the current Pioneer tempo
  master even if the active trigger was tracking some other player).
  To properly support this kind of use case, Beat Carabiner now offers
  a `:manual` sync mode.
- Some modes of operation needed by Open Beat Control (but not Beat
  Link Trigger) were not implemented correctly.
- Better validation and state cleanup around going offline when no
  devices are visible.


## [0.2.0] - 2019-11-24

### Changed

- This is a completely new purpose for the project, as a shared
  library to be used by Beat Link Trigger, Open Beat Control, and
  other Clojure projects that need to bridge between Beat Link and
  Carabiner. It has been released to support the release of Beat Link
  Trigger version 0.6.0, and will be documented and added to the
  Releases page once Open Beat Control is ready to take over the
  standalone capabilities offered by release 0.1.2.


## [0.1.2] - 2019-10-31

### Fixed

- Release 0.1.1 was not actually tested, and there were some changes
  to the Beat Link API which caused it to crash. Even though this is
  an interim release until Open Beat Control is ready (and people are
  ready to move to it), I want people to be able to take advantage of
  the fixes in Beat Link.


## [0.1.1] - 2019-10-25

### Fixed

- Incorporates a much newer version of beat-link which has many
  important fixes. This is expected to be the final release of this
  project as a standalone executable; those features are moving to the
  planned open-beat-control project, which will add many more too.


## 0.1.0 - 2017-03-20

### Added

- Intitial Release.

[Unreleased]: https://github.com/brunchboy/beat-carabiner/compare/v8.0.0...HEAD
[8.0.0]: https://github.com/brunchboy/beat-carabiner/compare/v7.3.0...v8.0.0
[7.3.0]: https://github.com/brunchboy/beat-carabiner/compare/v1.0.0...v7.3.0
[1.0.0]: https://github.com/brunchboy/beat-carabiner/compare/v0.2.3...v1.0.0
[0.2.3]: https://github.com/brunchboy/beat-carabiner/compare/v0.2.2...v0.2.3
[0.2.2]: https://github.com/brunchboy/beat-carabiner/compare/v0.2.1...v0.2.2
[0.2.1]: https://github.com/brunchboy/beat-carabiner/compare/v0.2.0...v0.2.1
[0.2.0]: https://github.com/brunchboy/beat-carabiner/compare/v0.1.2...v0.2.0
[0.1.2]: https://github.com/Deep-Symmetry/crate-digger/compare/v0.1.1...v0.1.2
[0.1.1]: https://github.com/Deep-Symmetry/crate-digger/compare/v0.1.0...v0.1.1
