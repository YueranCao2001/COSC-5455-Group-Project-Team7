# COSC-5455-Group-Project-Team7

# Fine-tuning Strategies based on DreamBooth

## Team Members: Yueran Cao, Zhengheng Li, Xizhong Xu, Zinian Wang

---

## Contents
1. [How to Run a Demo](#1-how-to-run-a-demo)
2. [References](#2-references)
3. [Member Assignments](#3-member-assignments)
4. [Link to Slides](#4-link-to-slides)

---

# 1. How to Run a Demo

## 1.1 Preparation
- **Google Colab**: Ensure you have access to [Google Colab](https://colab.research.google.com/).
- **Google Drive**

## 1.2 Steps to run
### Mount Google Drive
- Open the Colab notebook.
- Run the following code to mount your Google Drive:
  ```python
  from google.colab import drive
  drive.mount('/content/gdrive')

### Install Denpendencies
- Run the code cell named Requirment to install dependencies.

### Download the Model
- Select the model version from the dropdown (e.g., 1.5).
- If required, provide custom model paths or download links.
- Run the code cell to download the specified model version. The system will handle the process automatically.

### Create/Load a Session
- **Session Name**: Enter a session name. If it exists, it will load the session; otherwise, it will create a new one.
#### Important Note
- rename the instance pictures of each subject to a unique unknown identifier, example :
  - If your identifier is `phtmejhn`, rename the files as:
    ```
    phtmejhn (1).jpg, phtmejhn (2).png, etc.
    ```
  - Each subject/object should have a distinct identifier.

### Upload Instance Images
- Run the cell to upload the instance images.

#### Options
- **Remove_existing_instance_images**: Check this box to remove previously uploaded instance images.
- **Smart_Crop_images**: Check this box if you want the images to be automatically cropped to the desired size.

### Training
- **Training Parameters**:
   - **UNet_Training_Steps**: Adjust according to the size of the dataset. For smaller datasets (e.g., 10 images), start with `1500` or lower and adjust as needed.
   - **UNet_Learning_Rate**: Select the learning rate from the dropdown. Suggested default is `2e-6`. Avoid values too high to prevent overfitting.
   - **Text_Encoder_Training_Steps**: Default is `350`. Keep this value low (200–450) for small datasets.
   - **Text_Encoder_Learning_Rate**: Suggested default is `2e-6`.
   - **Offset_Noise**: Enable this option for style training.
- Run the cell to train model.

3. **Resolution**:
   - Default is `512`. Higher resolution provides better quality, but ensure instance images match the resolution.

4. **Save Checkpoints**:
   - **Save_Checkpoint_Every**: Set the interval for saving checkpoints (default is `500` steps).
   - **Start_saving_from_the_step**: Set the step from which to start saving checkpoints (default is `500`).

5. **Other Options**:
   - **Disconnect_after_training**: Check this box if you want to automatically disconnect from the session after training completes.

---

# 2. References

## 2.1 References related to coding part

**[1]. Dreambooth notebook we used for our project:** 

https://github.com/TheLastBen/fast-stable-diffusion

**[2]. A Youtube tutorial we used for the notebook:**

https://www.youtube.com/watch?v=nH18FMttD-c


---

## 2.2 References we use for literature review (More details can be found in the PPT)

**[1]. StyleGAN**

T. Karras, S. Laine, and T. Aila, "A Style-Based Generator Architecture for Generative Adversarial Networks," arXiv preprint arXiv:1812.04948, Dec. 2018. [Online]. Available: https://doi.org/10.48550/arXiv.1812.04948

**[2]. DDPM**

J. Ho, A. Jain, and P. Abbeel, "Denoising Diffusion Probabilistic Models," arXiv preprint arXiv:2006.11239, Jun. 2020. [Online]. Available: https://doi.org/10.48550/arXiv.2006.11239

**[3]. Stable Diffusion**

R. Rombach, A. Blattmann, D. Lorenz, P. Esser, and B. Ommer, "High-Resolution Image Synthesis with Latent Diffusion Models," arXiv preprint arXiv:2112.10752, Dec. 2021. [Online]. Available: https://doi.org/10.48550/arXiv.2112.10752

**[4]. CLIP**

A. Radford et al., "Learning Transferable Visual Models From Natural Language Supervision," arXiv preprint arXiv:2103.00020, Mar. 2021. [Online]. Available: https://doi.org/10.48550/arXiv.2103.00020

**[5]. Imagen**

C. Saharia et al., "Photorealistic Text-to-Image Diffusion Models with Deep Language Understanding," arXiv preprint arXiv:2205.11487, May 2022. [Online]. Available: https://doi.org/10.48550/arXiv.2205.11487

**[6]. Textual Inversion**

R. Gal, A. Alaluf, Y. Atzmon, O. Patashnik, A. Bermano, G. Chechik, and D. Cohen-Or, "An Image is Worth One Word: Personalizing Text-to-Image Generation using Textual Inversion," arXiv preprint arXiv:2208.01618, Aug. 2022. [Online]. Available: https://doi.org/10.48550/arXiv.2208.01618

**[7]. Pivotal Tuning**

R. Roich, A. Mokady, A. Bermano, D. Cohen-Or, and D. Lischinski, "Pivotal Tuning for Latent-based Editing of Real Images," arXiv preprint arXiv:2106.05744, Jun. 2021. [Online]. Available: https://doi.org/10.48550/arXiv.2106.05744

**[8]. DreamBooth**

N. Ruiz, Y. Li, V. Jampani, D. P. W. Ellis, and A. Veit, "DreamBooth: Fine Tuning Text-to-Image Diffusion Models for Subject-Driven Generation," arXiv preprint arXiv:2208.12242, Aug. 2022. [Online]. Available: https://doi.org/10.48550/arXiv.2208.12242

---

# 3. Member Assignments

In this project, each member was actively involved and made a similar contribution to the final result. The following table shows what each member is responsible for, but it does not mean that they are not doing other work that is not assigned to them.

|Member Name                 |Member Email           |Assignments                                    |Presentation  |
|:---------------------------|:---------------------:|:---------------------------------------------:|-------------:|
|Yueran Cao (Representative) |yc1306@georgetown.edu  |Coding, Organization Works, Literature Review  |Overview      |
|Zhengheng Li                |zl635@georgetown.edu   |Coding, Experiments, Coding-related Guidance   |Experiments   |
|Zinian Wang                 |zw475@georgetown.edu   |Coding, Evaluation, Handle with Datasets       |Evaluation    |
|Xizhong Xu                  |xx153@georgetown.edu   |Coding, Methodology, Model-related Explanation |Methodology   |

---

# 4. Link to Slides

You can see the slides in .pptx version via [Slides_PPTX](COSC-5455_Presentation.pptx)

Or you can see the slides in pdf version via [Slides_PDF](COSC-5455_Presentation.pdf)

Or just see via the Google Slide: https://docs.google.com/presentation/d/1Qt_NBI4VgZe3ITk6QHVXP-tyk0ldcWzrE8-5rDea5Jo/edit?usp=sharing

---
