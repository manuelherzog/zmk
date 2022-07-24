# ZMK Firmware: Personal fork

This is my personal ZMK fork containing various experimental features. It is regularly
rebased onto the latest upstream. Below is a list of features
currently included in the `main` branch *on top of* the official ZMK master branch.

* **mouse** (PR #778) - ftc's rebase: https://github.com/ftc/zmk/tree/mouse-ftc
* **swapper** (PR #1366) - PR branch: https://github.com/nickconway/zmk/tree/smart-interrupt
* **global-quick-tap-ms** (PR #1387) - PR branch: https://github.com/andrewjrae/zmk/tree/min-prior-ms
* **positional-hold-tap-on-release** (PR #1423) - PR branch: https://github.com/urob/zmk/tree/positional-hold-tap-on-release
* **num-word** (PR #1451) - PR branch: https://github.com/urob/zmk/tree/improve-caps-word
* **adv360pro** (driver + alternate matrix transform) - source: https://github.com/urob/zmk/tree/adv360
* **zen-display-improvements** - source: https://github.com/caksoylar/zmk/tree/caksoylar/zen-v2

In order to use this branch with Github Actions, replace the contents of `west.yml` in
your `zmk-config/config` directory with the following contents:
```
manifest:
  remotes:
    - name: urob
      url-base: https://github.com/urob
  projects:
    - name: zmk
      remote: urob
      revision: main
      import: app/west.yml
  self:
    path: config
```
