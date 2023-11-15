# Segment Anything full ONNX export

This is a source code for the [Export Segment Anything neural network to ONNX: the missing parts](https://dev.to/andreygermanov/export-segment-anything-neural-network-to-onnx-the-missing-parts-43c8) article.

Both the article and this repository aimed to show how to solve the ONNX export issue in the Segment Anything model. Official documentation explains how to export only the mask decoder model, but not the image encoder. So, even with exported ONNX model, developer still need to use original PyTorch model and official API. It makes most benefits of ONNX useless and greatly limits the possible use of this model in production. Due to this, the Segment Anything can be deployed only with Python and only if PyTorch and official API installed.

This repo fills this gap, here you can find how to export both SAM image encoder and mask decoder and how to use it for inference using only ONNX.

* `sam_onnx_export.ipynb` - Shows how to export both image encoder and masks decoder models to ONNX.
* `sam_onnx_inference.ipynb` - Shows how to use exported models for image segmentation.

Read the article for thorough explanation of this code.