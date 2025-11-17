PulseCam – Fingertip Heart Rate, Breathing & Stress Estimator

PulseCam is an iOS wellness-focused app that measures heart rate, respiratory rate, and stress level using only the rear camera + flashlight and a finger placed on the lens.

This project was fully built in SwiftUI, using AVFoundation for camera access and custom algorithms for physiological signal analysis.

🚀 Features
❤️ Heart Rate Estimation

Uses camera-based photoplethysmography (PPG)

Peak detection + smoothing + RR interval filtering

Clean & friendly UI with real-time live waveform

🌬 Respiratory Rate (Breaths/Min)

Estimated from slow variations in the PPG waveform

Includes smoothing and peak detection to provide stable values

Automatically displayed when signal is strong

😌 Stress Score (1–100)

Derived from Heart Rate Variability (HRV)

Uses RMSSD (Root Mean Square of Successive Differences)

Adjusted with heart rate zones

Displayed with color-coded levels (Low / Medium / High)

📊 History

All measurements are stored on-device

History includes:

BPM

Respiratory rate

Stress score

Timestamp

Duration

Automatically persisted using UserDefaults (Codable)

🟢 Real-Time Waveform

Green live PPG waveform

Shows amplitude and pulse patterns

Helps user understand signal quality

📸 Camera Preview Inside the Circle

Updated to display the camera feed inside a circular mask

Shows what the camera “sees” under the finger

🧠 How It Works

PulseCam uses the phone’s camera + flash to detect tiny changes in light absorption caused by blood flow in your fingertip.

Green-channel intensity is tracked frame-by-frame

Data is smoothed

Peaks (heartbeats) are detected

RR intervals → BPM

RR variability → stress score

Slow waveform oscillations → respiratory rate

This technique is non-medical and for wellness use only.

🛠 Project Structure

PulseCam/
│
├── PulseCamApp.swift            # App entry point
├── Models/
│   └── Measurement.swift        # Model stored in history
│
├── ViewModels/
│   └── MeasureViewModel.swift   # Heart/Resp/Stress logic
│
├── Services/
│   └── CameraService.swift      # AVFoundation camera handler
│
├── Views/
│   ├── HomeView.swift
│   ├── MeasureView.swift
│   ├── WaveformView.swift
│   └── HistoryView.swift
│
└── Assets.xcassets               # App icons and colors


📦 Additional Files Included

You may include in the repository (if available):

Xcode project folder (PulseCam.xcodeproj)

App Icon files

Design mockups (Sketch/Figma) (optional)

Notes or diagrams about PPG processing (optional)

Keynote slides (optional)

Mention these in your repo if you added them.

🧪 Requirements

iOS 16+

Swift 5+

Xcode 15+

Physical iPhone device (camera required)

Flashlight access

📥 Installation

Clone the repository:

git clone https://github.com/yourusername/PulseCam.git


Open:

PulseCam.xcodeproj


Run on a physical iPhone
(App does not work on the simulator—camera + flash required.)

⚠️ Disclaimer

PulseCam is not a medical device.
All values are estimates and should not be used for diagnosis.

👨‍💻 Author
Amirreza Jamshidi
