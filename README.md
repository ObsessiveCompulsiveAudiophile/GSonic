# GSonic Reference

**Stereo, redefined.**

GSonic Reference is a high-quality speaker and room correction tool that generates precision FIR correction filters from in-room measurements. It combines spatial measurement averaging with advanced filter generation to deliver studio-grade correction for any stereo listening environment.

---

## ✨ Features

- **Integrated Measurement & Filter Generation** — Measure and generate in a single application
- **Spatial Averaging** — Multi-position measurement for robust, position-independent correction
- **Automatic Clock Drift Compensation** — No need for loopback cables or synchronized clocks
- **Low Latency Filters** — 32,768-tap FIR filters at 48 kHz (pure C++ codebase, 341 ms, ~0.34 s processing latency)
- **Stereo Balance** — Perceptual loudness-based stereo balancing
- **Target Curve Support** — Built-in presets or bring your own custom target curves
- **Multiple Output Formats** — Mono (L/R) and interleaved stereo WAV filters for maximum compatibility
- **ASIO & WASAPI Support** — Choose your preferred audio backend on Windows

---

## 📥 Download

**[⬇ Download Latest Release](https://github.com/ObsessiveCompulsiveAudiophile/GSonic/releases/latest)**

| Platform | Download | Audio Backend |
|---|---|---|
| **Windows** | [GSonic-Reference-v1.0-Windows.zip](https://github.com/ObsessiveCompulsiveAudiophile/GSonic/releases/latest) | ASIO + WASAPI |
| **macOS (Apple Silicon)** | [GSonic-Reference-v1.0-macOS-ARM.zip](https://github.com/ObsessiveCompulsiveAudiophile/GSonic/releases/latest) | CoreAudio |
| **macOS (Intel)** | [GSonic-Reference-v1.0-macOS-Intel.zip](https://github.com/ObsessiveCompulsiveAudiophile/GSonic/releases/latest) | CoreAudio |
| **Linux** | [GSonic-Reference-v1.0-Linux.zip](https://github.com/ObsessiveCompulsiveAudiophile/GSonic/releases/latest) | ALSA |

**Installation:** Download the zip for your platform, extract to any folder, and run `GSonic` (or `GSonic.exe` on Windows).

---

## 🚀 Quick Start

### Step 1: Measure

1. Open the **Measure** tab
2. Select your audio backend (**ASIO** recommended, or **WASAPI**)
3. Choose your output device (speakers) and input device (measurement microphone)
4. Set an output folder for measurement files
5. Optionally load a microphone calibration file (`.txt` or `.cal`)
6. Click **Test Sound** to verify audio is working
7. Place your microphone at the **primary listening position, at ear height**
8. Click **Start Measurement** — the app plays a sweep through each speaker
9. Move the microphone to **two more positions** around the primary listening position
10. A total of **3 positions** are measured for spatial averaging

### Step 2: Generate Filters

1. Open the **Generate** tab
2. Browse to the folder containing your measurement WAV files
3. Optionally set an output folder and filter name prefix
4. Choose a **target curve** from the provided presets, or leave on **Auto** for a natural −1 dB/octave tilt
5. Click **Generate Filters**
6. Load the generated filters into your convolution engine (e.g. Equalizer APO, JRiver, Roon, HQPlayer)

---

## 🎯 Target Curves

GSonic Reference ships with several target curve presets in the `targetCurves/` folder. You can also create your own:

- Save a `.txt` file in the `targetCurves/` folder (next to the executable)
- Format: one `frequency_Hz  level_dB` pair per line
- Custom curves **should not** contain bass roll-off — the engine detects speaker roll-off automatically

---

## 💡 Tips

- Use a **calibrated measurement microphone** for best results
- Keep the room **quiet** during measurements
- Set playback level to your **normal listening level**
- **ASIO** is recommended for lowest latency and best clock accuracy
- Generated filters are automatically resampled by your convolution engine if needed

---

## 📋 System Requirements

| | Requirement |
|---|---|
| **Windows** | Windows 10/11 (64-bit) |
| **macOS** | macOS 12+ (Intel or Apple Silicon) |
| **Linux** | Ubuntu 22.04+ or equivalent (64-bit) |
| **Audio** | Any compatible audio interface |
| **Microphone** | Measurement microphone recommended (e.g. UMIK-1, EMM-6) |

---

## 📄 License

GSonic Reference is **free for personal, non-commercial use**.  
Commercial use requires written permission. See [LICENSE](LICENSE) for details.

---

## 🔗 Links

- **Video Tutorial**: [youtube.com/@ocaudiophile](https://youtube.com/@ocaudiophile)
- **Issues & Feedback**: [GitHub Issues](https://github.com/ObsessiveCompulsiveAudiophile/GSonic/issues)
