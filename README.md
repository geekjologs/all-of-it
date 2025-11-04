# All Of It: From Pixels to Prose

This repository contains a series of notebooks that will take you from the fundamental building blocks of deep learning to building and understanding modern models like GPT.

## Notebooks

This series of notebooks is designed to be completed in order:

1.  `notebook_1_building_blocks.ipynb`: The fundamental building blocks of deep learning.
2.  `notebook_2_your_first_model.ipynb`: Build your first neural network.
3.  `notebook_3_learning_patterns_cnn.ipynb`: Learn about convolutional neural networks for image recognition.
4.  `notebook_4_going_deeper_resnet.ipynb`: Dive into deeper architectures with ResNets.
5.  `notebook_5_from_pixels_to_prose.ipynb`: Explore models that can generate text from images.
6.  `notebook_6_the_main_event_gpt.ipynb`: Build and understand the GPT model.
7.  `notebook_7_demystifying_inference.ipynb`: Learn about the process of using a trained model.
8.  `notebook_8_huggingface_finetuning.ipynb`: Fine-tune models using the Hugging Face ecosystem.

## Getting Started

These instructions will guide you in setting up your environment to run the notebooks on macOS or a Linux machine with an NVIDIA GPU.

### Prerequisites

- Python 3.8+
- `uv` package manager. You can install it by following the [official instructions](https://github.com/astral-sh/uv).

### Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/infatoshi/all-of-it.git
    cd all-of-it
    ```

2.  **Create a virtual environment:**
    ```bash
    uv venv
    ```
    This will create a `.venv` directory in your project folder.

3.  **Activate the virtual environment:**
    ```bash
    source .venv/bin/activate
    ```

4.  **Install the dependencies:**
    ```bash
    uv pip install -r requirements.txt
    ```

5.  **Start Jupyter Lab:**
    ```bash
    uvx jupyter lab
    ```
    This will open Jupyter Lab in your browser, where you can navigate to and run the notebooks.

### Platform-specific Instructions

#### macOS (Apple Silicon)

The default setup using `uv` should work correctly on Apple Silicon Macs. PyTorch will use the Metal Performance Shaders (MPS) backend for acceleration.

#### Linux with NVIDIA GPU

To leverage your NVIDIA GPU, you need to have the NVIDIA drivers and CUDA Toolkit installed. The dependencies in `requirements.txt` are configured for CUDA.

The `unsloth` library provides significant speedups. Please refer to the [Unsloth documentation](https://github.com/unslothai/unsloth) for detailed installation instructions tailored to your specific CUDA version to ensure maximum performance. You might need to install a specific version of `unsloth` with a command like:
```bash
uv pip install "unsloth[cu121-py310]" --extra-index-url https://ai.unsloth.ai/pypi/simple
```
The command above is an example. Please check the Unsloth repository for the command that matches your environment.
