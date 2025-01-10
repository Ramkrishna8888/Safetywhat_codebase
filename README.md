# Safetywhat_codebase

Video Source:
https://youtu.be/Gr0HpDM8Ki8?si=cS2gjW8LLMSQWvMC (Duration : 23 sec, Quality 720p) 

# Hierarchical Object and Sub-Object Detection System
This project implements a robust computer vision system capable of detecting objects and their associated sub-objects in a hierarchical structure. It includes features such as real-time video processing, sub-object image retrieval, and JSON output generation. The system is optimized for inference on CPUs at 10–30 FPS and is modular to accommodate future extensions.

Features
Object and Sub-Object Detection

Detects objects like car, person, tree, road_sign, and their sub-objects (e.g., tires for cars).
Hierarchical association of objects and sub-objects, with unique IDs for each entity.

# JSON Output

Outputs detection results in a hierarchical JSON format:
{
    "object": "car",
    "id": 1,
    "bbox": [x1, y1, x2, y2],
    "subobject": [
        {
            "object": "tire",
            "id": 1,
            "bbox": [x1, y1, x2, y2]
        }
    ]
}
Sub-Object Image Retrieval

Enables retrieval of cropped images for specific sub-objects, such as the tires of a car.
Inference Speed Optimization

Achieves real-time processing with an average of 25 FPS on a CPU.
Modular Design

Easily extendable to add new object-sub-object pairs.
Installation
Prerequisites
Python 3.8 or later
Install required libraries using pip:
pip install -r requirements.txt
TensorFlow or PyTorch (ensure the correct version based on your system's compatibility).
Clone the Repository
git clone https://github.com/your-username/Hierarchical-Detection-System.git
cd Hierarchical-Detection-System
Usage
1. Running the System
To process a video and generate JSON outputs:

python detect_and_generate_json.py --video_path <path_to_video> --output_path <output_json_path>
2. Retrieving Sub-Object Images
To retrieve and save cropped images of sub-objects:

python retrieve_sub_objects.py --object car --subobject tire --video_path <path_to_video>
3. Benchmarking
Run the benchmarking script to evaluate the system's inference speed:

python benchmark.py --video_path <path_to_video>
JSON Output
Example JSON output for a sample frame:

[
    {
        "object": "car",
        "id": 1,
        "bbox": [50, 60, 200, 220],
        "subobject": [
            {
                "object": "tire",
                "id": 1,
                "bbox": [70, 80, 100, 120]
            },
            {
                "object": "tire",
                "id": 2,
                "bbox": [150, 180, 180, 200]
            }
        ]
    },
    {
        "object": "person",
        "id": 2,
        "bbox": [300, 350, 400, 500]
    }
]
