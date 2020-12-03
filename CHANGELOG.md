# Changelog
All notable changes to this project will be documented in this file.

## 2020-12-03
### Added
- Support `remapped_heldon_alone_timeout=TIMEOUT_MS`. This is a must have for a dual-key tool!

## 0.5
### Changed
- Mouse scrolling will now trigger the `with_other` modifier (`CTRL` by default).

## 0.4
### Added
- Dual-key-remap now supports remapping multiple keys.
- Mouse presses (keydown) will now work with the dual key. They trigger the with_other modifier (CTRL by default).
### Changed
- The dual key will only become the 'with_other' key when keys (or mouse) is pressed down as opposed both up and down. This means
  that fast typists should no longer experience unexpected results due to key rollover.
- Some keynames had incorrectly capitalized names, this has now been fixed (i.e. SCROLLLOCK instead of ScrollLock). If you remapped one
  of these keys you will have to update your config to use the all capitalized names.
### Fixed
- The config will now always be loaded from the same directory as the executable instead of the directory the executable was launched from.

## 0.3
### Added
- We now send hardware scan codes by default instead of virtual key codes. These inputs aren't intercepted by DirectX,
  and as a result will work better in a lot of applications (especially games).
- Now both hardware inputs and virtual inputs are supported in the config, for more information see the config.txt documentation.
- Added additional capabilities to handle both left and right modifier keys.
- Added logging support by setting `debug=1` in config.txt.

## 0.2
### Added
- Support remapping keys to themselves. For example: Escape can now be rebound to Escape alone and Ctrl with others.
### Fixed
- Fix no error messages showing in certain cases when "config.txt" could not be found.

## 0.1
### Added
- First release
