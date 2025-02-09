什么是 ONNX 
-----------

by @karminski-牙医

![onnx-ecosystem](assets/images/onnx.png)

(图片来自 ultralytics.com)

ONNX（Open Neural Network Exchange）是一种开放的神经网络交换格式。

它由微软和Facebook于2017年共同推出，现由Linux基金会的LF AI托管，旨在解决不同深度学习框架之间的互操作性问题，实现模型在不同平台和工具链之间的无缝迁移。

## ONNX 的主要特点和优势

- **跨框架兼容性：** 支持主流深度学习框架（PyTorch/TensorFlow/MXNet等）的模型转换，打破框架生态壁垒。开发者可以用PyTorch训练模型，导出为ONNX格式后通过[ONNX-TensorFlow](https://github.com/onnx/onnx-tensorflow)等适配器在TensorFlow中部署。
- **高效推理性能：** 通过运行时优化（如ONNX Runtime）实现低延迟推理，支持CPU/GPU/FPGA等多种硬件加速，在服务端和移动端均可获得优异性能。
- **可扩展性设计：** 采用protobuf格式存储计算图和权重参数，通过Operator Sets机制支持自定义算子扩展，持续跟进AI技术演进。
- **标准化模型格式：** 定义统一的模型表示规范，包含网络结构、层参数、输入输出格式等完整信息，支持可视化工具（如Netron）直接解析。

## ONNX 的应用场景

- **跨框架模型转换：** 将PyTorch训练的视觉模型转换为ONNX格式后，可进一步转换为TensorFlow Lite格式部署到移动端
- **生产环境部署：** 通过ONNX Runtime实现高性能推理，支持动态batching和硬件加速
- **边缘计算优化：** 与TensorRT/OpenVINO等推理引擎配合，实现模型在IoT设备的量化部署
- **算法研究验证：** 快速在不同框架间迁移实现，方便论文复现和效果对比

## ONNX 生态系统支持

- **训练框架：** PyTorch, TensorFlow（通过tf2onnx工具）, MXNet, PaddlePaddle
- **推理引擎：** ONNX Runtime, TensorRT, OpenVINO, NCNN
- **云服务平台：** Azure ML, AWS SageMaker, NVIDIA Triton
- **辅助工具：** Netron（模型可视化）, ONNX-SIM（模型优化）

## Reference

- https://onnx.ai/
- https://github.com/onnx/onnx
- https://onnxruntime.ai/
