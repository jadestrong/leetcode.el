[![MELPA](https://melpa.org/packages/leetcode-badge.svg)](https://melpa.org/#/leetcode)
# Introduction

LeetCode brings you offer, and now Emacs brings you LeetCode!

# Usage

![screencast](images/screencast.gif)

1. Execute `leetcode` command, and in problem list buffer:

| Keymap | Description                            |
|--------|----------------------------------------|
| n      | cursor move down                       |
| p      | cursor move up                         |
| l      | change prefer language                 |
| s      | filter problems by regex               |
| t      | filter problems by tag                 |
| d      | filter problems by difficulty          |
| /      | clear filters                          |
| g      | refresh without fetching from LeetCode |
| G      | refresh all data                       |
| RET    | show current problem description       |
| TAB    | view current problem description       |

More advanced navigation hotkeys can be found [here](#advanced-navigation).

2. Press `<RET>`, show problem description, move cursor to "solve it", press
   `<RET>` again, start coding!

3. After finishing your code, you can edit testcase and execute `leetcode-try`
   or execute `leetcode-submit`.

![leetcode-submit](images/leetcode-submit.png)

## Advanced Navigation

Here are some advanced navigation hotkeys that may be useful in problem list buffer:

| Keymap | Command                                    | Description                         |
|--------|--------------------------------------------|-------------------------------------|
| o      | `leetcode-show-problem`                    | show/open the current problem       |
| O      | `leetcode-show-current-problem`            | show/open a problem by id           |
| v      | `leetcode-view-problem`                    | view the current problem            |
| V      | `leetcode-view-current-problem`            | view a problem by id                |
| b      | `leetcode-show-problem-in-browser`         | show the current problem in browser |
| B      | `leetcode-show-current-problem-in-browser` | show a problem by id in browser     |
| c      | `leetcode-solve-problem`                   | start coding the current problem    |
| C      | `leetcode-solve-current-problem`           | start coding a problem by id        |

# Installation

- Vanilla Emacs: `package-install` it from melpa directly
- [Spacemacs](https://github.com/syl20bnr/spacemacs):
  [leetcode-emacs-layer](https://github.com/anmoljagetia/leetcode-emacs-layer)

~~LeetCode do not allow third party login, one workaround is restore LeetCode session from local Chrome cookies. To do this, you need to install a Python3 package called [my\_cookies](https://github.com/kaiwk/my_cookies): `pip3 install my_cookies`~~

LeetCode do not allow third party loading, one workaround is restore LeetCode session from local FireFox cookies.
To do ths, you need to install my Rust package called [browsercookie-rs](https://github.com/jadestrong/browsercookie-rs):

1. `git clone https://github.com/jadestrong/browsercookie-rs.git`
2. `cargo install --path . `

NOTE: You also need install FireFox browser, and login your leetcode accound.

## Manually

1. Clone this repository and install all dependencies
2. Move it to your load-path
3. Require it in your emacs config

# Configuration

You can set your preferred LeetCode programming language and SQL by setting
`leetcode-prefer-language` and `leetcode-prefer-sql`:

```elisp
(setq leetcode-prefer-language "python3")
(setq leetcode-prefer-sql "mysql")
```

All supported languages can be found in variable
`leetcode--lang-suffixes`.

You can save solution by setting `leetcode-save-solutions`:

```elisp
(setq leetcode-save-solutions t)
(setq leetcode-directory "~/leetcode")
```

# Debug

Call `leetcode-toggle-debug`, log will output in `*leetcode-log*` buffer.

# Contributing

Please submit PR to develop branch.
