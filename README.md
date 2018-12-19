# chain_colorization

### Requirements
- For AWS (recommended), use the "Amazon Deep Learning AMI (Ubuntu)" EC2 Instance
- Linux or OSX
- CPU or NVIDIA GPU + CUDA CuDNN.
- Python 2.7, and Caffe for Python 2.7 were tested in this implementation
- Other libraries: scikit-image, scikit-learn, python-opencv, python-qt4, qdarkstyle

### Setup
- Clone this repo:
```
git clone https://github.com/kaabashqeen/chain_colorization.git
cd chain_colorization
```
- Download the pretrained caffe model
```
bash ./models/fetch_models.sh
```
- Clone the chain_colorization_images repo to run the model on
```
git clone https://github.com/kaabashqeen/chain_colorization_images.git
```
- Rename the "chain_colorization_images" folder to "images"

- Use python 2.7, and caffe_p27
```
source activate python2
source activate caffe_p27
```

- Run jupyter notebook
```
jupyter notebook
```

- Open "chain_colorization.pynb"
- Run the first line to setup the image files and the pretrained caffe model
