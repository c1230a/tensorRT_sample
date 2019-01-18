FROM nvcr.io/nvidia/tensorrt:18.12-py3

WORKDIR /workspace/tensorrt/samples

RUN /opt/tensorrt/python/python_setup.sh

ENV CUDA_INSTALL_DIR=/usr/local/cuda-10.0

ENV CUDNN_INSTALL_DIR=/usr/include

RUN make -j

WORKDIR /workspace/tensorrt/samples/python/introductory_parser_samples

CMD ["python", "caffe_resnet50.py", "-d", "/workspace/tensorrt/python/data"]
