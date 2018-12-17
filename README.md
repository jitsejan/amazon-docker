# amazon-docker
Install the required Python libraries inside the Amazon Python 3.6 image

##
Some Python libraries (i.e. `pandas`) are installed differently for different operating systems. The `pandas` library
will not work when it is installed on Windows and deployed to AWS Lambda. In order to circumvent this the libraries should be
installed using the Docker image for the Amazon environment the Lambda function is running in.

## Howto

1. Change the `requirements.txt` to include the required Python libraries
2. Run `docker-compose up` in the folder
3. Copy the results of the `pipper` folder in the build folder for your Amazon Lambda function
4. Deploy your Lambda function 
