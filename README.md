https://drive.google.com/drive/folders/1xj4Shv7RzdGfZBytM1vIjK7SAM4Eo0vO?usp=sharing
go to this link and take the file paste in folder in which you are simulating  YOU WILL GET HERE YOLO WEIGHTS TAKE IT AND PLACE WHERE ABOVE FILES YOU HAVE PLACED



Python Security Camera with WhatsApp Alerts 📹🚨
This project transforms a standard webcam into a smart security camera using Python and OpenCV. It leverages the powerful YOLOv3 object detection model to identify specific objects (like a person) in real-time. When a target object is detected, the script automatically sends a security alert to a specified phone number via WhatsApp, complete with a snapshot, timestamp, and approximate location.

Features ✨
Real-Time Object Detection: Uses the YOLOv3 model for fast and accurate detection.

Customizable Alerts: You can configure which object triggers an alert (e.g., person, car, dog).

Rich WhatsApp Notifications: Alerts include a snapshot of the event, the time of detection, and a Google Maps link to the approximate location.

Spam Prevention: A built-in cooldown timer prevents the script from sending too many alerts in a short period.

Reliable Messaging: Uses pyautogui to ensure WhatsApp messages are sent successfully, even on slower systems.

Easy Configuration: All settings are centralized in a single CONFIG dictionary for easy modification.

How It Works ⚙️
The script follows a simple but effective workflow:

Initialize: The script loads the pre-trained YOLOv3 model and starts the webcam.

Capture & Process: It captures video frames one by one from the webcam.

Detect: Each frame is passed to the YOLO model to detect all objects present.

Verify: The script checks if the pre-defined TARGET_OBJECT (e.g., "person") is among the detected objects.

Trigger Alert: If the target is found and the cooldown period has passed:

A snapshot of the current frame is saved as a JPG image.

The script fetches the public IP address to get an approximate location.

pywhatkit is used to open WhatsApp Web in Chrome and pre-fill the message with the caption and image.

pyautogui takes control to press "Enter" to send the message and then closes the tab, ensuring reliable delivery.

Loop: The process repeats, providing continuous monitoring.

Prerequisites 📋
Before you begin, ensure you have the following:

Python 3.x (v3.11 is recommended as used during development).

A webcam connected to your computer.

A WhatsApp account.

Google Chrome installed, with WhatsApp Web already logged in.

Installation and Setup 🛠️
Follow these steps to get your security camera up and running.

Step 1: Clone the Repository
Open your terminal or command prompt and clone the project repository.

Bash

git clone https://github.com/UtkarshTripathiCv2/AI-Security-Camera.git
cd AI-Security-Camera
Step 2: Install Required Python Libraries
Install all the necessary libraries using pip.

Bash

pip install opencv-python numpy requests pywhatkit pyautogui
Step 3: Download YOLOv3 Model Files
The main model file (yolov3.weights) is too large to be stored on GitHub. You must download it separately.

Download the files from this Google Drive Link:

Download YOLOv3 Files Here

IMPORTANT: Place the following three files directly into the project folder (the same directory where the Python script is located):

yolov3.weights (the large model file)

yolov3.cfg (the model configuration)

coco.names (the list of detectable object names)

Step 4: Configure the Script
Open the Python script in an editor and modify the CONFIG dictionary at the top.

Python

CONFIG = {
    # --- Detection Settings ---
    "TARGET_OBJECT": "person",

    # --- WhatsApp Alert Settings ---
    "PHONE_NUMBER": "+91XXXXXXXXXX",    # <<< CHANGE THIS!
    "SEND_COOLDOWN": 60,
    
    # --- PyAutoGUI Timings (Adjust if WhatsApp Web is slow) ---
    "PYWHATKIT_WAIT_TIME": 25,
    "BROWSER_LOAD_DELAY": 12,
    # ... other settings
}
PHONE_NUMBER: This is the most important setting. Replace "+91XXXXXXXXXX" with the full phone number you want to send alerts to. It must include the country code with a + and have no spaces (e.g., +14155552671).

TARGET_OBJECT: (Optional) By default, it detects a "person". You can change this to any other object listed in the coco.names file (e.g., "car", "cat", "dog").

Usage ▶️
Prepare WhatsApp Web: Open Google Chrome and make sure you are logged into WhatsApp Web. Leave this browser tab active and visible before running the script. The program needs to interact with this window.

Run the Script: Open your terminal, navigate to the project directory, and run the following command:

Bash

python security_camera.py
(Assuming you have named the file security_camera.py)

Monitor: A window titled "Security Feed" will appear, showing your live webcam feed. Detected objects will be highlighted with bounding boxes.

Stop the Script: To shut down the program, click on the "Security Feed" window to make it active, and then press the 'q' key on your keyboard.

Troubleshooting ❓
Error: CRITICAL: Please set your phone number...

You forgot to change the PHONE_NUMBER in the CONFIG section. Please update it with a valid number.

Error: FileNotFoundError for YOLO files

This means the script cannot find yolov3.weights, yolov3.cfg, or coco.names. Ensure all three files are downloaded and placed in the exact same folder as the Python script.

WhatsApp message is typed but not sent

Your computer or internet might be slow. Try increasing the time delays in the CONFIG dictionary. Good values to increase are PYWHATKIT_WAIT_TIME and BROWSER_LOAD_DELAY.

Script fails with permission errors (macOS/Linux)

pyautogui needs permission to control your mouse and keyboard. You may need to grant "Accessibility" or "Input Monitoring" permissions to your terminal or code editor in your system's security settings.





or read this


Of course. Here are the installation commands and a concise, updated README file for your project.

Installation Command
Open your terminal or command prompt and run this single command to install all the necessary Python libraries:

Bash

pip install opencv-python numpy requests pywhatkit pyautogui
AI Security Camera with WhatsApp Alerts 📹
This Python script uses your webcam to detect objects in real-time with YOLOv3 and sends an instant security alert to your phone via WhatsApp when a specific object (like a "person") is found.

🚀 Setup & Configuration
1. Get the Code
Clone this repository to your computer:

Bash

git clone https://github.com/UtkarshTripathiCv2/Securitycamerapart2.git
cd Securitycamerapart2
2. Install Libraries
Use the pip command provided at the top of this document.

3. Download the YOLOv3 Model
The main model file, yolov3.weights, is too large for GitHub.

Download yolov3.weights from Google Drive

Place the downloaded yolov3.weights file in the same folder as APPUL.PY. The other model files (yolov3.cfg and coco.names) are already in the repository.

4. Configure the Script
Open the APPUL.PY file and edit the CONFIG section at the top:

PHONE_NUMBER: This is the most important step. Change "+91IAMIRONMAN" to the recipient's full phone number, including the country code (e.g., "+911234567890"). Do not include spaces.

▶️ How to Run
Open WhatsApp Web: Log in to WhatsApp Web in your Google Chrome browser and keep the tab active.

Run the script: Open a terminal in the project folder and run the command:

Bash

python APPUL.PY
Monitor: A "Security Feed" window will open, showing your camera's view.

Stop: To close the program, click on the feed window and press the 'q' key.

⚙️ Troubleshooting
Message Not Sending? If WhatsApp opens but the message doesn't send, your computer might be slow. Try increasing the BROWSER_LOAD_DELAY value inside the CONFIG dictionary in the script.




Author
Utkarsh Tripathi (@JacKALKI)












Tools

