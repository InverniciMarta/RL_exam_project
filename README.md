# Adaptive Optics Control with Reinforcement Learning

This project explores the use of **Soft Actor-Critic (SAC)** to improve the control of an **adaptive optics (AO)** system.

The simulation is built with HCIPy. A reinforcement learning controller adds corrections to a classical integrator, and the two approaches are compared using the **long-exposure Strehl ratio**.

## Project structure

```text
project/
├── checkpoints/                    # Training checkpoints
├── training_logs/                  # Training logs and statistics
├── .gitignore                     
├── ProjectSlides.pdf               # Project presentation
├── README.md                      
├── project.ipynb                   # Project notebook
├── requirements.txt               
├── sac_policy.pth                  # Final trained policy
├── sac_policy.pth.scales.json      # Final policy normalization scales
├── sac_policy_best.pth             # Best evaluated policy
└── sac_policy_best.pth.scales.json # Best policy normalization scales
```

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

## References

1. E. H. Por et al., *High Contrast Imaging for Python (HCIPy): an open-source adaptive optics and coronagraph simulator*. Adaptive Optics Systems VI, 2018. [DOI: 10.1117/12.2314407](https://doi.org/10.1117/12.2314407).

2. T. Haarnoja et al., *Soft Actor-Critic Algorithms and Applications*. arXiv:1812.05905v2, 2019. [arXiv](https://arxiv.org/abs/1812.05905).

3. B. Pou et al., *Model-free Reinforcement Learning with a Non-linear Reconstructor for closed-loop Adaptive Optics control with a pyramid wavefront sensor*. Proceedings of SPIE 12185, 2022.

4. B. Pou et al., *Integrating supervised and reinforcement learning for predictive control with an unmodulated pyramid wavefront sensor for adaptive optics*. Optics Express 32, 37011–37035, 2024.

5. B. Pou, J. Smith, E. Quinones, et al., *Implementation of integrating supervised and reinforcement learning for predictive control with an unmodulated pyramid wavefront sensor for adaptive optics*. GitHub, 2024. [Repository](https://github.com/Tomeu7/Integrating-SL-and-RL-for-AO).

6. R. Sutton and A. Barto, *Reinforcement Learning: An Introduction*. MIT Press, 2018.

## Use of ChatGPT

**ChatGPT was used as a development support tool** for:

- File logging functionality.
- Video recording functionality.
- Code acceleration and performance optimization.
- Writing and improving comments and documentation for classes and functions.
- Ongoing support for code refinement and cleanup.

ChatGPT assisted with these tasks during development of the project.
