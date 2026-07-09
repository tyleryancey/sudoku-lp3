# Sudoku — Light Phone 3 sideload build

A signed APK of the **Sudoku** tool (`dev.tyler.sudoku`), built with the Light SDK for
testing on a real **Light Phone 3**.

> ⚠️ **Unofficial / experimental.** This is a self-signed sideload. Light Phone does not
> yet officially support installing self-built tools on real hardware — LightOS treats
> this as an *unverified* app and will show a privacy/performance warning. Install at your
> own discretion. The Sudoku game itself is fully local: **no network, no permissions.**

## Install on the Light Phone 3

1. Open this page in **Chrome on your LP3** → go to **[Releases](../../releases/latest)**
   → tap **`sudoku-lp3-v1.0.apk`** to download.
2. When prompted, allow Chrome to install apps:
   **Settings → Apps → Chrome → Install unknown apps → Allow**.
3. Open the downloaded APK → **Install**. Acknowledge any LightOS
   "unverified app / dangerous sideload" warning.
4. Launch **Sudoku** from your app list.

## What to expect

- The game is **fully self-contained** — daily puzzles, candidate mode, hints, timer,
  solve chime, and the past-puzzles archive all run locally. It needs no server and
  requests **no permissions**.
- Because it's self-signed, LightOS won't grant it a "tool session token" — but Sudoku
  uses no token-gated features, so it plays normally regardless.
- If it doesn't appear in your launcher after install, that's a known LightOS limitation
  for sideloaded tools (not a bug in the game).

## Build details

|  |  |
|---|---|
| Package | `dev.tyler.sudoku` |
| Version | 1.0 (versionCode 1) |
| serverPackage | `com.lightos` (real LP3 LightOS) |
| minSdk / targetSdk | 33 / 36 |
| Signed with | Light SDK dev key (`lightsdk-dev`), APK Signature Scheme v3 |
| SHA-256 | `9a0bf84983d49b00421226ee674d0c383d07ee187c79f64133d55ba51d7d7be2` |

Built from the private `sudoku-port` branch of the Light SDK. This repo hosts only the
compiled APK for convenient on-device download.
