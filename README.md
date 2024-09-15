# Activity Tracking Agent

This application is an activity tracking agent designed to monitor mouse movements, keyboard inputs, and capture screenshots at defined intervals. The collected data is either uploaded to an AWS S3 bucket in real-time or queued for offline upload when the internet connection is restored.

## Features

- **Activity Monitoring**: Tracks mouse movements and keyboard presses.
- **Irregular Activity Detection**: Discards intervals with irregular mouse or keyboard activity (e.g., unnatural movements or overly fast key presses).
- **Screenshot Capture**: Takes periodic screenshots, which can be blurred for privacy.
- **AWS S3 Integration**: Uploads logs and screenshots to an AWS S3 bucket, with retry logic for offline periods.
- **Tkinter GUI**: Provides a simple interface to start/stop activity tracking, adjust intervals, and toggle features.

## Requirements

- Python 3.x
- The following Python packages are required:
  - `os`
  - `time`
  - `pyautogui`
  - `Pillow` (for image processing)
  - `tkinter`
  - `threading`
  - `pynput`
  - `numpy`
  - `boto3` (for AWS S3 integration)
  - `msvcrt` (for ensuring single instance on Windows)
  - `queue`
  - `socket`

You can install dependencies using:

```bash
pip instal -r requirements.txt


Setup for AWS S3:
AWS Setup: Configure AWS credentials for S3:

bash
aws configure

Create file named credentials
aws_access_key_id = 'your-access-key'
aws_secret_access_key = 'your-secret-key'

Replace the following variables in the code with your AWS details in the code:
aws_bucket_name = 'your-bucket-name'
aws_region = 'your-aws-region'



To run the application:
python script.py
