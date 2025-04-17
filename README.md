
# Squat Analysis with MediaPipe

![squat_with_feedback 00_00_03-00_00_09](https://github.com/user-attachments/assets/72925d06-ca1b-4e96-9e63-90489075f5b4)


## 📌 Overview
This project uses **MediaPipe Pose Estimation** to analyze squat form in real-time or from video files. It provides:
- Squat repetition counting
- Real-time form feedback
- Improper movement detection
- Video output with visual feedback

## 🛠️ Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/FarzadMalik/squat_analysis_with_python_and_mediapipe.git
   cd squat-analysis
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
   *(or)*  
   ```bash
   pip install opencv-python mediapipe numpy
   ```

## 🚀 Usage
### Basic Analysis
```bash
python squat_analysis.py --input squat.mp4 --output squat_with_feedback.mp4
```

### Command Line Options
| Argument | Description | Default |
|----------|-------------|---------|
| `--input` | Input video file | `squat.mp4` |
| `--output` | Output video file | `squat_with_feedback.mp4` |
| `--show` | Display real-time analysis | `False` |
| `--strict` | Enable strict form checking | `False` |

### Key Features
- **Rep Counting**: Automatically counts squat repetitions
- **Form Feedback**:
  - "Knees too forward!" - When knees extend past toes
  - "Leaning too much!" - Excessive forward torso lean
  - "Good form!" - When form is correct
- **Depth Analysis**: Detects partial vs. full squats

## 📊 Output Example
```
Frame 120: Count: 5, Knee Angle: 89°, Feedback: Good form!
Frame 121: Count: 5, Knee Angle: 92°, Feedback: Stand tall
```

## 🧠 How It Works
1. **Pose Detection**: Uses MediaPipe to identify 33 body landmarks
2. **Angle Calculation**:
   - Hip-Knee-Ankle angle for squat depth
   - Shoulder-Hip-Knee angle for torso position
3. **Form Analysis**:
   - Compares angles against biomechanical thresholds
   - Provides real-time feedback

## 📂 File Structure
```
squat-analysis/
├── main.ipynb                  # Main analysis script
├── requirements.txt            # Dependencies
├── squat.mp4                   # Sample input
├── squat_with_feedback.mp4     # Sample output
└── README.md                   # This file
```

## 🤝 Contributing
1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📜 License
Distributed under the MIT License. See `LICENSE` for more information.

## ✉️ Contact
Farzad Malik - anpmlk6@qq.com  
Project Link: [https://github.com/yourusername/squat-analysis]([https://github.com/yourusername/squat-analysis](https://github.com/FarzadMalik/squat_analysis_with_python_and_mediapipe))



