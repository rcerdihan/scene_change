📄 Detailed Report
If you are only interested in the mathematical background, experimental results, and visual outputs, please check out the scene_change_report.pdf file included in the repository.

# Scene Change Detection Using TAD and Custom SVD

This project implements a two-stage video shot boundary detection system using Total Absolute Difference (TAD) and Singular Value Decomposition (SVD). The algorithmic approach is based on the paper by Zhe-Ming Lu and Yong Shi.

## 🌟 Features
- **Two-Stage Detection:** First, it detects candidate scene changes using the TAD method. Then, it tests these candidates using SVD analysis to reduce false positives.
- **Custom SVD Implementation:** The SVD algorithm is implemented from scratch as specified in the project requirements. It is based on the relationship between SVD and Eigenvalue Decomposition.
- **Automated Output:** The script saves detected transition frames as JPG images and lists them in a `transitions.txt` file within a specified output directory.

## ⚙️ How It Works
1. **Frame Extraction:** The video is read frame by frame, and each frame is converted to grayscale to reduce complexity.
2. **TAD Filtering:** The TAD is used as a first filter to detect potential scene changes. For consecutive frames F(i) and F(i+1), the TAD is calculated as the sum of the absolute differences between the pixels of the two frames.
3. **SVD Verification:** The frames initially detected as TAD candidates then move to SVD analysis. The Euclidean distance between the dominant singular values of consecutive frames is computed. If this distance is bigger than a predefined threshold, the scene change is confirmed.

## 🛠️ Technologies Used
- **Python**
- **OpenCV (`cv2`):** For frame extraction and saving images.
- **NumPy:** For matrix operations and custom SVD math.

👨‍💻 Developer
-Regaip Cuma Erdihan
