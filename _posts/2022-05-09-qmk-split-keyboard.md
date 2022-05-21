---
title: "One side of QMK split keyboard not working"
---

## Context:

- Creating firmware for a split keyboard with QMK
- Using 2 ATMega32u4 controllers (ItsyBitsy 5v)
- Using `#define MASTER_LEFT` to set handedness

## Symtoms:

- Which ever MCU was connected via USB would detect input. The other would not.

## Working Solution:

- Add `#define SPLIT_USB_DETECT` to config.h

The docs don't seem to mention this clearly, but (from what I can tell) by default both controllers assume they are master. The above option is needed to tell them to check to see if they are master or slave.

Most people set handedness either with a pin or by writing data to EEPROM memory, making this unnecessary. Doing things this way seems much simpler.

ARM controllers have this enabled by default, but ARV controllers do not.

[Further Reading...](https://docs.qmk.fm/#/feature_split_keyboard?id=hardware-considerations-and-mods)


## Questions/search terms that didn't help:

- which is master QMK
- qmk split mode

## Questions/search terms that did help:

- [https://geekhack.org/index.php?topic=102657.0](https://geekhack.org/index.php?topic=102657.0)