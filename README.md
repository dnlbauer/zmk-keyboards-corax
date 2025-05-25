# ZMK Module: Corax Keyboard

This repository contains shield files for the [Corax Keyboard](https://github.com/dnlbauer/corax-keyboard).
It can be used to build the zmk firmware for the keyboard.

**Example user config**: For a usage example, see my [Corax keyboard configuration](https://github.com/dnlbauer/corax-zmk-config)

## Supported Keyboards:
Supports the Corax56 and Corax54 keyboard variants.

**Hardware**: [Corax Keyboard Repository](https://github.com/dnlbauer/corax-keyboard)

## Usage

Edit your west.yaml file found in your zmk config's config directory to add the corax module.

Example:
```yaml
manifest:
  remotes:
    - name: dnlbauer
      url-base: https://github.com/dnlbauer
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: zmk-keyboards-corax
      remote: dnlbauer
      revision: main
  self:
    path: config
```

## More Info

For more info on modules, you can read through  through the [Zephyr modules page](https://docs.zephyrproject.org/3.5.0/develop/modules.html) and [ZMK's page on using modules](https://zmk.dev/docs/features/modules). [Zephyr's west manifest page](https://docs.zephyrproject.org/3.5.0/develop/west/manifest.html#west-manifests) may also be of use.
