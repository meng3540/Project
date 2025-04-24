**New Concepts and Skills Learned**
Throughout this project, I gained hands-on experience with GPU-accelerated computer vision on embedded systems. I learned how to work with the Jetson Orin Nano, including how to configure it, install CUDA-compatible libraries, and set up a Docker-based deep learning environment. I also learned how to run YOLOv5 for real-time object detection using pre-trained models, and how to monitor GPU utilization using jtop.

Additionally, I gained familiarity with tools and workflows that I had never used before, such as VSCodium, Chromium via Snap, and NVIDIA's TensorRT ecosystem. I applied and improved my skills in Linux command-line usage, Python scripting, and system troubleshooting, which are all applicable to my future studies in robotics, AI, and any role involving embedded systems or edge computing.

**Project Successes and Effective Strategies**
One of the biggest successes was getting real-time YOLOv5 inference running on the GPU of the Jetson Orin Nano. The strategy of using pre-validated, JetPack-compatible PyTorch wheels and following Ultralytics' recommended workflow allowed me to avoid many compatibility issues. I maintained a clear, step-by-step installation log, which proved essential for debugging and reproducibility.

**Challenges and My Individual Contribution**
 I encountered several challenges throughout the project, such as:
Inability to access the camera through OpenCV initially
OpenCV not being CUDA-enabled
PyTorch not recognizing the GPU
Compatibility mismatches with NumPy and system packages


To address these, I researched and applied solutions individually. For example, I diagnosed the OpenCV-CUDA issue and proposed removing pip-installed versions in favor of the JetPack system version. I also played a key role in verifying GPU usage through tegrastats and jtop, and iteratively updated the setup process to be beginner-friendly. I documented every step, ensuring the entire setup could be reproduced on a fresh device with no prior configurations.

**Learning Plan**
By doing this project, I identified areas where my skills and abilities were lacking extension. One of the key pieces missing was being more aware in terms of TensorRT as well as in changing the PyTorch model into ONNX and TensorRT forms, as a pre-requisite to AI model optimization on the edge device. I also recognized that I must improve my capability to deploy and manage Docker containers for GPU workloads, especially for real-time applications. To expand this solution to an extended or industrial-level deployment, I would need to learn more about creating efficient data pipelines, handling multiple video streams, and performing real-time analytics under hardware limitations. To bridge such gaps, I plan to make use of training tools such as NVIDIA Deep Learning Institute (DLI) to train on Jetson optimization, TensorRT, and DeepStream. Furthermore, I will use official documentation as well as community-led tutorials in Ultralytics and JetsonHacks to widen my expertise in embedded AI development. These steps will equip me with the knowledge and expertise to build robust, scalable, and efficient AI applications on edge devices like the Jetson Orin Nano.
