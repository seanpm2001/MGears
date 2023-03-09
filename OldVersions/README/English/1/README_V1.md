
***

<img alt="MGears logo failed to load. Click/tap here to attempt to view it" src="/MGears_Logo_1024pxIcon_V1_HighCompression.png" width="200" height="200"/>

# MGears

`A micro-language for defining settings pages`

**File extension:** `*.mgear` as in [`PROJECT_LANG_1.mgear`](/PROJECT_LANG_1.mgear)

[`The rest of this document is taken from the original MGears draft`](/Docs/Original-Concept/Draft1/README.md)

## Developer notes

I didn't want to have to create a language for a single task, 
but I couldn't find anything that fit my needs for this project.
This language is in its early stages, and I am hoping that it can simply be
replaced with a Python/other language LIBrary in the future if possible.

## What does MGear stand for?

It originally stood for Meadows, the name of the operating system it was 
originally intended for, but 2 other common terms are unofficially
associated with it:

- Mozilla (can't use for legal and originality reasons)
- Myrick
- A 3rd other term can be anything you want it to stand for. The M is a wildcard.
Additionally, an s can be added to the end of the name (gears, instead of gear)

## Shebangs

Shebang for settings pages:

```shell
#!/usr/bin/env mgearA
```

Shebang for other pages:

```shell
#!/usr/bin/env mgearB
```

## Style files

- Mozilla style
- Chrome style
- Meadows style
- Custom style

## Setting types (Markup)

- [ ]

- ( )

- { }

## Settings type ID sets

- `NUM-INT` : Number field (integer)
- `NUM-DOU` : Number field (double)
- `NUM-FLO` : Number field (float)
- `BOX-CHECK` : Checkbox
- `BOX-RADIO` : Radio button

## Settings type ID attributes

- `:disabled`
- `:enabled`
- `:active`
- `:inactive`
- `:drops1`

The `:disabled` attribute makes a setting locked, and impossible for the user to change through the GUI

The `:enabled` attribute is optional, and makes a setting unlocked. It may be removed due to verbosity.

The `:active:` attribute means that a setting is currently enabled/enabled by default

The `:inactive:` attribute means that a setting is currently disabled/disabled by default

The `:drops1` attribute makes it so this setting has to be checked in order to enable/disable settings in its group.

Objects

`[OBJ-ID:CUR="DEMO"_NUM-INT_SUB1_ID="11111111"]()`

Refer to objects by their ID, the current settings page, with its ID, the type of object (integer), the level of the setting (H1-H6) and its 8 digit ID. The ID can commonly contain numbers 0-9, and letters A-Z, although it can also contain any character other than quotation marks. The field is limited to a maximum amount of 256 bytes of data.

Each setting has this object code applied to it

The succeeding `()`

`[]("Set a time limit of", "seconds")`

The `,` indicates that there is a piece of text that comes after the number field. You can use as many checkmarks as needed. If there is no number field, the following can be used:

`[]("Enable smooth scrolling")`

## Comments

```python
# This is a comment
```

```python
"""
This is a multi-line comment
"""
```

```python
'''
This is also a multi-line comment
'''
```

As you can see, comments in this language are identical to comments in the Python programming language.

***

**File version:** `1 (2023, Wednesday, March 8th at 4:04 pm PST)`

***
