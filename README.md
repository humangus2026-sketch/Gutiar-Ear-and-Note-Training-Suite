# The Rising Resonance Suite

An interactive, hands-free web application designed for guitarists to bridge the gap between their ears, their minds, and the fretboard. By leveraging modern **Web Audio API Real-Time Pitch Detection**, this suite listens to your actual guitar signal (via any connected audio input or your device's internal microphone) and uses your own recorded instrument samples to validate your playing in real time.

Built to be completely hands-free, the application utilizes the **Keyboard Spacebar** to navigate menus and trigger training loops, allowing you to keep both hands on your guitar neck at all times.

---

## 🚀 Core Modules

### 1. Functional Ear Training (Contextual Loop)
Unlike isolated interval trainers, this module teaches you to hear notes relative to a key center (Moveable Do). 
* **How it works:** Choose a specific key or select **"Randomize Key Each Note"** to test your adaptability. Press the **Spacebar** to begin a 5-note round. 
* **The Flow:** The app plays an authentic $I - IV - V - I$ block triad cadence using your raw guitar samples to anchor your ears, pauses for 3 seconds, and then plucks a mystery scale degree. Find the note on your guitar (optimized for Frets 0–5) and play it. 
* **Automation:** The moment you strike the correct note, the app automatically advances, tracks your accuracy out of 5, and spins up the next cadence loop.

### 2. Fretboard Note Flashcards
Perfect for beginner and intermediate players learning note names and structural fret locations.
* **How it works:** Press the **Spacebar** to draw a random note name card (e.g., "Find and play a G note!"). 
* **The Flow:** Locate that pitch anywhere within the lower register of the neck (Frets 0–5) and pluck it. The real-time processing engine validates the note name instantly, moving forward when you nail the match.

### 3. Chromatic Guitar Tuner
A precision microtonal tuning utility running on high-accuracy auto-correlation algorithms.
* **How it works:** Pluck any open string cleanly to view your exact frequency in Hertz ($\text{Hz}$) and dynamic microtonal deviation ($\pm50\text{ cents}$). A responsive visual needle helps you calibrate your intonation before jumping into practice modules.

---

## 💻 Running the App on Your Computer

Web browsers enforce strict security boundaries regarding audio inputs. To grant microphone permissions locally on your machine, the file must be opened via a secure web server context rather than a raw hard drive file path (`file:///`).

### Method A: Run via GitHub Pages (Easiest)
1. Go to your repository **Settings** tab on GitHub.
2. Click **Pages** on the left menu.
3. Set the source branch to **`main`** (or `master`) and click **Save**.
4. Launch the secure `https://[your-username].github.io/[your-repo-name]/` link provided at the top of the screen in Google Chrome or Microsoft Edge.

### Method B: Local Server Preview (VS Code)
1. Open the project folder in **Visual Studio Code**.
2. Install the **Live Server** extension.
3. Open `index.html` and click **"Go Live"** in the bottom right corner of your window to run the app instantly on `http://127.0.0.1:5500`.

---

## ⚙️ Audio Input Optimization

* **Audio Interface Users:** Ensure your interface or instrument input channel is selected as your computer's default system audio input device before clicking **"Enable Audio Input"**.
* **Internal Microphone Users:** Position your laptop or device microphone directly facing your acoustic guitar soundhole or amplifier speaker cabinet.
* **Noise Gate Calibration:** The algorithm features a built-in input noise threshold gate set to `0.03` RMS to block out background room hums. If your environment is noisy or your pickups have lower output, you can tweak the `autoCorrelate` threshold variable inside the script code.

---

## 📝 License

This project is open-source and intended for custom community music education development. Play hard, practice smart, and expand your resonance.
