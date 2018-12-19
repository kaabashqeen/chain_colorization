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

### Run

- Use python 2.7, and caffe_p27
```
source activate python2
source activate caffe_p27
```
- Run jupyter notebook
```
jupyter notebook
```
- "chain_colorization.pynb" implements our algorithm for chain model colorization on images. In the images file, there are three images for a picture: a "-inputs.png" picture, which is the input (greyscaled) picture,  a "-outputs.png" picture, which is the output from our trained cDCGAN model (Pix2Pix), and a "-targets.png" picture, which is what the test image actually looks like with color. You can change the number of hints you use to produce the image, change the thresholds to find the "best" pixels that are used as hints, and change the "nearest pixel" threshold to find closer pixels to previously chosen pixels.
- "output_results.ipynb" produces the output strips of outputs to compare and contrast the effectiveness of our tests.

### References
Code setup for the production and use of the hint model
```
@article{zhang2017real,
  title={Real-Time User-Guided Image Colorization with Learned Deep Priors},
  author={Zhang, Richard and Zhu, Jun-Yan and Isola, Phillip and Geng, Xinyang and Lin, Angela S and Yu, Tianhe and Efros, Alexei A},
  journal={ACM Transactions on Graphics (TOG)},
  volume={9},
  number={4},
  year={2017},
  publisher={ACM}
}
