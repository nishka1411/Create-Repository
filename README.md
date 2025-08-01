# AI Dog Breeds Model

This project uses NVIDIA Jetson's `jetson-inference` library to classify images using pre-trained deep learning models. The script, `main.py`, takes an image file as input and returns the predicted class label along with confidence.

## 📄 File Used: `main.py`

### ✅ Description

This script loads an image, processes it using a specified image classification model (default: `resnet-18`), and outputs the top classification result.

### 🖼️ Usage

```bash
python3 main.py <image_file> --network <model_name>
```

#### Arguments:

* `<image_file>`: Path to the image you want to classify (required)
* `--network`: *(Optional)* The classification model to use. Default is `resnet-18`.

#### Example:

```bash
python3 main.py images/dog.jpg --network resnet-18
```

### 📁 Model & Labels

Ensure the following files exist:

* `resnet18.onnx` (or your chosen model)
* `dataset/labels.txt`

These can be specified or replaced depending on your model.

### 🧠 Supported Models

You can use any compatible model available in `jetson-inference`, such as:

* `googlenet`
* `resnet-18`
* `resnet-50`
* etc.

### 📤 Output

The script will print the classification result like:

```
image is recognized as Labrador (class #207) with 85.23% confidence
```
