# demo-dvc
This a demo repository to store a project that uses dvc (Data Version Control)

## Example

This demo uses the [Students Performance Dataset](https://www.kaggle.com/datasets/rabieelkharoua/students-performance-dataset) and the code [Student Performance Prediction | 91%](https://www.kaggle.com/code/muhammadmagistra/student-performance-prediction-91).

## Run the demo

### Dependencies
It is necessary to install others tools for this demo before:
* [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [AWS-CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

After installing the AWS-CLI application, set up an AWS profile with credentials to connect to the S3 bucket, follows the [Configuration and credential file settings](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html).

### Install the requeriments

```shell
pip install -r requeriments.txt
```

### Create the DVC local repository

```shell
dvc init
```

### Connect to remote storage
For this demo we will use an AWS S3 bucket as remote storage, but dvc can work with other storage providers, more info [here](https://dvc.org/doc/user-guide/data-management/remote-storage).

```shell
dvc remote add demo-dvc s3://{name_of_bucket}/{path_of_folder}
```

