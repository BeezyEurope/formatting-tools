# Formatting Tools

Prettier is an opinionated code formatter. It enforces a consistent style by parsing your code and re-printing it with its own rules that take the maximum line length into account, wrapping code when necessary.

Prettier can be run in your editor on-save, in a pre-commit hook, or in CI environments to ensure your codebase has a consistent style without devs ever having to post a nit-picky comment on a code review ever again!

## Installation

First of all you need install the `prettier`  and `prettier-eslint` packages in your project.

```
npm install --save-dev prettier prettier-eslint
```

**NOTE:** This step is not necessary because these packages are already included in our repositories.

### Editor integration

The first step to getting immediate feedback while writing code is to add a plugin to your text editor. If you don't know how to do it, keep reading and we'll see how to add it to VSCode. If you use another editor and want to add Prettier, you can see how to do it in the [Prettier documentation](https://prettier.io/docs/en/editors.html).


To integrate prettier into VS Code you just need install the `prettier` package.

[Visual Studio Code Marketplace: Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode).


## Usage

### Using Command Palette (CMD/CTRL + Shift + P)

```
1. CMD + Shift + P -> Format Document
OR
1. Select the text you want to Prettify
2. CMD + Shift + P -> Format Selection
```

These two options are also available doing right click in the current doccument window.

### Format On Save (recommended)

You can turn on format-on-save on a per-language basis by scoping the setting:

```json
// Set the default
"editor.formatOnSave": true,
// Disable per-language
"[markdown]": {
    "editor.formatOnSave": false
}
```

## Motivation

ESLint is really an amazing tool that allow you to enforce coding patterns among your teams. This has many benefits, like outputting better and more consistent code, getting rid of useless diffs in commits like newlines, indentation among many others.

But over time, this can prove to be a bit of a pesky among the developers of a team, who find it an extra load to manually add semicolons, newlines, indentations, etc just to conform to the lint rules. This is where a code formatting tool like Prettier comes in to help you reduce these syntax mistakes and save a lot of time to focus on what really matters.
