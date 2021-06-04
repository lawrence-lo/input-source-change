# input-source-change.json
A Karabiner-Elements configuration file that allows function keys (F7/F8/F9) to select specific input source (particularly including Chinese, Japanese, Korean or Vietnamese, see below) without cycing though the input menu on macOS for trilingual users.

# Background
* Switching input sources among 3 languages (English/Chinese/Japanese in my case) using ^Space or ^⌥Space has been a pain as one would need to look at the input menu or menu bar to select and cycle through the input sources. 
* Attempted to use `select_input_source` in Karabiner-Elements but it would sometimes fail on CJKV (Chinese, Japanese, Korean, Vietnamese) input sources due to an old unfixed macOS bug as mentioned in [Docs](https://karabiner-elements.pqrs.org/docs/json/complex-modifications-manipulator-definition/to/select-input-source/).
* Kawa has a [workaround](https://github.com/hatashiro/kawa/pull/12) but it is still unreliable when I tried to implement it in Karabiner-Elements.
* **input-source-change.json** avoids `select_input_source` and instead uses `input_source_if` to determine if ^⌥Space (default "Select next source in Input menu" shortcut) needs to be sent once or twice depending on the current input source.

# Installation
* Change function keys to key f7, f8, f9 in Karabiner-Elements > Preference
* Put the json file in [complex_modifications folder](https://karabiner-elements.pqrs.org/docs/json/location/)
* Add rule in Preference > Complex modifications