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
