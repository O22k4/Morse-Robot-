# Morse Code Translation Robot (EV3)

##  Project Overview
This project implements a **Morse Code translator robot** using LEGO EV3. The robot detects signals using **color and distance sensors**, interprets them as Morse code (dots and dashes), and translates them into readable text (A–Z).

The system uses **timing logic and sensor inputs** to distinguish between:
* Dot (`.`)
* Dash (`-`)
* Letter spacing
* Word spacing

The translated message is displayed on the EV3 screen.

---

##  Features
* Detects colors (Red, Black, Green, Yellow, White)
* Uses timer-based logic to differentiate dots and dashes
* Converts Morse code into alphabet letters (A–Z)
* Builds full words and messages dynamically
* Includes movement logic (line-following behavior)
* Stops when obstacle detected (distance < 4 cm)

---

##  How It Works

### 1. Signal Detection
* Uses **Color Sensor (Port 3)** to detect signals
* Color meanings:
  - **Red** → Signal input
  - **Black / Green** → Line following
  - **Yellow / White** → Direction adjustment

---

### 2. Timing Logic
* A timer measures signal duration:
  - Short press → `.` (dot)
  - Long press → `-` (dash)

* Space detection:
  - Short gap → next symbol
  - Medium gap → new letter
  - Long gap → new word

---

### 3. Morse Code Translation
The system maps Morse patterns to letters:

Examples:
* `.−` → A  
* `−...` → B  
* `...` → S  

---

### 4. Message Construction
* Letters are combined into words
* Words are combined into a full message

---

### 5. Movement Control
* Robot adjusts direction based on color detection:
  - Green → move right
  - Black → move left
* Stops when obstacle detected (distance < 4 cm)

---

##  Hardware Requirements
* LEGO EV3 Brick
* 2 × Large Motors
* Color Sensor (Port 3)
* Ultrasonic Sensor (Port 4)

---

##  Software Requirements
* EV3 Classroom (Scratch-based)
* `.lmsp` project file

---

##  How to Run
1. Open EV3 Classroom
2. Import the `.lmsp` file
3. Connect EV3 brick
4. Upload the program
5. Press the start button
6. Provide Morse signals using color/timing

---

##  Known Issues
* Robot may drift off track
* Timing inconsistencies can cause incorrect decoding
* May loop if spacing is not well calibrated

---

##  Improvements
* Add timing calibration
* Improve line-following accuracy
* Add sound output
* Extend to numbers and symbols

---

##  Morse Code Reference (A–Z)

| Letter | Code | Letter | Code |
|--------|------|--------|------|
| A | .- | N | -. |
| B | -... | O | --- |
| C | -.-. | P | .--. |
| D | -.. | Q | --.- |
| E | . | R | .-. |
| F | ..-. | S | ... |
| G | --. | T | - |
| H | .... | U | ..- |
| I | .. | V | ...- |
| J | .--- | W | .-- |
| K | -.- | X | -..- |
| L | .-.. | Y | -.-- |
| M | -- | Z | --.. |

---

##  Notes
* Uses timer-based interpretation of signals
* Combines robotics + communication concepts
* Suitable for educational and demonstration purposes

---
