# Image Captioning and Hashtag Generation

A deep learning project exploring image captioning, hashtag generation, multilingual caption output, and image inpainting using CNNs, Transformer-based sequence modeling, NLP, and Partial Convolution.

## Overview

The project contains an image-captioning pipeline that uses a CNN-based visual feature extractor and a Transformer encoder-decoder for autoregressive caption generation. It also includes a separate hashtag-generation component and an image-restoration component based on a U-Net-style architecture and Partial Convolution.

## Objectives

- Extract visual representations from images using CNNs.
- Generate natural-language image captions using Transformer-based sequence modeling.
- Explore knowledge distillation in image-captioning model development.
- Generate relevant hashtags from processed textual information.
- Support multilingual caption translation.
- Explore image restoration using U-Net-style and Partial Convolution methods.

## Methodology

### Image Captioning

The captioning inference pipeline follows:

```text
Input Image
     |
     v
VGG16 CNN Feature Extractor
     |
     v
Visual Feature Representation
     |
     v
Transformer Encoder
     |
     v
Transformer Decoder
     |
     v
Generated Caption
```

### Hashtag Generation

A separate sequence model is used to generate hashtag tokens from processed textual/image-derived information.

### Multilingual Output

The project includes mBART-50 based translation for multilingual output.

### Image Inpainting

The image-restoration component explores U-Net-style architecture and Partial Convolution for reconstructing masked image regions.

## Dataset

The captioning notebooks use the Flickr8k image-captioning dataset. The dataset is not included in this repository.

Obtain the dataset from its appropriate source and place the required files in the paths expected by the notebooks. Do not commit large datasets or credentials.

## Repository Structure

```text
image-captioning-and-hashtag-generation/
|
├── notebooks/
|   ├── 01_captioning_training_and_evaluation.ipynb
|   ├── 02_cnn_transformer_inference.ipynb
|   ├── 03_hashtag_generation.ipynb
|   └── 04_image_inpainting.ipynb
|
├── results/
|   └── README.md
|
├── test_images/
|   └── README.md
|
├── docs/
|   └── methodology.md
|
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

## Notebooks

- **01_captioning_training_and_evaluation.ipynb** — Captioning training/evaluation workflow, including knowledge-distillation/Show-and-Tell and Transformer-based components.
- **02_cnn_transformer_inference.ipynb** — VGG16 CNN feature extraction followed by Transformer-based caption inference.
- **03_hashtag_generation.ipynb** — Hashtag-generation model training and inference.
- **04_image_inpainting.ipynb** — U-Net-style and Partial Convolution based image restoration.

## Model Artifacts

Large trained model artifacts are intentionally excluded from the repository. Place required artifacts in the paths specified by the corresponding notebook configuration cells.

## How to Run

```bash
git clone https://github.com/EshaSingh02/image-captioning-and-hashtag-generation.git
cd image-captioning-and-hashtag-generation

python -m venv .venv
source .venv/bin/activate

pip install -r requirements.txt
pip install notebook
jupyter notebook
```

Open the required notebook from `notebooks/` and configure the dataset, test-image, and model-artifact paths as described in its configuration cells.

## Results

Selected qualitative outputs can be placed in `results/`. Quantitative metrics should only be reported when directly supported by the corresponding experiment.

## Limitations

- Training deep learning models can require substantial computational resources.
- Datasets and large trained model artifacts are not included.
- Caption and hashtag quality depends on the training data and model configuration.
- Image-inpainting quality depends on the masked region and image content.

## Future Work

Potential improvements include stronger vision encoders, improved decoding strategies, better hashtag relevance, additional multilingual support, and more advanced image-inpainting architectures.

## Author

**Esha Singh**  
M.Tech, Sustainable Energy Engineering  
Indian Institute of Technology Kanpur
