# PyTorch for Deep Learning

My notes and code as I work through Daniel Bourke's **[Learn PyTorch for Deep Learning in a Day. Literally.](https://www.youtube.com/watch?v=Z_ikDlimN6A)**, a ~25-hour beginner course covering PyTorch fundamentals through computer vision and custom datasets. Course materials: [learnpytorch.io](https://www.learnpytorch.io/) · [mrdbourke/pytorch-deep-learning](https://github.com/mrdbourke/pytorch-deep-learning)

I'm an undergraduate researcher in computational biology, and I'm using this course to build a solid foundation in PyTorch for applying deep learning to biological problems. Each notebook follows along with the video and includes my own **Practice** cells where I experiment beyond the course code.

All notebooks run in Google Colab (see the "Open in Colab" badge at the top of each).

## Progress

| # | Notebook | Status |
|---|----------|--------|
| 00 | [PyTorch Fundamentals](00_pytorch_fundamentals.ipynb) | ✅ Complete |
| 01 | [PyTorch Workflow](01_pytorch_workflow.ipynb) | ✅ Complete |
| 02 | [Neural Network Classification](02_PyTorch_Neural_Network_Classification.ipynb) | 🚧 In progress |
| 03 | Computer Vision | ⏳ Up next |
| 04 | Custom Datasets | ⏳ Up next |

## What I'm Learning

### 00 — PyTorch Fundamentals
- Creating tensors: scalars, vectors, matrices, and higher-dimensional tensors
- Inspecting tensors with `.ndim`, `.shape`, `.dtype`, `.device`, and `.item()`
- Random tensors (e.g. an image-shaped `(3, 224, 224)` tensor), zeros, ones, `arange`, and `*_like` functions
- Tensor datatypes and converting between them (float32, float16, etc.)
- The three most common PyTorch errors: wrong **datatype**, wrong **shape**, wrong **device**
- Tensor operations: addition, subtraction, multiplication, division
- Element-wise vs. matrix multiplication, and why `torch.matmul` is far faster than a Python loop

### 01 — PyTorch Workflow
The end-to-end workflow, built around a simple linear regression problem (`y = 0.7x + 0.3`):
- **Data:** generating data and making an 80/20 train/test split, then plotting it
- **Build a model:** subclassing `nn.Module`, using `nn.Parameter` and `nn.Linear`, and inspecting `state_dict()`
- **Predict:** making predictions with `torch.inference_mode()`
- **Train:** using a loss function (`nn.L1Loss`) and optimizer (`torch.optim.SGD`), and writing training and testing loops
- **Evaluate:** plotting loss curves to watch the model converge
- **Save and load:** `torch.save()`, `torch.load()`, and `load_state_dict()`
- **Device-agnostic code:** running on GPU when available (`cuda` vs. `cpu`)

### 02 — Neural Network Classification *(in progress)*
- Generating a toy dataset with scikit-learn's `make_circles`
- Exploring data with pandas and matplotlib
- Checking input/output shapes
- Converting NumPy arrays to tensors and splitting with `train_test_split`
- *Coming up:* building a classification model, non-linear activations, and evaluation metrics

## Tools
Python · PyTorch · NumPy · pandas · matplotlib · scikit-learn · Google Colab

## Credit
All course content and teaching credit goes to [Daniel Bourke](https://github.com/mrdbourke). This repo is my personal learning record.
