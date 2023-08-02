# Twitter Trending Topics Analysis with ARIMA and LSTM

This repository contains Python scripts for analyzing and predicting the position of specific topics in Twitter's trending topics using ARIMA and LSTM models.

## Project Description

The data used in this project are daily CSV files, each line starting with a Unix timestamp and each element of the line being the Trending topic, in descending position order. The data can be found in the following URL structure: `https://artint.tech/tw/f/trends/mx_log/YYYYMMDD`. The data spans from 2020-03-10 to 2023-04-27.

The analysis performed by the scripts in this repository helps in predicting the rank of a specific topic in the future, taking into account the time of day and whether it's a weekday or a weekend.

## Setup and Installation

The scripts are intended to be run on Google Colab. No specific setup is needed beyond having a Google account to access the Colab environment.

## Usage

First, run the `download_data.py` script. This script uses `wget` to download CSV files from the specified URL and save them in the Colab environment.

Next, use the `process_data.py` script to read the downloaded data, perform some preprocessing and feed the data into an ARIMA model or LSTM model.

The ARIMA model uses the statsmodels library's `ARIMA` function, with parameters `(5,1,0)`. This might need to be adjusted for better results.

## Limitations

ARIMA and LSTM models assume that the data is stationary, which might not be the case with this particular dataset. This is future work for the project.

## Contributions

Contributions, issues and feature requests are welcome.

## License

This project is open source, feel free to use the scripts and modify them according to your needs. 

Enjoy your data analysis!
