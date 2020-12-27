# Tensorflow Lite Object Detection on Raspberry Pi

This project is about setting up a Raspberry Pi 4 with a Raspberry Pi camera and
TensorFlow lite. Please check the TensorFlow-Lite-Object-Detection repository linked at the end of this document.

I did perform following steps to setup the Tensorflow Lite Object Detection on my Raspberry Pi 4:

    python3 -m venv tflite1-env
    source tflite1-env/bin/activate
    bash get_pi_requirements.sh
    wget https://storage.googleapis.com/download.tensorflow.org/models/tflite/coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip
    unzip coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip
    python3 TFLite_detection_webcam.py --modeldir=model`

I did use the following command to check whether the Raspberry Pi camera is working.

    vcgencmd get_camera

Furthermore, as I was not using the pi user, add had to grant following rights to the user which is execution the Tensorflow Lite Object Detection.

    sudo adduser tfuser gpio
    sudo adduser tfuser video
    xhost +localhost`

https://github.com/EdjeElectronics/TensorFlow-Lite-Object-Detection-on-Android-and-Raspberry-Pi/blob/master/Raspberry_Pi_Guide.md
