# ZMK Firmware: Personal fork

This is @theol0403's personal ZMK fork containing various experimental features.
It is based on [urob's fork](https://github.com/urob/zmk/tree/main).

Below is a list of features currently included in the `main` branch _on top of_
the official ZMK master branch.

**Theo's fork:**

- **dynamic-macros** (PR [#1351](https://github.com/zmkfirmware/zmk/pull/1351))
- **hold-while-undecided** (PR
  [#1811](https://github.com/zmkfirmware/zmk/pull/1811))
- **deactivate sticky keys on release** (PR
  [#1788](https://github.com/zmkfirmware/zmk/pull/1788))
- **lazy-sticky-keys** (PR
  [#1812](https://github.com/zmkfirmware/zmk/pull/1812))
- **partial-holds** (PR [#1809](https://github.com/zmkfirmware/zmk/pull/1809))

**Urob's fork:**

- **mouse** (PR [#778](https://github.com/zmkfirmware/zmk/pull/778)) - official
  PR + ftc's changes +
  [fixes needed for Zephyr 3.2](https://github.com/urob/zmk/tree/mouse-3.2) +
  safeguads + always use hog device
- **swapper** (PR [#1366](https://github.com/zmkfirmware/zmk/pull/1366)) -
  official PR + fixes needed for Zephyr 3.2
- **global-quick-tap-ms** (PR
  [#1387](https://github.com/zmkfirmware/zmk/pull/1387)) - official PR
- **smart-word** (PR [#1451](https://github.com/zmkfirmware/zmk/pull/1451)) -
  official PR, updated to Zephyr-3.2
- **fix-key-repeat** - fix
  [key-repeat rolling issue](https://github.com/zmkfirmware/zmk/issues/1207) by
  Andrew Rae
- **on-release-for-tap-preferred** -
  [on-release feature for tap-preferred](https://github.com/celejewski/zmk/commit/d7a8482712d87963e59b74238667346221199293)
  by Andrzej
- **adv360pro** - driver +
  [alternate matrix transform](https://github.com/urob/adv360-demo-config#alternate-matrix-transform)
- **zen-tweaks** -
  [display & battery improvements](https://github.com/caksoylar/zmk/tree/caksoylar/zen-v1%2Bv2)
  by Cem Aksoylar

In order to use this branch with Github Actions, replace the contents of
`west.yml` in your `zmk-config/config` directory with the following contents:

```
manifest:
  remotes:
    - name: theol0403
      url-base: https://github.com/theol0403
  projects:
    - name: zmk
      remote: theol0403
      revision: main
      import: app/west.yml
  self:
    path: config
```
