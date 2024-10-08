# Face Recognition Attendance System

This project implements a face recognition-based attendance system using Python, OpenCV, and the `face_recognition` library. The system identifies individuals based on their facial features, marks their attendance in an Excel file, and updates the total number of days the individual has been present. Attendance is marked only if the individual is identified correctly more than three times in a single session.

## Features

- **Face Recognition**: Identifies individuals based on precomputed face encodings.
- **Attendance Tracking**: Marks attendance in an Excel file with the current date and time.
- **Daily Attendance**: Each person can only mark their attendance once per day.
- **Days Counter**: Tracks the total number of days an individual was present.
- **Real-Time Feedback**: Displays the attendance information in the command prompt when successfully marked.

## Prerequisites

Ensure you have the following libraries installed:

- **Python 3.x**
- **OpenCV** (`opencv-python`)
- **face_recognition**
- **pandas**
- **scikit-learn**
- **openpyxl** (for Excel file handling)


## Project Structure

- **`known_faces/`**: Directory containing subfolders with images of known individuals. Each subfolder is named after the individual's roll number.
- **`encodings.pkl`**: File where the face encodings are precomputed and stored.
- **`attendance.xlsx`**: Excel file where attendance records are stored.
- **`face1.py`**: Script to precompute and save face encodings.
- **`attendance.py`**: Main script for real-time face recognition and attendance marking.
- **`README.md`**: This readme file.

## Usage

### 1. Precompute Face Encodings

Before running the attendance system, precompute the face encodings for the individuals in the `known_faces/` directory:


face1.py

## Notes
1. The system processes every other frame to reduce CPU load, which may improve performance on machines without a dedicated GPU.
2. The face detection model used is HOG, which is more CPU-friendly. For faster processing with a GPU, consider switching to the cnn model in the script.
3. Ensure that the attendance.xlsx file is in the same directory as your script, or adjust the path accordingly.
## Future Enhancements
1. Add functionality for face registration directly through the UI.
2. Implement multi-camera support for larger setups.
3. Integrate with a cloud-based attendance management system.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

**MIT License**

Copyright (c) [2024]

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.