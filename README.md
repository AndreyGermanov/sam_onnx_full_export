# Segment Anything full ONNX export

This repository shows how to solve the following ONNX export issue in Segment Anything model. 

Official documentation shows how to export only the mask decoder model, but not the image encoder. So, even with exported ONNX model, developer still need to use original PyTorch model and official API. It makes most benefits of ONNX useless and greatly limits the possible use of this model in production. Due to this, the Segment Anything can be deployed only with Python and only if PyTorch and official API installed.

This repo aimed to fill this gap, here you can find how to export both SAM Image encoder and Mask decoder and how to use it for inference using only ONNX.

* `sam_onnx_export.ipynb` - Shows how to export both image encoder and masks decoder models to ONNX.
* `sam_onnx_inference.ipynb` - Shows how to use exported models for image segmentation.
