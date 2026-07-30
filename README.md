# ShieldSight: PPE Compliance Detection System

## Project Overview

ShieldSight is a computer vision system designed to detect workers and personal protective equipment (PPE) in construction site images. The system uses a trained YOLO11 object detection model to identify five classes:

- Person
- Hardhat
- NO-Hardhat
- Safety Vest
- NO-Safety Vest

The goal of ShieldSight is to demonstrate how computer vision can assist with workplace safety monitoring by identifying workers and PPE within an image.

## Team Member

Brandi Green

## Project Tier

**Tier 2 – Object Detection**

ShieldSight uses object detection to locate workers and PPE within construction site images. The model produces bounding boxes, class labels, and confidence scores for detected objects.

## Problem Statement

Construction sites, warehouses, and manufacturing facilities require workers to wear personal protective equipment to reduce the risk of injuries. Monitoring every worker manually can be difficult, especially on large job sites.

ShieldSight explores how object detection can be used to assist with PPE monitoring by automatically detecting workers, hardhats, safety vests, and potential missing PPE.

## Solution

ShieldSight uses a custom-trained YOLO11 model to analyze construction site images and identify workers and PPE.

The system:

1. Receives a construction site image.
2. Processes the image using the trained YOLO11 model.
3. Detects PPE-related classes.
4. Displays bounding boxes, class labels, and confidence scores.
5. Allows the detections to be reviewed for potential PPE compliance issues.

## Technical Approach

**Computer Vision Technique:** Object Detection

**Model:** YOLO11

**Framework/Libraries:**
- Ultralytics
- PyTorch
- Python

**Development Environment:**
- Google Colab

YOLO11 was selected because it can detect multiple objects within a single image while providing the location, class, and confidence of each detection.

The original dataset contained additional classes that were not needed for the project. The dataset was filtered to five classes so the final model could focus specifically on workers and PPE compliance.

The final model was trained for 50 epochs using GPU acceleration in Google Colab.

## Dataset

**Dataset:** Construction Site Safety Image Dataset (Roboflow)

**Source:** Kaggle

**Original Size:** Approximately 2,800 labeled images

**Classes Used:**
- Person
- Hardhat
- NO-Hardhat
- Safety Vest
- NO-Safety Vest

Dataset source:

https://www.kaggle.com/datasets/snehilsanyal/construction-site-safety-image-dataset-roboflow

## Final Model Results

The final ShieldSight model achieved:

| Metric | Score |
|---|---:|
| Precision | 0.888 |
| Recall | 0.705 |
| mAP50 | 0.788 |
| mAP50-95 | 0.473 |

The model performed well overall, particularly when detecting hardhats and safety vests.

NO-Hardhat was one of the more challenging classes, with a recall of 0.551. This limitation was also observed during demo testing when the model occasionally detected a worker but did not identify the worker as NO-Hardhat.

Additional results and example detections are available in the `results/` folder.

## Demo Testing

The final model was tested on construction images outside of the training process.

Testing showed that ShieldSight could successfully detect multiple workers and PPE items within the same image. The model produced bounding boxes, class labels, and confidence scores for its predictions.

Testing also revealed failure cases. For example, the model could detect a person correctly while failing to identify missing PPE. These examples demonstrate why model evaluation should include both successful detections and failure cases.

Examples of successful and unsuccessful predictions are included in the `results/` folder.

## Repository Structure

ShieldSight-PPE-Detection/

- `data/` – Dataset information
- `docs/` – Project proposal and AI Usage Log
- `notebooks/` – Final project notebook
- `results/` – Final metrics and detection examples
- `README.md` – Project documentation
- `requirements.txt` – Project dependencies

## How to Run

1. Open the project notebook in Google Colab.
2. Install the required dependencies.
3. Import Ultralytics YOLO.
4. Load the trained `best.pt` model.
5. Provide a test construction image.
6. Run inference.
7. Review the bounding boxes, detected classes, and confidence scores.

The `requirements.txt` file contains the project dependencies needed to reproduce the environment.

## Limitations

ShieldSight does not detect every PPE condition correctly. Performance can be affected by:

- Small or distant workers
- Crowded scenes
- Partially blocked workers or PPE
- Different viewing angles
- Similar visual features between PPE classes
- Limited examples of some classes in the training data

The NO-Hardhat class was a particular challenge for the final model.

## Future Improvements

Future improvements could include:

- Adding more training examples for weaker classes such as NO-Hardhat
- Improving class balance within the dataset
- Testing additional YOLO11 model sizes
- Further hyperparameter tuning
- Testing on a wider variety of real-world construction images
- Expanding ShieldSight from image-based detection toward video or real-time PPE monitoring

## AI Usage

ChatGPT was used throughout the project as a learning and development resource. AI assistance included helping with project planning, dataset preparation, troubleshooting, interpreting model metrics, organizing the demo, and reviewing project documentation.

A detailed record of the major AI interactions, what was learned, and how the guidance was applied is available in:

`docs/AI_usage_log.md`

## Project Status

- ✅ Dataset prepared and filtered
- ✅ YOLO11 model trained
- ✅ Final 50-epoch training completed
- ✅ Model evaluated
- ✅ Final metrics documented
- ✅ Successful detections tested
- ✅ Failure cases analyzed
- ✅ Demo created
- ✅ AI Usage Log completed
- ✅ GitHub repository organized
