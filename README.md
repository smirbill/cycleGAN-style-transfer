#  CycleGAN: Image Style Transfer (Horse ↔ Zebra)

This project implements a CycleGAN architecture for unpaired image-to-image translation using TensorFlow and Keras. The model learns to convert images of horses into zebras and vice versa without needing paired datasets.

##  Key Features
- Full implementation of generators and discriminators (ResNet & PatchGAN)
- Training on the horse2zebra dataset from TensorFlow Datasets
- Cycle consistency and identity loss
- Custom training loop and monitoring via matplotlib
- Result visualization and image saving

##  Project Structure
- `cyclegan.py`: full code with data loading, model building, training and testing
- `samples/`: example input/output images (add yours here!)
- `README.md`: this file

##  How to Run
1. Clone the repository
2. Set up your Conda environment:
    ```bash
    conda create --name cyclegan-env python=3.9
    conda activate cyclegan-env
    conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1.0
    pip install "numpy<2" "tensorflow<2.11"
    ```
3. Run the training script:
    ```bash
    python cyclegan.py
    ```

## Sample Results
| Input (Horse) | Output (Zebra) |
|---------------|----------------|
| ![](samples/horse1.jpg) | ![](samples/zebra1.jpg) |
| ... | ... |

##  Notes
- Model trained for 70 epochs with Adam optimizer
- Used a callback function to generate and save results per epoch
- Preprocessing includes resizing, cropping, normalization to [-1, 1]

##  Authors
- Vasileios Smyridis 
  
*MSc AI & Data Analysis – University of Macedonia*

##  License
MIT

