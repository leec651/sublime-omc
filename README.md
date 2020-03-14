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

## Available Transformers
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
* `extract_column_value`: This transform should only need to be used in headers and footers, please don't use in regular column mappings.
* `delpay_start`: This is way too specific Lucy :(
* `get_term_date`: If the status is cancelled then return the day before the eff_date as the term_date. Otherwise return the inclusive term_date, in BigQuery the term_date is exclusive so a 2018 plan would have a term_date of 2019-01-01, most vendors want an inclusive term date so 2018-12-31.
* `to_ascii`:  Returns an object where string values are converted to ascii.
* `conditional`: Used to find the result of a binary operation used on two values within a record. Available options: `eq`, `contains`, `le`, and `not_`.
* `to_upper`: Convert stirng to uppercase.
* `arithmetic`: Return value_one operand value_two.
* `replace_regex_matches`: Replaces the characters matched by regex_pattern with replacement.

### Record
* `aggregate_value`: Take the final aggregate value after processing all records, for the specified aggregate_function_name.
* `count_by_column`: Get aggregate value from an aggregate value counting function.
```
Imagine we have the following 3 input records to our value count aggregator:
{'person_name': 'bob'}
{'person_name': 'bob'}
{'person_name': 'bobette'}

the aggregated value count object would look like so:

{'bob': 2, 'bobette': 1}

Now we want to access the output values. For group footers we need to dynamically specify the key we want the count
for, using the last record in the group. Ex imagine we have this last record in a group:

{'person_name': 'bob'}

now we pass in this last record as the 'record', with column_name = 'person_name'. We get 2 back.
```
* `count_by_value`: Get aggregate value from an aggregate value counting function
```
Imagine we have the following 3 input records to our value count aggregator:

{'person_name': 'bob'}
{'person_name': 'bob'}
{'person_name': 'bobette'}

the aggregated value count object would look like so:

{'bob': 2, 'bobette': 1}

Now we want to access the output values. Using this method we pass value = 'bobette' to this function and get
1 back.
```



## Tip
* You can press `tab` to cycle through the available inputs.
