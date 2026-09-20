# Bias

A tape-machine view for the TASCAM Model 2400, on the Mac. A meter bridge of every channel against the recorder's 24 tracks, a cassette and counter that follow the recorder, Audio Unit inserts on the strips that print to the SD card, a setup per song, markers and takes against the recorder's timecode, MIDI control of the plugins, and an MCP server so an agent can work the session. The 2400's own recorder stays the tape machine; Bias follows it.

This repository holds the downloads and release notes. Bias's source is not published; the "Source code" archives GitHub attaches to each release contain only this README.

**[Download Bias for Mac](https://github.com/Symbia-Labs/bias-releases/releases)** — the newest build is at the top; open the DMG and drag Bias to Applications.

## Requirements

- macOS 13 or later, Apple Silicon (Intel builds later).
- A TASCAM Model 2400 connected to the Mac by USB.
- Audio Unit effects on the Mac for the inserts.

## Installing a beta build

Beta builds are not yet signed or notarized, so macOS refuses the first launch.

1. Open the DMG and drag **Bias** to Applications.
2. Right‑click Bias in Applications and choose **Open**, then **Open** again in the dialog. On macOS 15 and later you can instead launch it once, then go to **System Settings → Privacy & Security**, scroll to "Bias was blocked", and click **Open Anyway**.
3. On first launch macOS asks to let Bias use the **microphone**. Click **Allow**. The inserts run on the 2400's USB channels, which macOS treats as audio input.

## Before using inserts

Each strip's **INPUT SEL** and **REC OUT** switches decide what Bias hears, what the strip plays and what goes to tape.

| Goal | INPUT SEL | REC OUT |
| --- | --- | --- |
| Track through inserts and print them | USB | Off |
| Play back what was printed | MTR | Off |
| Straight input, no inserts | MIC/LINE | Off |

**Never set INPUT SEL to USB with REC OUT on.** The 2400 then sends the strip's USB return back to the Mac, Bias processes its own output, and the strip builds into loud noise. Bias watches for this and mutes the strip's return within a fraction of a second, but keep monitors down the first time you set a strip up.

## Beta terms

Beta builds run as the full Studio tier and stop working on the date shown under the gear at the top right → **License**, when a newer build will be out.

## Reporting a problem

Click the ⚠ at the top right of the app. Your mail app opens with a report to **help@symbia-labs.com** already filled in. Nothing is sent automatically.

---

Bias is an independent product of Symbia Labs and is not affiliated with or endorsed by TEAC Corporation. TASCAM and Model 2400 are trademarks of TEAC Corporation.
