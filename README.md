# Foreign-Object-Debris-FOD-Detection-Using-Computer-Vision

Project Overview:

This project addresses the critical problem of Foreign Object Debris (FOD) on airbase runways. FODs—such as pins, caps, stones, and metal fragments—pose serious risks to aircraft safety and operations. This solution utilizes computer vision and deep learning, combined with a cost-effective hardware setup, to detect and classify FODs in real time.The system uses the YOLOv8 Nano object detection model along with ESP32 CAM hardware to ensure continuous monitoring of runways, thereby enhancing operational safety and reducing maintenance costs.

Technologies Used:

     Deep Learning Framework: YOLOv8 (Nano)

     Programming Language: Python

     Libraries: Ultralytics YOLOv8, OpenCV, NumPy

     Hardware: ESP32 CAM, CH340 FTDI USB Module

     Image Annotation Format: YOLO

     Development Environment: Google Colab or Local Machine

     Dataset: Custom dataset with over 4000 annotated images

Objectives:

       Automate the detection and classification of Foreign Object Debris (FOD) on airbase runways

      Prevent aircraft damage through reliable and real-time monitoring

      Provide a low-cost, efficient system using embedded hardware

      Develop a scalable framework for integrating object detection with edge devices

Methodology:

      Dataset Preparation
         
          A dataset of 4000+ images of various FODs was created.

          Images were annotated in YOLO format with bounding boxes and class labels.

          The dataset was split into training, validation, and testing sets.

    Model Selection and Training
    
          YOLOv8 Nano was selected for its efficiency and speed on edge devices.

          Training was conducted for 100 epochs with 416x416 input image size.

          Data augmentation techniques (flipping, scaling, color jittering) were applied.

          Model configuration was managed via a .yaml file.

    Evaluation Metrics
    
           Box Loss (bounding box accuracy)

           Class Loss (object classification accuracy)

           DFL Loss (Distribution Focal Loss for precise bounding box regression)

           Precision and Recall

           Confusion matrix for overall model accuracy

      Hardware Integration
      
              Components Used
          
              ESP32 CAM WiFi Module

              CH340 FTDI USB Module (for programming the ESP32)

       Real-Time Detection Process
  
              ESP32 CAM captures images of the runway in real time.

              Images are sent over a local IP address to a host system.

              The YOLOv8 model processes the images and detects any FOD present.

              Bounding boxes are drawn around detected objects and results are displayed.


Note: The ESP32-CAM module was utilized with a general-purpose image streaming and capture code. No specific custom code was developed for the hardware, as the standard setup was sufficient for the application.


Results:

        The model achieved a detection accuracy of 99.4% on the test dataset.
        
        Consistent training and validation performance across epochs indicate robust generalization.
        
        Real-time detection of multiple FODs such as pen caps, pins, and wires was successfully demonstrated using the ESP32 CAM module.
        
        Captured images are automatically processed and displayed with bounding boxes indicating detected objects.

Conclusion:

    This project demonstrates a robust, low-cost solution for real-time FOD detection using YOLOv8 and embedded hardware. By automating the process of identifying hazardous objects on runways, the system significantly improves aircraft safety and reduces maintenance costs.
    
    The system uses standard hardware and software integration techniques. The ESP32-CAM module was implemented using general-purpose streaming code without any customized firmware, making the solution easy to replicate and cost-effective.

Future Enhancements:

   Integrate automated FOD removal mechanisms
   
   Enhance classification by including material-type identification (e.g., metal vs plastic)
   
   Expand deployment to larger airfields using UAVs or drone-based monitoring systems
  
   Improve real-time alerting systems and integrate with airport safety infrastructure
