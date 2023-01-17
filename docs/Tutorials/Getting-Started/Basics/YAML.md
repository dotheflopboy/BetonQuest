---
icon: material/newspaper
tags: 
  - YAML-Tutorials
---
# YAML Syntax
This plugin uses the YAML (`.yml`) format for all files. You may already know it from other plugins as most use this format.
Before we can start you need to understand the fundamentals of YAML.

In theory, you can edit quests with any editor. However, using the feature-packed 
Visual Studio Code is highly recommended! It will highlight any syntax errors you may make with YAML.

[:material-download: Install Visual Studio Code](https://code.visualstudio.com){ .md-button .md-button--primary .noExternalLinkIcon}

## YAML Basics

YAML is `key: "value"` based. This means you use a :octicons-key-16: to get a certain value.
Let me show you an example:

```YAML title="YAML Data Format"
key: "value"
Jack: "Some data about Jack"
```
Now you can use the :octicons-key-16: `Jack` to obtain `Some data about Jack`.

Keys and values can also be nested into each other. Then they **must** be indented with two spaces.

```YAML title="Nested YAML"
outerName:
  innerName: "innerValue"
  anotherInnerName: "BetonQuest is great!"
```

Values can span multiple lines using `|` or `>`.
Spanning multiple lines using a “Literal Block Scalar” `|` will include the newlines and any trailing spaces. 
Using a “Folded Block Scalar” `>` will fold newlines to spaces, 
it’s used to make what would otherwise be a very long line easier to read and edit. 
In either case the indentation will be ignored.

Examples:

```YAML title="Multiple lines"
include_newlines: |
            exactly as you see
            will appear these three
            lines of poetry

fold_newlines: >
            this is really a
            single line of text
            despite appearances
```

Another way to show multiple lines is using the newline characters: `\n`.

```YAML title="Multiple lines"
fold_same_newlines: "line1\nline 2\nline  3\nf\last line"
```

!!! warning
    Tabs are not supported. Use spaces instead.
    You shouldn't name anything `yes`, `no`, `on`, `off`, `null`, `true` or `false` as those names are reserved keywords in YAML.  
    if you use the `:` character in a value you have to escape it using backslashes.
    One backslash (\) is required when using no quoting at all (...) or single quotes ('...'). Two backslashes are required (\\) when using double quotes ("...").
 
---
[:material-arrow-right: Next Step: Conversations](../Basics/Conversations.md){ .md-button .md-button--primary }
