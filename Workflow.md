# Workflow
The system architecture consists of four core components: input acquisition via a USB webcam, real-time image processing and inference using the YOLOv5 object detection model on the Jetson Orin Nano GPU, output visualization through an HDMI-connected display, and monitoring tools for GPU resource usage. The data flow begins with continuous frame capture from the webcam, which is then passed to the YOLOv5 pipeline. The frames undergo necessary preprocessing before being fed into the model for inference. Post-processing includes drawing bounding boxes and class labels on detected objects, with the annotated frame displayed in real time.
# System Block Diagram
```[USB Camera] --> [OpenCV Frame Capture] --> [YOLOv5 Inference (GPU)] --> [Bounding Box & Label Overlay] --> [Display]```
                                                        
