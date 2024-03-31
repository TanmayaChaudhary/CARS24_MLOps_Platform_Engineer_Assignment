# <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30px">  **Project Name:** Cars24 : MLOps/Platform Engineer Position : Assignment : Train a model on MNIST handwritten digit dataset. <img src = "https://media2.giphy.com/media/3OsFzorSZSUZcvo6UC/giphy.gif?cid=ecf05e47sjg7d63iong5jbzedhgn4btt0fekifdb0xv486im&rid=giphy.gif&ct=g" width="50px" height="50px">

---

## <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30px">**Assignment Overview** <img src = "https://media2.giphy.com/media/3OsFzorSZSUZcvo6UC/giphy.gif?cid=ecf05e47sjg7d63iong5jbzedhgn4btt0fekifdb0xv486im&rid=giphy.gif&ct=g" width="45px" height="45px">
- This project aims to train a model on the MNIST handwritten digit dataset and deploy it using MLOps practices. The assignment includes tasks related to model building, experiment tracking, best model selection, deployment of a FastAPI web app on Docker for inference & Kubernetes deployment files.

---

## <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30px">Architecture<img src = "https://media2.giphy.com/media/3OsFzorSZSUZcvo6UC/giphy.gif?cid=ecf05e47sjg7d63iong5jbzedhgn4btt0fekifdb0xv486im&rid=giphy.gif&ct=g" width="45px" height="45px">
![Architecture Diagram](10.%20Snapshots/10.%20CARS24_MNIST_MLOps_Architecture.png)

---

## <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30px">**Folder Structure:** <img src = "https://media2.giphy.com/media/3OsFzorSZSUZcvo6UC/giphy.gif?cid=ecf05e47sjg7d63iong5jbzedhgn4btt0fekifdb0xv486im&rid=giphy.gif&ct=g" width="45px" height="45px">

1. **requirements.txt**:
   - Contains required libraries to set up the environment.

2. **CARS24_Assignment_Model_Building_Experiment_Tracking.ipynb**:
   - Codes related to dataset loading, preprocessing, model building, model evaluations, experiment tracking, best model selection, local inferencing testing.

3. **mlruns folder**:
   - Contains experiment tracking runs details for each model used.

4. **Best_Model folder**:
   - Contains the best model (Neural Network Model) exported from mlruns folder.

5. **inference_images folder**:
   - contains 3 images for inferencing testing of the model: **0.png (image of 5), 2.png (image of 4), and 3.png (image of 1).**

6. **CARS24_Assignment_Model_WebApp_Deployment.ipynb**:
   - Code related to web app development using FastAPI for the deployment of the best model.

7. **app.py**:
   - Python file containing the final code of the FastAPI web app.

8. **Docker_File folder**:
   - Contains files related to Docker containerization of the best model.
     - Dockerfile: Code related to building the Docker container for the web app.
     - app.py: Python script of the web app.
     - requirements.txt: Requirement file for the web app.
     - Best_Model folder: Contains the best model exported from the MLFlow experiment tracking.
     - docker-compose.yml: Code related to building the Docker image of the web app.

9. **Kubernetes_Deployment_Files folder**:
   - Contains files related to Kubernetes deployment of the Docker container.
     - Kubernetes_Deployment_Files.ipynb: Detailed explanation of the deployment.yaml & service.yaml files.
     - deployment.yaml: Kubernetes deployment code of the Docker container.
     - service.yaml: Services code for Kubernetes deployment of the Docker container.

10. **Snapshots**:
   - Contains some snapshots of outputs.
--- 

## <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30px">Instructions for Setup and Deployment <img src = "https://media2.giphy.com/media/3OsFzorSZSUZcvo6UC/giphy.gif?cid=ecf05e47sjg7d63iong5jbzedhgn4btt0fekifdb0xv486im&rid=giphy.gif&ct=g" width="45px" height="45px">

1. Clone the repository.
2. Create a new virtual environment with Python 3.7.16 using `conda create -n CARS24 python=3.7.16 `.
4. Activate the new virtual environment using `activate CARS24` .
3. Set up the environment using `pip install -r requirements.txt`.
4. Train the model, track experiments & get the best model using `CARS24_Assignment_Model_Building_Experiment_Tracking.ipynb`.
5. Deploy the FastAPI web app using `CARS24_Assignment_Model_WebApp_Deployment.ipynb`.
6. Dockerize the web app using the files in the `Docker_File` folder.
    - 1. Build the Docker image: `docker-compose build`
    - 2. Run the Docker container: `docker-compose up -d`
    - 3. Access the FastAPI app: Visit `http://localhost:8000/predict/` in your web browser
    - 4. Stop the Docker container: `docker-compose down`
7. Deploy the Docker container on Kubernetes using the files in the `Kubernetes_Deployment_Files` folder.

---

## <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30px">Output Snapshots <img src = "https://media2.giphy.com/media/3OsFzorSZSUZcvo6UC/giphy.gif?cid=ecf05e47sjg7d63iong5jbzedhgn4btt0fekifdb0xv486im&rid=giphy.gif&ct=g" width="45px" height="45px">

1. Docker Containerization Process :
![Docker Containerization Process](10.%20Snapshots/Docker_Contanerization.png)

2. Docker Container End To End Testing :
![Docker Container End To End Testing](10.%20Snapshots/Docker_End-To-End_Testing.png)

---

## <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30px">Resources <img src = "https://media2.giphy.com/media/3OsFzorSZSUZcvo6UC/giphy.gif?cid=ecf05e47sjg7d63iong5jbzedhgn4btt0fekifdb0xv486im&rid=giphy.gif&ct=g" width="45px" height="45px">

- [MNIST Dataset](https://www.tensorflow.org/datasets/catalog/mnist)
- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [Docker Documentation](https://docs.docker.com/)
- [Kubernetes Documentation](https://kubernetes.io/docs/home/)

---

**For detailed instructions and explanations, refer to the respective notebooks and files in the repository.**

## <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="30px">**Thanks & Regards,** <img src = "https://media2.giphy.com/media/3OsFzorSZSUZcvo6UC/giphy.gif?cid=ecf05e47sjg7d63iong5jbzedhgn4btt0fekifdb0xv486im&rid=giphy.gif&ct=g" width="45px" height="45px"><br>
## **Tanmaya Chaudhary**
## **MLOps & Generative AI Engineer @ Ernst & Young LLP**

