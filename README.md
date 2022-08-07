# input-source-change.json
A Karabiner-Elements configuration file that allows function keys (F7/F8/F9) to select specific input source (particularly including Chinese, Japanese, Korean or Vietnamese, see below) without cycing though the input menu on macOS for trilingual users.

# Background
* Switching input sources among 3 languages (English/Chinese/Japanese in my case) using ^Space or ^⌥Space has been a pain as one would need to look at the input menu or menu bar to select and cycle through the input sources. 
* Using `select_input_source` directly in Karabiner-Elements would sometimes fail on CJKV (Chinese, Japanese, Korean, Vietnamese) input sources as `select_input_source` uses a deprecated macOS Carbon API that is not very reliable. The input icon changes but the actual input does not.
* As a workaround this json configuration file selects the input source before the target input source using `select_input_source` and then sends a default macOS shortcut (^⌥Space) to go to the next(target) input source.

# Installation
* Change function keys to key f7, f8, f9 in Karabiner-Elements > Preference
* Put the json file in [complex_modifications folder](https://karabiner-elements.pqrs.org/docs/json/location/)
* Add rule in Preference > Complex modifications