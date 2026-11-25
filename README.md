# Adaptive Optics Control with Reinforcement Learning

This project explores the use of **Soft Actor-Critic (SAC)** to improve the control of an **adaptive optics (AO)** system.

The simulation is built with HCIPy. A reinforcement learning controller adds corrections to a classical integrator, and the two approaches are compared using the **long-exposure Strehl ratio**.

## Requirements

- Python and Jupyter Notebook (or Google Colab)
- `numpy`, `scipy`, `pandas`, `matplotlib`
- `torch`, `hcipy`, `xxhash`, `tqdm`, `imageio-ffmpeg`

Install the required packages in your Python environment before running the notebook.

## How to run

1. Open the project notebook (`.ipynb` file) in Jupyter or Google Colab.
2. Adjust the simulation and training parameters in the `create_args()` cell if needed.
3. Run the cells in order.

By default, the notebook trains the SAC agent and compares it with the classical controller. The main settings include the number of training episodes, the number of test repetitions, logging, video recording, and checkpointing.

## Outputs

The notebook can save:

- Trained SAC policies and checkpoints.
- CSV logs with training and evaluation statistics.
- Test results and a comparison plot of the long-exposure Strehl ratio.
- MP4 recordings of the AO system with and without reinforcement learning.

Results are saved to `RL_AO_results/` when running locally, or to `MyDrive/RL_AO/` when using Google Colab with Google Drive.

## Use of ChatGPT

**ChatGPT was used as a development support tool** for:

- File logging functionality.
- Video recording functionality.
- Code acceleration and performance optimization.
- Writing and improving comments and documentation for classes and functions.
- Ongoing support for code refinement and cleanup.

ChatGPT assisted with these tasks during development of the project.
