# Car Detection From Video

## Setup

1. Clone repository:
    ```bash
    git clone git@github.com:hussainhadi673/Car-Detection-from-Video.git
   
    cd yolov5
    ```

2. Set up environment including all dependencies:
    ```bash
    # Install all requirements
    pip install -qr requirements.txt  # install
    ```

3. Data preparation:
   In order to train the model from scratch, you will need the dataset. Dataset is available on the link 
   https://drive.google.com/file/d/1kICql6ZwK_O0F3otxWQVLzw4UGc-KNJG/view?usp=drive_link

   Download the dataset and paste the zip file in yolov5 folder and then run

    ```bash
    # Unzip all files
    unzip -q video_dataset.zip  # Unzip
    ```

4. Model Training:
   To train the model run
    ```bash
    python train.py --batch 16 --epochs 100 --data dataset.yaml --weights yolov5s.pt --cache
    ```

5. Model Inference:
   To infer from the model run
    ```bash
    python detect.py --weight ./Trained_Model/car_detection_yolov5s.pt --source path/to/video --conf-thres 0.66 --iou-thres 0.65 
    ```


