### Deploy ML model to AWS using FastAPI

AWS app: 

In this exercise, we will build a fastapi ML application and deploy it with continuous delivery on AWS using AWS using Elastic Beanstalk and Code Pipeline.

### ML

To build a ML model, refer the colab notebook under `notebooks` folder.

### FastAPI

To validate the fastapi application locally,

```bash
docker build -t wine .
docker run --rm -it -v $(pwd):/app -p 8000:8000 wine
```

### AWS

To deploy the fastapi application on AWS following steps were taken.

1. Create AWS account.
1. Follow  this tutorial: https://aws.amazon.com/getting-started/hands-on/continuous-deployment-pipeline/

