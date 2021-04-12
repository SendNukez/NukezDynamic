# NukezDynamic

This is a tweaked version of the DribbblishDynamic theme.

## Screenshots

#### Dark

![demo-dark](./color-match-bg.gif)

#### White

![demo-white](./white.png)

## More

Requires spicetify-cli **v0.9.9 or newer**.

### How to install

Run these command:

#### Linux and MacOS:

In **Bash**:

```bash
cd "$(dirname "$(spicetify -c)")/Themes/NukezDynamic"
mkdir -p ../../Extensions
cp nukez-dynamic.js ../../Extensions/.
spicetify config extensions nukez-dynamic.js
spicetify config current_theme NukezDynamic color_scheme dark
spicetify config inject_css 1 replace_colors 1 overwrite_assets 1
spicetify apply
```

#### Windows

In **Powershell**:

```powershell
cd "$(spicetify -c | Split-Path)\Themes\NukezDynamic"
Copy-Item nukez-dynamic.js ..\..\Extensions
spicetify config extensions nukez-dynamic.js
spicetify config current_theme NukezDynamic color_scheme dark
spicetify config inject_css 1 replace_colors 1 overwrite_assets 1
spicetify apply
```

### Hide Window Controls

Windows user, please edit your Spotify shortcut and add flag `--transparent-window-controls` after the Spotify.exe:
![instruction1](./windows-shortcut-instruction.png)

Alternatively, you can use `SpotifyNoControl.exe`, included in this theme package, to completely remove all windows controls and title menu (three dot at top left corner). Title menu still can be access via Alt key. Closing, minimizing can be done via right click menu at top window region.  
`SpotifyNoControl.exe` could be used as Spotify launcher, it opens Spotify and hides controls right after. You can drag and drop it to your taskbar but make sure you unpin the original Spotify icon first. Alternatively you can make a shortcut for it and add to desktop or start menu.  
Moreover, by default, Spotify adjusted sidebar items and profile menu icon to stay out of Windows native controls region. If you decided to use `SpotifyNoControl.exe` from now on, please open `user.css` file and change variable `--os-windows-icon-dodge` value to 0 as instruction to snap icons back to their original position.

![nocontrol](https://i.imgur.com/qdZyv1t.png)

### Color Schemes

There are 2 color schemes you can choose: `white`, `dark`. Change scheme with commands:

```bash
spicetify config color_scheme <scheme name>
spicetify apply
```

# How to uninstall

Remove the nukez-dynamic script with the following commands

```bash
spicetify config extensions nukez-dynamic.js-
spicetify apply
```

## `color.ini` reference

These keys are used in the `colors.ini` file.

| Key                                     | Target                                                                   |
| --------------------------------------- | ------------------------------------------------------------------------ |
| `main_fg`                               | The main Accent, used for sidebar and some interface elements            |
| `main_bg`                               | The real star of the show, the main Backgroud of app (on the right side) |
| `secondary_fg`                          | Main text and some other small stuff                                     |
| `secondary_bg`                          | The background for the left side navbar                                  |
| `selected_button`                       | Button currenly being hovered                                            |
| `pressing_fg`                           | The color that momentarialy appears when you press anything              |
| `pressing_button_fg`                    | The textcolor for a pressed button                                       |
| `pressing_button_bg`                    | BG color for the pressed button                                          |
| `sidebar_and_player_bg`                 | Background for the player                                                |
| `sidebar_indicator_and_hover_button_bg` | For the slider & selected items when you hover over it                   |
| `cover_overlay_and_shadow`              | Overlay for when you hover over the album covers                         |
| `slider_bg`                             | The background for the slider                                            |
| `scrollbar_fg_and_selected_row_bg`      | Color for the current selected row                                       |
| `active_control_fg`                     | Foreground for active control items                                      |
| `indicator_fg_and_button_bg`            | Button text color                                                        |
| `miscellaneous_bg`                      | The background color of toolips ("You're offline" etc)                   |
| `miscellaneous_hover_bg`                | Hover Color for the Tooltips                                             |
| `preserve_1`                            | Misc text colors                                                         |

## Credits

Shoutout to @khanhas for the original Dribbblish theme!
