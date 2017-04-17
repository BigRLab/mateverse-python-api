# mateverse-python-api
Python Client for Mateverse APIs https://www.mateverse.com/

## Introduction

The Mateverse-Python API call will return you the confidence score of your images that are trained on a particular model of your choice. When you make a prediction through the API, you pass in the image and tell it what model to use, authenticating the API call with your api_secret key and model_id


## Usage

In request.py you need to pass in the following parameters to make the API work:

#### api_secret key
The api_secret key serves as the authentication key to the API call. Just copy-paste your api_secret key in request.py and you are good to go.

#### model_id
The model_id is to tell the API which model to use for your prediction.

#### Path to your images
You need to give the path to the images which will go inside a list. You can pass in the path to as much images as you want.

## Run
    python request.py

## Response
Response will be a JSON object, easily parseable in all programming languages.

    [
      {
        "status": "success",
        "message": "Predictions.",
        "predictions": [
          {
            "sample": "earring_470.jpg",
            "predictions": [
              {
                "predicted_score": "0.999816",
                "predicted_label": "earring"
              },
              {
                "predicted_score": "0.000184305",
                "predicted_label": "bracelt"
              }
            ]
          }
        ]
      }
    ]


## Licensing

MIT License
