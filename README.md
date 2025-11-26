
# 👁️ ClearPath - Custom Object Detection & Distance Estimation for the Visually Impaired

ClearPath is a real-time object detection and distance estimation system designed to assist visually impaired individuals. It uses a **YOLOv8s** model trained on a **custom dataset of 25 objects**, with verbal announcements to alert the user of nearby objects and their distance.

## 📦 Requirements

- Python 3.8+
- Jupyter Notebook (for interactive exploration)
- A webcam (for real-time video input)
- Virtual environment (recommended)

## 📁 Custom Dataset

This project **does not rely on COCO**. Instead, we created and labeled our **own dataset** containing 25 commonly encountered objects by visually impaired individuals, such as:

[Chair, Lamp, TrashBin, Tree, Car, Crosswalk, Person, Motorcycle, Bicycle,
TrafficLight, CrossSign, Dog, Wall, Bus, Cat, Barrier, DeliveryBox, FireHydrant,
FallenSign, Fence, Hole_in_the_road, Road_cone, Open_manhole, Road_workahead, shopping_cart]

- Dataset Annotation Tool: [LabelImg](https://github.com/tzutalin/labelImg)
- Dataset Split: Train/Validation (80/20)
- Image Size: 640x640
- Model: YOLOv8s
- Epochs: 100


## 🛠️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/AyoubFanaoui/clearPath.git
cd clearPath
```

### 2. Create a Virtual Environment + Jupyter Kernel

```bash
python -m venv YoloEnv
source YoloEnv/bin/activate  # On Windows use: YoloEnv\Scripts\activate

pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=YoloEnv --display-name "Python (YoloEnv)"
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## 💡 Notes

- The webcam will open and start detecting objects. The system will verbally announce nearby objects and estimate their distance.
- Press **Q** to exit the detection window.
- Focal length is currently set to 462 — for better accuracy, calibrate it using known objects and distances.
- The app estimates distance based on the object's width in pixels and real-world width.

## 📷 Use Cases

- Assistive technology for visually impaired individuals
- Real-time object detection and voice guidance
- Smart navigation for robotics and embedded systems




