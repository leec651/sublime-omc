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
* `add_relativedelta`
* `fixed_value`
* `format_datetime_field`
* `format_phone`
* `if_not_default`
* `map_ethnicity`
* `map_with_default`
* `regex_pattern_match`
* `replace_inf_datetime_field`
* `replace_regex_matches`
* `substring`
* `truncate`

### Row
TBD 


## Tip
* You can key in `tab` to go to the next input field. For example,
