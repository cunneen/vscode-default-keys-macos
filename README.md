This extension provides the default key bindings for MacOS
for Visual Studio Code on any platform.

Based on the excellent instructions at [Scott McPeak's windows key bindings](https://github.com/smcpeak/vscode-default-keys-windows).

![mac keyboard](./assets/keyboard.jpg)

Currently, these are the defaults for VSCode 1.78.2.

This is useful if you want to run VSCode on another platform
but continue to use the bindings that are the defaults on
MacOS (e.g.,
[here](https://stackoverflow.com/questions/52726849/how-to-transfer-vscode-key-mapping-on-macos-to-ubuntu)
and
[here](https://stackoverflow.com/questions/45840945/vscode-importing-keyboard-shortcuts)).

This extension does not remove any existing bindings.  On
MacOS, that means you have everything bound twice.  On
other platforms, you have that platform's default bindings
plus the MacOS ones.  The bindings in this extension take
precedence over the defaults provided by VSCode.

<!-- copied from vscode-default-keys-windows, commented by Mike ; I should add similar screenshots
Example screenshot running on Linux:

![Screenshot of bindings](bindings-screenshot.png)

-->

## Installation

From within VSCode, go to extensions (Ctrl+Shift+X),
search for "MacOS Default Keybindings", click on it, then
click on Install.  The new bindings should be active immediately.

Alternatively, install it from the
[Marketplace page](https://marketplace.visualstudio.com/items?itemName=cunneen.default-keys-macos),
or download the VSIX file from the
[Github releases page](https://github.com/cunneen/vscode-default-keys-macos/releases)
and then use "Install from VSIX..." menu option from the "..." menu in
the Extensions page.

## How it was created

For the curious or adventurous, the procedure I used to create this
extension is:

1. Run `yo code` to make a new keybindings extension.
2. Disable all non-default extensions (within the workspace) so their
   entries do not appear in the output from the next command.
3. Run command "Preference: Open Default Keyboard Shortcuts (JSON)"
   from the command palette.
4. Copy the output into the `contributes.keybindings` section
   of `package.json`.
5. Tidy up `package.json` by adding `publisher`, etc.
6. Write documentation.

Photo by <a href="https://unsplash.com/fr/@hannahjoshua?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">hannah joshua</a> on <a href="https://unsplash.com/photos/46T6nVjRc2w?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
