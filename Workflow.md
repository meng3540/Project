# Workflow
The system architecture consists of four core components: input acquisition via a USB webcam, real-time image processing and inference using the YOLOv5 object detection model on the Jetson Orin Nano GPU, output visualization through an HDMI-connected display, and monitoring tools for GPU resource usage. The data flow begins with continuous frame capture from the webcam, which is then passed to the YOLOv5 pipeline. The frames undergo necessary preprocessing before being fed into the model for inference. Post-processing includes drawing bounding boxes and class labels on detected objects, with the annotated frame displayed in real time.
# System Block Diagram
```[USB Camera] --> [OpenCV Frame Capture] --> [YOLOv5 Inference (GPU)] --> [Bounding Box & Label Overlay] --> [Display]```
# Workflow Outline
The project workflow to implement and test the object detection pipeline on the Jetson Orin Nano involved the following structured sequence:

System Preparation: The Jetson Orin Nano was connected to a monitor, power supply, keyboard, and mouse. WiFi was configured using nmcli to allow internet access for package installation.

Package Installation: Essential packages such as python3-pip, git, v4l-utils, wget, and curl were installed, along with snapd for managing sandboxed applications. Chromium and Codium (VS Code alternative) were installed via Snap for browser access and code editing.

Camera Validation: Using /dev/video*, the available video devices were listed and validated using a short OpenCV Python script. Additional testing was done with nvgstcapture-1.0 to verify NVIDIA camera capabilities.

YOLOv5 Setup: The official YOLOv5 repository was cloned, and its requirements were installed. The small model yolov5s.pt was downloaded from Ultralytics’ release page.

PyTorch and Torchvision Installation: PyTorch and Torchvision were installed using pre-compiled Jetson-compatible wheels that support CUDA.

CUDA Optimization Packages: CUDA-specific libraries like libcusparselt and onnxruntime-gpu were installed to enable potential future optimization and deployment extensions.

Monitoring Tools: jetson-stats and jtop were installed and used to monitor GPU resource utilization during inference.

Object Detection Execution: The YOLOv5 detection script was run using both Python terminal calls and programmatically from within Codium. Detection used the live camera feed (source=0) and executed fully on the GPU (device=0).
