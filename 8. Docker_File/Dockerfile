# Use the official Python image as the base image
FROM python:3.8-slim

# Set the working directory in the container
WORKDIR /app

# Copy all files of current directory into the container at /app
COPY . .

# Install any dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose the port that the FastAPI app runs on
EXPOSE 8000

# To suppress the warnings related to missing CUDA and TensorRT libraries.
ENV CUDA_VISIBLE_DEVICES=""  

# Command to run the FastAPI app when the container starts
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8000"]



######################################### Command to Build Docker Container From Docker File ######################################################################################
## 1. Build the Docker image: Open a terminal in the directory containing your Dockerfile and requirements.txt files, and run the following command to build the Docker image:
#     Command to run in CMD :=> docker build -t fastapi-app .
#     This command builds a Docker image named fastapi-app using the Dockerfile in the current directory.

## 2. Run the Docker container: Once the image is built, you can run a Docker container using the following command:
#     Command to run in CMD :=> docker run -d --name fastapi-container -p 8000:8000 fastapi-app
#     This command starts a Docker container named fastapi-container from the fastapi-app image, mapping port 8000 on the host to port 8000 in the container.

## 3. Access the FastAPI app: 
#     You can now access your FastAPI app running in the Docker container by visiting ** http://localhost:8000/predict/ ** in your web browser & provide the image of any 
#     no. between 0 to 9 or 
#     using tools like Postman to send requests to ** http://localhost:8000/predict/ **
#     In Postman attach a file in Body of it as a key value pair & select key type as File :-> file : 2.png

## 4. Stop the Docker container: docker stop CONTAINER_ID_OR_NAME
###################################################################################################################################################################################
