
# Depth Estimation Project

Depth Estimation is a project designed for depth estimation using the powerful ZoeDepth model. This repository offers multiple interfaces for seamless integration and deployment, making it accessible through both command-line (CLI) and API methods.

Features
Depth Estimation: Utilizes the ZoeDepth model to estimate depth maps from input images.

CLI Interface: The command-line interface allows users to perform depth estimation by providing input and output image paths as arguments.

API Interface: Provides a simple API endpoint (http://127.0.0.1:8041/predict) for integrating depth estimation functionality into other applications or services.

Docker Support: Offers Docker support for easy deployment and scaling of the depth estimation service. Users can build a Docker image and run it as a container to encapsulate the environment.



<img src="https://github.com/erentorlak/Depth_Estimation/blob/main/example/input_image.jpg" width="400" height="200">
<img src="https://github.com/erentorlak/Depth_Estimation/blob/main/example/output_image.png" width="400" height="200">




## Usage/Examples

### CLI Usage
```bash
usage: cli.py [-h] input_image output_image

Depth estimation using ZoeDepth.

positional arguments:
  input_image   Path to input image.
  output_image  Path to output depth map.

options:
  -h, --help    show this help message and exit
```
### API Usage

```
http://127.0.0.1:8041/predict
```

## Installation

Install depth estimation project with pip

```bash
pip install -r requirements.txt
```
    
## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`IMG_API_KEY`

## Deployment

To deploy this project run

```bash
docker build -t depth_estimation .
docker run -d -p 8041:8041 depth_estimation
```


