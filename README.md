![bash_unit CI](https://github.com/pforret/shaml/workflows/bash_unit%20CI/badge.svg)
![Shellcheck CI](https://github.com/pforret/shaml/workflows/Shellcheck%20CI/badge.svg)
![GH Language](https://img.shields.io/github/languages/top/pforret/shaml)
![GH stars](https://img.shields.io/github/stars/pforret/shaml)
![GH tag](https://img.shields.io/github/v/tag/pforret/shaml)
![GH License](https://img.shields.io/github/license/pforret/shaml)
[![basher install](https://img.shields.io/badge/basher-install-white?logo=gnu-bash&style=flat)](https://www.basher.it/package/)

# shaml

![shaml](assets/url.download.215333.jpg)

Read YAML files within bash

## 🔥 Usage

```
Program : shaml  by peter@forret.com
Version : v0.0.1 (Apr 22 16:07:13 2023)
Purpose : Read YAML files within bash
Usage   : shaml [-h] [-q] [-v] [-f] [-l <log_dir>] [-t <tmp_dir>] <action>
Flags, options and parameters:
    -h|--help        : [flag] show usage [default: off]
    -q|--quiet       : [flag] no output [default: off]
    -v|--verbose     : [flag] also show debug messages [default: off]
    -f|--force       : [flag] do not ask for confirmation (always yes) [default: off]
    -l|--log_dir <?> : [option] folder for log files   [default: /Users/pforret/log/script]
    -t|--tmp_dir <?> : [option] folder for temp files  [default: /tmp/script]
    <action>         : [choice] action to perform  [options: action1,action2,check,env,update]
                                  
### TIPS & EXAMPLES
* use shaml action1 to ...
  shaml action1
* use shaml action2 to ...
  shaml action2
* use shaml check to check if this script is ready to execute and what values the options/flags are
  shaml check
* use shaml env to generate an example .env file
  shaml env > .env
* use shaml update to update to the latest version
  shaml update
* >>> bash script created with pforret/bashew
* >>> for bash development, also check out pforret/setver and pforret/progressbar
```

## ⚡️ Examples

Input:

```yaml
# comment start on col 1
Word: one # comment starts after
Sentence: "one sentence"
level1:
  level2:
    level3:
      level4:
        level5:
          level6: "sixth level"

Months:
  - January
  - February
  - March

Author:
  Name: "John Doe"
  Address: "123 Main St, Anytown, USA"
  Tags:
    Hobbies:
      - "Fishing"
      - "Waterpolo"
```

`shaml all input.yaml` will output:

```bash
Word="one"
Sentence="one sentence"
level1_level2_level3_level4_level5_level6="sixth level"
Months+=("January")
Months+=("February")
Months+=("March")
Author_Name="John Doe"
Author_Address="123 Main St, Anytown, USA"
Author_Tags_Hobbies+=("Fishing")
Author_Tags_Hobbies+=("Waterpolo")
```


## 🚀 Installation

with [basher](https://github.com/basherpm/basher)

	$ basher install pforret/shaml

or with `git`

	$ git clone https://github.com/pforret/shaml.git
	$ cd shaml

## 📝 Acknowledgements

* script created with [bashew](https://github.com/pforret/bashew)

&copy; 2024 Peter Forret
