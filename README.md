# PiRecall

A lightweight, self-contained Pi memorization tool that runs entirely in a single HTML file. I originally built this for myself to push my own digit memory, and decided to make it public because why not? If I have a good tool, everyone else should have access to it.

**Try it yourself:** [moo2308m.github.io/PiRecall](https://github.io)

---

## Instructions

### Normal Runs & Stats
1. **Start Typing:** Click the input box and type the digits of Pi starting after `3.` (`14159...`). Your timer and typing speed (**WPM**) start automatically as soon as you enter the first digit.
2. **Track Your Progress:** The top bar displays your current **Digits** count, your all-time **Best** score, elapsed **Time**, and live **WPM**.
3. **Mistakes & Giving Up:**
   - **Backspace (`⌫`):** Delete your last typed digit if you hit the wrong key by accident, or use **`Ctrl+Z` / `Cmd+Z`** to undo typed digits.
   - **Don't Know:** If you hit a wall and can't remember what comes next, click **Don't Know** to end the run.
   - **Show Next 5 Digits:** Once a run ends, click **Show Next 5 Digits** to reveal the upcoming digits so you can learn where you got tripped up.
   - **Restart Game:** Click **Restart Game** (or press **`Enter`** / **`R`** after a run ends) to reset the board and start a new attempt.

### Practice Mode & Chunk Drilling
If you don't want to start from `3.` every single time, open **Settings → Recall & Practice**:
- **Practice Mode:** Turn **Practice Mode: On** to drill without affecting your normal personal best record.
- **Chunk Drill (Start From):** Type any decimal position into the **Where to start** box and click **Start Here** to jump straight to that spot in Pi (for example, starting at decimal `#50` or `#100`). Click **Reset to 1** anytime to go back to the beginning.
- **Chunk Sizing:** Choose a preset chunk size (**Off**, **2**, **3**, **4**, **5**, **6**, **8**, **10**) or enter a **Custom** number to group digits into easier-to-read blocks as you type.
- **Visual Chunking Indices:** Toggle **Visual Chunking Indices** on or off to show or hide the position markers above your digit chunks.

### Interactive Background & Audio
The background and audio engine aren't just static decorations—they respond directly to your input, milestones, and music in real time:
- **Click-and-Hold Wave Warping:** Click (or touch) and hold anywhere on the background outside the main card to physically bend, indent, and ripple the shader waves around your cursor. You can adjust how strongly the waves react using the **Hold Indent Depth** slider.
- **Typing & Milestone Pulses:** Every digit you type triggers subtle key chimes and micro-sparks, while hitting chunks, unlocking milestones, or beating your personal best sends shockwaves, particle bursts, and color-reactive pulses across the shader waves.
- **Built-In Procedural Lo-Fi Synth:** Generates endless lo-fi tracks on the fly using the Web Audio API (no MP3s or internet connection required). Every beat is synthesized live with warm electric-piano chords, dusty drum loops, sub-bass, and vinyl crackle—and hitting **New Beat** generates a fresh chord progression and tempo.
- **Real-Time Audio-Reactive Shaders:** With **Wave Sync** turned on, the shader analyzes the live audio output so the waves pulse, swell, and shift brightness in time with the kick drums and chords—whether you're listening to the built-in synth or your own imported songs.
- **Offline Device Audio Support:** Import your own `MP3`, `WAV`, `OGG`, or `M4A` tracks from your device to play inside the website. Imported tracks are stored locally in your browser so they stay available offline, complete with a **Loop** toggle and one-click switching back to the built-in lo-fi synth.

---

## Settings

Click **Settings** in the top-right corner of the card to open the control panel:

### 1. Recall & Practice
- **Practice Mode:** Toggle practice runs on or off.
- **Chunk Drill — Where to start:** Set a custom decimal starting index (**Start Here**) or return to the start (**Reset to 1**).
- **Visual Chunking Indices:** Show or hide chunk index labels.
- **Chunk Size:** Pick from preset group sizes (`Off`, `2`, `3`, `4`, `5`, `6`, `8`, `10`) or set a custom size.

### 2. Effects & Particles
- **Preview Burst:** Trigger a test burst to preview your particle and shader settings.
- **Master Toggle & Master Intensity:** Turn all visual effects on/off or scale every effect slider at once (`0%`–`200%`).
- **Individual Sliders & Toggles:** Fine-tune intensity or toggle each effect separately:
  - **Screen & Card Shake**
  - **PB Fireworks & Confetti**
  - **Shockwaves & Flash**
  - **Milestone Bursts**
  - **Chunk & Key Sparks**
  - **Shader Wave Pulse**

### 3. Background Waves
- **New Seed:** Generate a brand-new procedural wave layout.
- **Waves Toggle:** Turn the animated shader background on or off.
- **Sliders:** Adjust **Wave Speed**, **Wave Scale / Frequency**, **Turbulence & Warp**, **Ribbon Thickness**, **Glow & Brightness**, **Music Reactivity**, **Hold Indent Depth**, and **Wave Color Hue** (`0°`–`360°`).

### 4. Sound & Music
- **New Beat:** Switch to a different procedural lo-fi track (such as *Midnight Tape* at 74 BPM).
- **Lo-Fi Toggle & Wave Sync:** Turn the built-in synth on/off and sync wave pulses to the audio.
- **Mixer Sliders:** Independently adjust **Master Volume**, **Warm Chords & Keys**, **Lo-Fi Drums & Sub**, **Vinyl Crackle**, **Key Chimes (SFX)**, and the **Tape Low-Pass** filter (`Hz`).
- **Offline Music Import (Device Audio):** Click **+ Import Song(s)** to load your own **MP3**, **WAV**, **OGG**, or **M4A** files directly from your device. Imported tracks are saved offline in your browser, with a **Loop** toggle and a **Use Built-in Lo-Fi** button to switch back anytime.

### 5. Milestones
- View all digit milestones and track how many you have unlocked so far.

### 6. Settings Backup & History
- **Undo / Redo:** Step backward or forward through typed digits, setting tweaks, and panel states using the **Undo** / **Redo** buttons or keyboard shortcuts.
- **Export .json / Copy JSON:** Download your full settings and progress as a `.json` file or copy the raw JSON to your clipboard.
- **Import .json:** Restore your saved settings, personal best, and preferences on any browser or device.
- **Reset Defaults:** Wipe custom tweaks and restore the default configuration.

---

## Keyboard Shortcuts

| Key / Shortcut | Action |
| :--- | :--- |
| **`0` – `9`** | Enter the next digit of Pi |
| **`Backspace`** | Delete the last entered digit |
| **`Ctrl + Z` / `Cmd + Z`** | Undo typed digits, setting changes, or panel collapses |
| **`Ctrl + Y` / `Cmd + Shift + Z`** | Redo undone actions |
| **`Enter` or `R`** | Restart the game after a run ends |
