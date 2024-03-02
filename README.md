# Project Title

## Table of Contents

1. [Steps](#Step-by-Step-Process)
2. [Implementation Details](#implementation-details)
3. [How to Run](#how-to-run)
4. [Additional Information](#additional-information)
5. [Usage](#usage)
6. [Contribution](#contribution)
7. [Dependencies](#Dependencies)
8. [Contact](#contact)



## Introduction
This project aims to create a Django-based API for disease prediction using machine learning models.

## Step-by-Step Process

1. **Requirement Gathering**
    - Understand the problem statement and the data available.
   
2. **Data Preprocessing**
    - Clean and preprocess the dataset to make it suitable for machine learning models.
   
3. **Model Training**
    - Use a machine learning algorithm to train the predictive model on the preprocessed data.

4. **Model Testing and Validation**
    - Test the model with a separate test dataset and validate its performance using appropriate evaluation metrics.
   
5. **Creating Django App**
    - Create a Django app to host the machine learning model. Set up URLs, views, and serializers as necessary.

6. **Adding Dependencies**
    - Add necessary dependencies to `requirements.txt`.

7. **Deployment**
    - Deploy the Django app using a platform like Heroku, AWS, or DigitalOcean. Ensure the environment has all required packages installed.
   
8. **API Testing**
    - Test the API endpoints using tools like Postman or cURL.

9. **Documentation**
    - Write a detailed README.md to help users understand how to use the API, and include a description of the project, implementation details, usage, and other relevant information.
   
10. **Continuous Integration and Deployment (CI/CD)**
    - Set up a CI/CD pipeline to automate testing and deployment processes.

11. **Review and Update**
    - Regularly review and update the project, fix bugs, and incorporate new features if needed.

12. **Feedback and Maintenance** 
    - Gather feedback from users and stakeholders to improve the project. Regularly maintain and update the project to ensure it stays up-to-date and performs optimally.


### These steps provide a broad outline, and the actual process may vary depending on the specific requirements and complexity of the project. It's also important to consider factors like scalability, security, and maintainability throughout the development process.

# This project uses Django and Django Rest Framework to create a simple API for making predictions.

## API Endpoint
- `/api/predict/` - POST method

## Request Format
- Content-Type: application/json
- Body:
  ```json
  {
    "Blood_Pressure_Abnormality": 1,
    "Level_of_Hemoglobin": 15.2,
    "Age": 35,
    "BMI": 25.1,
    "Sex": 1,
    "Pregnancy": 0,
    "Smoking": 0,
    "Chronic_kidney_disease": 1,
    "Adrenal_and_thyroid_disorders": 0
  }

## Implementation Details

This project uses Django Rest Framework's `CreateAPIView` to create an endpoint for making predictions.
The `PredictView` class uses a trained machine learning model stored as a joblib file (`svm_model.joblib`) to make predictions based on input data.
The input data is passed through a Django Rest Framework serializer (`PredictSerializer`) and then fed into the machine learning model.
The prediction result is then returned as a JSON response.

## How to Run

1. Make sure you have Python installed (https://www.python.org/downloads/)
2. Clone this repository: `git clone https://github.com/your-username/your-project-name.git`
3. Navigate to the project directory: `cd your-project-name`
4. Create a virtual environment: `python -m venv venv`
5. Activate the virtual environment:
   - On Windows: `venv\Scripts\activate`
   - On macOS and Linux: `source venv/bin/activate`
6. Install the required packages: `pip install -r requirements.txt`
7. Run the Django server: `python manage.py runserver`


## Additional Information

For more information about the dependencies used in this project, you can refer to their respective documentation:

- [Django Documentation](https://docs.djangoproject.com/en/4.2/)
- [Django Rest Framework Documentation](https://www.django-rest-framework.org/)
- [Gunicorn Documentation](https://docs.gunicorn.org/en/stable/index.html)
- [Joblib Documentation](https://joblib.readthedocs.io/en/latest/)
- [Numpy Documentation](https://numpy.org/doc/stable/)
- [Pytz Documentation](https://pytz.sourceforge.io/)
- [Scikit-Learn Documentation](https://scikit-learn.org/stable/documentation.html)
- [Scipy Documentation](https://docs.scipy.org/doc/scipy/reference/)
- [SQLparse Documentation](https://sqlparse.readthedocs.io/en/latest/)
- [Threadpoolctl Documentation](https://github.com/joblib/threadpoolctl/blob/main/README.md)
- [Tzdata Documentation](https://github.com/eggert/tz/blob/master/README)

Feel free to customize the content based on your project's specific details and requirements.


## Usage

1. Make a POST request to `/api/predict/` with input data in the request body.
2. Receive a JSON response containing the prediction result.
   

## Dependencies

- asgiref==3.7.2
- Django==5.0
- djangorestframework==3.14.0
- gunicorn==21.2.0
- joblib==1.3.2
- numpy==1.26.2
- pytz==2023.3.post1
- scikit-learn==1.3.2
- scipy==1.11.4
- sqlparse==0.4.4
- threadpoolctl==3.2.0
- tzdata==2023.3



## Contribution

1. Fork the repository
2. Clone your forked repository locally
3. Create a new branch (e.g., `feature/xyz`) and make your changes
4. Test your changes locally
5. Push your changes to your forked repository
6. Create a pull request against the original repository

## Contact

For any questions or feedback, feel free to contact me at [email@example.com](tara02664@gmail.com).
