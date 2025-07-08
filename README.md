# Meal Mind AI

Meal Mind AI is a Streamlit web application that uses deep learning to automatically **detect food from images, track calorie and nutrition intake, and visualize your daily progress**. Built for students and health-conscious users, this project leverages computer vision models (YOLO & MobileNetV3) and a simple user-friendly interface.

---

## Features

- User authentication (sign up & log in)
- Personal profile: weight, height, age, gender, activity, dietary goals
- Upload food photos, automatic food recognition & calorie estimation
- Nutrition and calorie tracking (daily logs, progress visualization)
- Local SQLite database for user data and logs
- Dashboard with interactive charts (powered by Altair)

---

## Project Structure

---

meal-mind-ai/
app.py
requirements.txt
models/
final_fruit_mobilenetv3.keras
indo_yolo.pt
mobilenetv3_food41.keras
assets/
sample_images/
...jpg
data/
calorie_tracker.db
nutrition_data.csv
class_lists/
food101_classes.txt
indo_labels.yaml

---

## Installation & Usage

1. **Clone the repository**
    ```bash
    git clone https://github.com/raflyml/meal-mind-ai.git
    cd meal-mind-ai
    ```

2. **Install requirements**
    ```bash
    pip install -r requirements.txt
    ```

3. **Prepare models**
    > Make sure the `models/` directory contains all required pretrained models.  
    > If models are too large for GitHub, host them (Google Drive/Hugging Face) and download them at runtime.

4. **Run locally**
    ```bash
    streamlit run app.py
    ```
    Visit [http://localhost:8501](http://localhost:8501) to open the app.

---

## Deploy to Streamlit Community Cloud

1. **Push this project to your GitHub repository.**
2. Go to [https://streamlit.io/cloud](https://streamlit.io/cloud).
3. Click **"New app"**, select your repo, set the main file as `app.py`, and deploy.
4. If models are large, use a script in `app.py` to automatically download them from your cloud storage before loading.

**Tip:**  
Add any secrets (API keys, etc.) via `.streamlit/secrets.toml` in your repo or from the Streamlit Cloud dashboard.

---

## Example Workflow

1. Sign up and log in.
2. Complete your profile (weight, height, age, etc.).
3. Upload a food image.
4. The app will recognize the food, estimate calories, and add it to your daily log.
5. View your eating history and nutrition insights via the dashboard.

---

## Requirements

- Python 3.8+
- Streamlit
- TensorFlow
- OpenCV
- Ultralytics
- Altair
- Pandas, Numpy, Pillow

(Install all with `pip install -r requirements.txt`)

---

## License

MIT License

---

**Developed by:**  
[Rafly Ramadan]

