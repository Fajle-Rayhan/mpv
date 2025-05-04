## Setting Used 

- *fonts*
    - uosc_icons.otf 
    - uosc.textures.ttf
- *scripts*
    - uosc (pack)
    - autoload.lua
    - delete_current_file.lua 
    - thumbfast.lua
- *script-opts*
    - console.conf (not in use)
    - thumbfast.conf
    - uosc.conf
- *Keybindign*
    - no annoying OSD, time-stamp
    - youtube like timeline thumb 
    - auto load playing file's folder into the mpv playlist 
    - "delete" key to delete playing file from the system 
    - "shift+." next playlist file to play
    - "shift+," previous playlist file to play 
    - "p" open any file with in mpv
    - "g" open playing file folder
    - "alt+s" load subtitles
    - "shit+s" to take screenshot of the playing media frame, auto save to the "user/Pictures/screenshots/" folder with png fomate 
    
## Configuration Files

1. The input.conf file allows you to configure keyboard and mouse shortcuts.
2. The mpv.conf file allows you to customize various aspects of the player's behavior, such as video and audio settings, playback options, and user interface preferences.

## Windows Config

`%APPDATA%\mpv\scripts\`

or 
`C:\Users\USER\AppData\Roaming\mpv\scripts\`

or in local mpv folder 
`/portable_config`

## Linux Config 

`~/.config/mpv/scripts/`

## Include

- script
    - uosc
    - autoload.lua
    - delete_current_file.lua
    - thumbfast.lua
- script-opts
    - console.conf
    - thumbfast.conf
    - uosc.conf
- fonts
    - uosc_icons.otf
    - uosc_textures.ttf
- input.conf
- mpv.conf

## mpv.conf

```
screenshot-directory=~/Pictures/screenshots
slang="en,eng,en-US,en-GB"
alang=en
osd-bar=no  
keep-open=yes
keep-open-pause=yes

```

## inpute.conf

```
y               cycle deband
z               cycle deband
ctrl+d          vf toggle yadif
x               add sub-delay +0.042
c               add sub-delay -0.042
b               add audio-delay +0.042
n               add audio-delay -0.042
a               cycle-values video-aspect "16:9" "4:3" "2.35:1" "-1"

ESC             quit-watch-later
CLOSE_WIN       quit-watch-later
POWER           quit-watch-later
STOP            quit-watch-later

Shift+DEL       script-message-to delete_current_file delete-file

tab             script-binding uosc/toggle-ui
# Shift+DEL     script-binding uosc/delete-file-next
end             script-binding uosc/playlist
/               script-binding uosc/keybinds
p               script-binding uosc/open-file
g               script-binding uosc/show-in-directory
G               script-binding uosc/open-config-directory
R               script-message-to uosc show-submenu "Utils > Aspect ratio"
alt+s           script-binding uosc/load-subtitles

menu            script-binding uosc/menu
.               frame-step; script-binding uosc/flash-timeline
,               frame-back-step; script-binding uosc/flash-timeline
right           seek  3; script-binding uosc/flash-timeline
left            seek -3; script-binding uosc/flash-timeline

m               cycle mute
up              add volume  5
down            add volume -5
[               add speed -0.25
]               add speed  0.25
\               set speed 1
>               script-binding uosc/next; script-message-to uosc flash-elements top_bar,timeline
<               script-binding uosc/prev; script-message-to uosc flash-elements top_bar,timeline
```
