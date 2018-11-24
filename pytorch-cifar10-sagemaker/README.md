# PyTorch Cifar10 SageMaker Sweep

This example uses [AWS SageMaker](https://aws.amazon.com/sagemaker/) to launch a hyperparameter sweep. `train.py` uses
the sagemaker api to launch a sweep. If you run this script outside of a SageMaker notebook instance, you'll need to set the **SAGEMAKER_ROLE** environment variable to an AWS role name that has access to SageMaker, you can find your roles [here](https://console.aws.amazon.com/iam/home?#/roles).

To authenticate with W&B, we call `wandb.sagemaker_auth()` in `train.py`. This will look for W&B credentials in the current environment and pass them to sagemaker.