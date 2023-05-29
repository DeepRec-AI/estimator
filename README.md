# DeepRec Estimator

Estimator for DeepRec is based on TensorFlow Estimator, which is high-level TensorFlow API that greatly simplifies machine learning programming.
Estimators encapsulate training, evaluation, prediction, and exporting for your model.

New features in DeepRec Estimator:
-   Support GRPC++ for large scale distributed training in parameter server mode.
-   Support StarServer for large scale distributed training in parameter server mode.

## Installation

### Prepare for build

**CPU Dev Docker**

| GCC Version | Python Version |                           IMAGE                           |
| ----------- | -------------- | --------------------------------------------------------- |
|   9.4.0     |    3.8.10      | alideeprec/deeprec-build:deeprec-dev-cpu-py38-ubuntu20.04 |

**GPU(cuda11.6) Dev Docker**

| GCC Version | Python Version | CUDA VERSION |                           IMAGE                                 |
| ----------- | -------------- | ------------ | --------------------------------------------------------------- |
|    9.4.0    |    3.8.10      | CUDA 11.6.2  | alideeprec/deeprec-build:deeprec-dev-gpu-py38-cu116-ubuntu20.04 |

### Build from source

Develop Branch：master, Latest Release Branch: deeprec2302

**Build Package Builder**

```bash
bazel build //tensorflow_estimator/tools/pip_package:build_pip_package
```

**Build Package**

```bash
bazel-bin/tensorflow_estimator/tools/pip_package/build_pip_package /tmp/estimator_whl
```

Installing DeepRec will install the native tensorflow-estimator by default, please reinstall the compiled Estimator.

## More details

* [GRPC++](https://github.com/DeepRec-AI/DeepRec/blob/main/docs/docs_en/GRPC%2B%2B.md)
* [StarServer](https://github.com/DeepRec-AI/DeepRec/blob/main/docs/docs_en/StarServer.md)

See TensorFlow Estimator [getting started guide](https://www.tensorflow.org/guide/estimators) for an introduction to the Estimator APIs.
