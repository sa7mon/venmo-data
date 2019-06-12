# Venmo Transaction Dataset

## What is this? 

This is a dataset of transaction data scraped from the [Venmo](https://venmo.com) public API. Venmo is an app which allows users to easily send and receive money. 

This data was collected as part of a data analysis project and was scraped during the following date ranges:

* July 2018 - September 2018
* October 2018
* Jan 2019 - Feb 2019


## Dataset Info

The dataset is in BSON form as it was exported from a MongoDB database. It has been compressed with `xz` to allow for faster transfers. 

* **Compressed size:** 1.03 GB
* **Uncompressed size:** 10.87 GB
* **Transaction Count:** 7,076,585

A sample transaction .json file is included as `sample.json`

## Download Dataset

* **Torrent (Preferred):** Use the included `.torrent` file
* **HTTPS:** [Here](https://d.badtech.xyz/venmo.tar.xz)

## Use This Dataset
This dataset was exported from a MongoDB instance with the following settings:
* Database name: `test`
* Collection name: `venmo`

1. Install MongoDB
    * `sudo apt install mongodb`
2. Extract .xz
    * `tar xf venmo.tar.xz` 
    * or with progress: `pv venmo.tar.xz | tar xf - -C extracted/ --xz`
3. Restore dump
    * `mongorestore --collection venmo --db test venmo.bson`





