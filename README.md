# NeuroAI-Task - Hymenoptera Dataset

This project is designed to train a model on the Hymenoptera dataset using a ViT (Vision Transformer) model using transfer learning.

![image](https://github.com/user-attachments/assets/a239ee50-3f04-4918-add0-4a73825ee43e)

### Results

The model is trained on the Hymenoptera dataset with the performance and logs visualized using TensorBoard. The hyperparameters are as follows:

![Results](https://github.com/user-attachments/assets/4beede49-3d40-4bf9-bb47-3952ace78f6f)

| **Hyperparameter**                | Value                  | Description                                                |
|--------------------------------|----------------|------------------------------------------------|
| **Run Name**                       | `hymenoptera`          | Name of the training run for logging and monitoring. |
| **Dataset**                           | `hymenoptera_data` | The dataset being used for training. |
| **Model Type**                     | `ViT-B_16`                | Vision Transformer Base model with a patch size of 16x16. |
| **Pretrained Directory**     | `checkpoint/ViT-B_16.npz` | Path to the pretrained ViT model. |
| **Image Size (`img_size`)** | `224` (default)         | Input image resolution. |
| **Training Batch Size**        | `64`                              | Batch size during training. |
| **Evaluation Batch Size**   | `16`                              | Batch size during evaluation. |
| **Number of Steps**            | `1000`                          | Total number of training steps. |
| **Evaluation Frequency (`eval_every`)** | `100` (default)             | Frequency of evaluation in steps. |
| **Learning Rate**                  | `3e-2` (default)             | Initial learning rate for SGD. |
| **Weight Decay**                 | `0` (default)                  | Weight decay for regularization. |
| **Decay Type**                      | `cosine` (default)          | Learning rate decay strategy (`cosine` or `linear`). |
| **Warmup Steps**                  | `500` (default)                | Number of warmup steps for the learning rate scheduler. |
| **Max Gradient Norm**        | `1.0` (default)                | Maximum gradient norm for clipping. |
| **Local Rank**                       | `-1` (default)                  | Rank for distributed training on GPUs. |
| **Seed**                                  | `42` (default)                  | Random seed for reproducibility. |
| **Gradient Accumulation Steps** | `1` (default)                    | Number of steps to accumulate gradients before updating. |
| **Mixed Precision (`fp16`)** | Enabled                        | Use of 16-bit floating point precision for faster training and reduced memory usage. |

| Step | Test Accuracy | Train Loss | Train Learning Rate |
|------|----------------|----------------|---------------------|
| 100  | 0.9804        | 0.00006          | 0.6934               |
| 200  | 0.9869        | 0.00012          | 0.6934               |
| 300  | 0.9804        | 0.00018          | 0.6929               |
| 400  | 0.9804        | 0.00024          | 0.6927               |
| 500  | 0.9804        | 0.00030          | 0.6920               |
| 600  | 0.9739        | 0.00036          | 0.6911               |
| 700  | 0.9739        | 0.00042          | 0.6896               |
| 800  | 0.9739        | 0.00048          | 0.6881               |
| 900  | 0.9739        | 0.00054          | 0.6851               |
| 1000| 0.9739        | 0.00060          | 0.6824               |

## Setup

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Visit the ```run.ipynb``` for the complete task.

## TensorBoard Monitoring

Load TensorBoard to monitor training progress:

```python
%load_ext tensorboard
```
