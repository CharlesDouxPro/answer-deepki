# answer-deepki


## Description
This repository is a technical assessment for the Deepki Data Engineer role. For this test, I am not just trying to solve the problem but also aiming to show my coding style. It is also an opportunity for me to receive constructive feedback on what could be improved if a future collaboration is possible.

The pipeline take in entry 3 inputs:
  - ref_lat : The latitude of the reference building
  - ref_lon : The longitude of the reference building
  - url : The google open buildings region file url
  

When you run the application, it will generate two outputs:

  - The Plus Code of the closest building, shown in the terminal.
  - A plot saved as output.png.

## Requirements
Docker should be running on your environment.

## Installation
Clone the repo Git :
```bash
git clone https://github.com/CharlesDouxPro/answer-deepki.git
cd answer-deepki
```

## Run
```bash
docker build -t deepki-container .
```

```bash
docker run -v $(pwd):/workspace deepki-container 
```

it will generate the outputs.

The inputs are already set in the Docker CMD line but can be easily overridden by using : 

```bash
docker run -v $(pwd):/workspace deepki-container python main.py --ref_lat <latitude> --ref_lon <longitude> --url <csv_file_url>
```


