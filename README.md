🏓 Pickleball Video Analysis 🎥
📌 Introduction
Welcome to Pickleball Video Analysis, an advanced tool for tracking player movement, ball shot speed, and in-game statistics using cutting-edge computer vision and machine learning techniques. This project analyzes pickleball matches to provide actionable insights into player performance, speed, and court positioning.

✨ Features
✅ Player & Ball Detection 🎯

Uses YOLO v8 for highly accurate player detection.
Fine-tuned YOLOv5 for precise pickleball tracking.
✅ Court Mapping & Visualization 🎾🏟️

Generates a "mini court" visualization showing player & ball positions in real-time.
✅ Comprehensive Speed Analysis ⚡📊

Ball Shot Speed: Measured in km/h for each shot.
Player Movement Speed: Tracks movement both while receiving shots and throughout the match.
Total Distance Covered: Calculates how far each player moves during the game.
✅ Advanced Match Statistics 📈📊

Shot Count: Number of shots played by each player.
Receiving Positions: Tracks where players receive the ball.
Court Positioning Data: Helps analyze gameplay patterns.
🔬 Methodology
🏎️ Speed Calculation Approach
1️⃣ Shot Detection

Identifies frames where the ball is hit.
Determines which player hit the ball based on proximity.
2️⃣ Distance Calculation

Converts pixel distances to real-world meters using court dimensions.
Uses standard pickleball court width: 6.10 meters (20 feet).
3️⃣ Speed Calculation Formula

Ball Speed:
Speed
=
Distance in meters
Time in seconds
×
3.6
Speed= 
Time in seconds
Distance in meters
​
 ×3.6
(Converts m/s to km/h)
Player Speed:
Tracks movement between shots & frame-by-frame to determine total distance traveled.
🏟️ Court Dimensions (Reference)
This project follows USA Pickleball Association standard court dimensions:

📌 Court Width: 6.10 meters (20 feet)
📌 Court Length: 13.41 meters (44 feet)
📌 Non-Volley Zone (Kitchen): 2.13 meters (7 feet)
📌 Full reference can be found in constants/__init__.py.

⚙️ Requirements
📌 Python 3.8+
📌 OpenCV
📌 PyTorch
📌 Ultralytics (YOLO)
📌 Pandas
📌 NumPy

🔧 Installation

bash
Copy
Edit
pip install -r requirements.txt
🚀 Usage
🔹 Step 1: Place Your Video
Copy your pickleball match video to the input_videos folder and rename it as:

plaintext
Copy
Edit
input_video.mp4
🔹 Step 2: Run the Analysis
Execute the following command:

bash
Copy
Edit
python main.py
🔹 Step 3: View the Results
Your processed match analysis video will be saved in:

plaintext
Copy
Edit
output_videos/
🎬 Example Output
🔹 The output video displays:
✔ Bounding Boxes around detected players & the ball.
✔ Mini-Court Visualization to track game flow.
✔ Detailed Match Statistics Panel:

Shot counts & speeds
Player movement metrics
Average speeds
Total distance covered
🖼️ Example Screenshot:

![image](https://github.com/user-attachments/assets/84674af7-6ee6-48e7-8176-d06df6d7bb8b)



🧠 Model Information
✅ Player Detection: YOLOv8x
✅ Ball Detection: Fine-Tuned YOLOv5 Model
✅ Court Line Detection: Custom Keypoint Detection Model
