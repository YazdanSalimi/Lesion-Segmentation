# Lesion-Segmentation
## Deep Learning Multi-Modality Automated abnormalities Segmentation Tools
This repsotiry is about lesion segmentation on multi modality images including CT, PET/CT, and SPECT/CT. 
All models have been trained using nnU-Net. You can find inference instructions in the provided inference-example.py file. It includes easy-to-use code for handling large images and several useful options for efficient inference on large datasets. You can also select the appropriate input image modality based on your needs. 
Currently, the code supports only the NIfTI file format, so you’ll need to convert your DICOM images to NIfTI before running the code. Instructions and scripts for converting DICOM to NIfTI will be available shortly. Alternatively, you can follow the standard nnU-Net inference instructions available on [nnU-Net](https://github.com/MIC-DKFZ/nnUNet) after downloading the trained models folder.
## Available Models

# PET Ga-PSMA lesion segmentation
The models require body-weight SUV unit and HU CT images as input. Separate models are available using PET only, CT only, and both PET and CT (PET/CT) images. Please ensure you select the appropriate model based on your input. We recommend using the PET only segmentation model when there is a respiratory misalignment between PET and CT images to ave a more accurate output. for the cases with perfect alignment we recommend using PET/CT models. The presence of respiratory misalignment can be automatedly checked using [this resposiroy](https://github.com/YazdanSalimi/PETCT-RMA-Detection). 
there are two versions of trained models, first using the old nnU-Net network architecture, and the second using the new nnU-Net architceture using residual blocks. the comparison can be found [here](https://github.com/MIC-DKFZ/nnUNet/blob/43349fa5f0680e8109a78dca7215c19e258c9dd7/documentation/resenc_presets.md?plain=1#L80)
## Download Trained Models
[All trained models](https://drive.google.com/drive/folders/1R6_EELnOeTb27YfueGm-X-bR-glgqOAF?usp=drive_link)


## Citation
If you use these models in your research or project, please cite the relevant papers:

[CT Modalities paper](https://www.medrxiv.org/content/10.1101/2023.10.20.23297331v1)

[PET Modalities paper](https://www.medrxiv.org/content/10.1101/2024.08.27.24312482v1)

## Installation:
Before running the tools, make sure your GPU drivers are properly installed and that nnunetv2 is installed as per their instructions, which can be found at: https://github.com/MIC-DKFZ/nnUNet.
Alternatively, you can install nnunetv2 using the following commands:
```bash
pip install --upgrade git+https://github.com/MIC-DKFZ/nnUNet.git

pip install --upgrade git+https://github.com/FabianIsensee/hiddenlayer.git
```
To install this repository, simply run:
```bash
pip install git+https://github.com/YazdanSalimi/Organ-Segmentation.git
```
We welcome any feedback, suggestions, or contributions to improve this project!

for any furtehr question please email me at: [salimiyazdan@gmail.com](mailto:salimiyazdan@gmail.com)

