## Install
```
cd "~/Library/Application Support/Sublime Text 3/Packages"
git clone https://github.com/leec651/sublime-omc.git
```

## Usage

### Generate New Config
The plug-in currently supports generating empty csv and fixed width templates. To create an empty template, type `new` in your `.yaml`.  You will then see the folllowing suggestion. Choose the file type you are working on.

<img src="https://i.imgur.com/w8sEf01.png" width="30%">
<img src="https://i.imgur.com/IWlTVXv.png" width="30%">

### Transformer Auto-complete 
During the implementation of your config, the plug-in offers auto-complete features for most of the transfoemrs avaialbe. For example, when you type `sub`, avaiable transformers will appear in the list. 

<img src="https://i.imgur.com/OWMdzFg.png" width="30%">
<img src="https://i.imgur.com/iPet12x.png" width="30%">

## Available Transformer
### Field
* `add_relativedelta`:  add relative delta.
* `fixed_value`: fixed value.
* `format_datetime_field`: formate a datetime.
* `format_phone`: format a phone number.
* `if_not_default`: Returns a function to set a default value if the value is None or falsey. Use the function default if False should not also evaluate to the default.
* `map_ethnicity`: Maps industry race ethnicity codes to standard codes.
* `map_with_default`: Map with default.
* `regex_pattern_match`: Regex match only matches first pattern from the start of the string.
* `replace_inf_datetime_field`: Replace infinite time with 9990/01/01.
* `replace_regex_matches`: Replaces the characters matched by regex_pattern with replacement.
* `substring`: Ability to slice a string. Work similar to string[start:end]. End index must be smaller than length of column value.
* `truncate`: truncate up to # of characters.

### Row
TBD 


## Tip
* You can key in `tab` to go to the next input field. For example,
