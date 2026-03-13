# corne1

ZMK config for a Corne split keyboard on `nice_nano_v2`.

This layout is tuned for macOS and keeps an HHKB-style base layer:

- `Esc` on the top-left
- `Ctrl` to the left of `A`
- `Backspace` on the top-right
- a minimal base layer with symbols and navigation moved to `Layer 2`

## Build Targets

GitHub Actions builds these two artifacts:

- `corne_left_studio`
- `corne_right_studio`

Flash the matching firmware to each half separately.

## Keymap

### Base

```text
Esc    Q    W    E    R    T        Y    U    I    O    P    Bspc
Ctrl   A    S    D    F    G        H    J    K    L    ;    '
Shift  Z    X    C    V    B        N    M    ,    .    /    RShift
             Tab  Alt  Cmd  Space   Enter/Fn  IME
```

Notes:

- `Enter/Fn`: tap for `Enter`, hold for `Layer 2`
- `IME`: `C_AC_NEXT_KEYBOARD_LAYOUT_SELECT`

### Layer 2

```text
`      1    2    3    4    5        6    7    8    9    0    Del
___    F1   F2   F3   F4   F5       Left Down Up   Right -    =
___    F6   F7   F8   F9   F10      Home PgDn PgUp End   [    ]
             \    +    ___  ___      ___   ___
```

`___` means transparent and falls through to the base layer.

## Symbol Coverage

This keymap covers the standard printable keys expected from a US ANSI MacBook layout:

- letters: `A-Z`
- digits: `0-9`
- punctuation: `` ` - = [ ] \ ; ' , . / ``
- shifted symbols such as `! @ # $ % ^ & * ( ) _ + { } | : " < > ?`

For example:

- `!` = `Shift + Fn + 1`
- `+` = `Fn +` the second left thumb key on `Layer 2`
- `|` = `Shift + Fn +` the first left thumb key on `Layer 2`

## Files

- Keymap: `config/corne.keymap`
- Build matrix: `build.yaml`
