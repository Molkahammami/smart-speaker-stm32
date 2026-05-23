# 🔊 Smart Speaker — STM32F4

> USB WAV audio player with Play/Pause/Next/Previous controls

![STM32](https://img.shields.io/badge/STM32F4-03234B?style=flat&logo=stmicroelectronics&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=flat&logo=c&logoColor=white)
![Altium](https://img.shields.io/badge/Altium_Designer-A5915F?style=flat&logo=altiumdesigner&logoColor=white)

## Overview

A smart audio player built on STM32F407. Reads WAV files from a USB flash drive and plays them via I2S at 44kHz. Three hardware buttons control playback in real time using EXTI interrupts.

## Hardware
| Component | Details |
|---|---|
| MCU | STM32F407VGTx |
| Audio output | I2S3 — Philips standard, 44kHz, 16-bit |
| Audio codec | CS43L22 via I2C1 |
| Storage | USB Host — FAT32 flash drive |
| Controls | 3 push buttons (PA0, PA1, PA2) |
## Features
- WAV file playback from USB flash drive (FatFS)
- Play / Pause / Resume via button interrupt
- Next / Previous track navigation
- LED visual feedback (PD12, PD13, PD14)
- Debounced EXTI interrupt handling
- I2S DMA for zero-CPU audio streaming

## Project Structure
src/
└── main.c         ← USB host, I2S init, button interrupts
docs/              ← Technical report
media/             ← Hardware photos
## Author

**Molka Hammami** — Microelectronics Engineering Student, Tunisia  
[LinkedIn](https://linkedin.com/in/molka-hammami) · [GitHub](https://github.com/Molkahammami)
