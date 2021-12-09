### Deploy ML model to AWS using FastAPI

AWS app: http://wine-ratings.us-east-1.elasticbeanstalk.com/

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

2. Under `Elastic Beanstalk`, create a environment. Select `Docker` under `Platform` section. 

3. Zip the contents of repo using command below and upload the file to `Application code` section. Creating environment takes fair amount of time.

   ```bash
   cd 6-fastapi-ml-aws-serverless
   zip -r -D code.zip .
   ```

4. In next step, we will use `Code Pipeline` for continuous delivery using Github event trigger. Create a pipeline that connects the source code to Elastic beanstalk application.

