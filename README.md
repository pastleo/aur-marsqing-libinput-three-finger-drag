# aur-marsqing-libinput-three-finger-drag
AUR of https://github.com/marsqing/libinput-three-finger-drag

## Installation & Setup

```
git clone https://github.com/pastleo/aur-marsqing-libinput-three-finger-drag.git
makepkg -si

usermod -a -G input {user}
# reboot/re-login might be needed

systemctl --user start libinput-three-finger-drag # see if it works
systemctl --user enable libinput-three-finger-drag # auto-start at login
```

## Configuration

to set cursor acceleration during dragging, set `LIBINPUT_THREE_FINGER_DRAG_ACC` (default: `1.4`) environment variable, eg in `/etc/environment`:

```
LIBINPUT_THREE_FINGER_DRAG_ACC=4
```

using `:0` as `DISPLAY` by default, set `LIBINPUT_THREE_FINGER_DRAG_DISPLAY` if needed
