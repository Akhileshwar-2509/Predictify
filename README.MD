## AI-Powered Insights Engine

```text
.
├── docs                                  # Documents Folder.
│   ├── github-readme-content                 # Contains GitHub Readme Content.
│   └── project-documentations                # Contains Project-related Documents.
├── research                              # Contains Research files
│   ├── employee-performance-dataset          # Sample Agile-based Employee Performance Dataset.
│   ├── velocity-prediction-analysis          # Research and Analysis on Velocity Prediction.
│   ├── database-schema.txt                   # Database Schema for the Project.
│   └── data-preprocessing-scripts.py         # Scripts for Preprocessing Data.
├── source                                # Contains Source Code (Main Project Folder)
│   ├── 0-resources                           # Contains resources: dataset, requirements.txt
│   ├── 1-ml-model                             # Contains Machine Learning Model Code.
│   └── 2-frontend                             # Contains Frontend Code for Visualization.
├── LICENCE                               # Licence File.
└── README.MD                             # Readme file.
```

## Introduction

The AI-Powered Insights Engine is a robust solution designed to analyze historical employee performance data, uncover key trends, and predict future performance metrics. This project empowers businesses to make data-driven decisions to enhance productivity and team efficiency.

## Features
Data Analysis: Identify performance trends, such as productivity drops or consistent improvements, using historical Agile sprint data.
Prediction: Forecast individual employee performance and team velocity for upcoming months.
API Integration: Expose the AI model as an API to accept input data and return predictions or insights.
Visualization: Frontend dashboard to display trends and predictions with interactive charts and graphs.

![Banner Image](docs/github-readme-content/0-banner-image.jpg)

## Technologies Used
Machine Learning Frameworks: TensorFlow.js, PyTorch, or Scikit-learn.
Database: MySQL for data management.
API Integration: Custom-built API for data communication.
Frontend: Web-based visualization for insights presentation.

## How It Works
Dataset: Utilizes Agile Sprint-based employee performance data, including story points, as input.
AI Model: Processes historical data to identify patterns and predict future performance.
API Endpoint: Exposes the AI model to accept data and return actionable insights.
Frontend Visualization: Displays trends and predictions for better decision-making.

### Monitoring System Features

- Able to count customers.
- Able to welcome customers with a greeting voice.
- Able to welcome visitors in Tamil, Sinhala, and English (Language can be changed in the management system)
- Able to predict the age of customers and categorize them into groups such as kids, teenage, adults, and elders.
- Able to predict gender.
- Able to predict emotions.
- Able to predict customers' race, such as Asian, White, and Black.
- Able to predict whether customers wear a mask or not.
- Able to classify customers' and employees' vocals to identify their sentiments.

### Management System Features

- Able to log in with admin credentials.
- Able to change the monitoring system's welcoming language (Tamil, Sinhala, English)
- There is a line chart on the dashboard to plot the traffics of customers.
- Many pie charts on the dashboard show age groups, genders, emotions, sentiments, and races in a graphical way.
- A page called "Vision Data." stores information about the customer, such as date, time, customer image, emotion, race, gender, age, age group, etc.; it has a filtering option where the admin can search based on dates.
- An "Audio Data" page stores information about the conversations between sales employees and customers, such as the sentiment of their negative, positive, and neutral speeches.
- Able to change the password of the management system.

**Note:** The monitoring system works as it is named and stores those prediction data in the database to be accessed by the management system for further analysis.

### Architecture Diagram

The following architecture diagram explains how this AI Customer Analyzer functions; it typically includes various components and stages that work together to analyze customer data and generate insights. Here is a breakdown of each element and its function:

![Architecture Diagram](docs/github-readme-content/1-architecture-diagram.png)

## Usage
Analyze historical employee performance data for trend identification.
Predict future productivity metrics to optimize team performance.
Visualize data-driven insights in an easy-to-understand format.

![Architecture Diagram](docs/github-readme-content/2-system-flow-digram.png)

## Technology Stack

### Primary Programming Tools

| Programming Tools | Version     | Description                     |
| ----------------- | ----------- | ------------------------------- |
| **Python**        | Ver: 3.9    | Use to build monitoring system. |
| **MySQL**         | Ver: 15.1   | Used as central database.       |
| **Laravel**       | Ver: 10.3.3 | Use to build management system. |

### Python Dependencies (Monitoring System)

| Programming Tools   | Version       |
| ------------------- | ------------- |
| **TensorFlow**      | Ver: 2.11.0   |
| **Keras**           | Ver: 2.11.0   |
| **OpenCV**          | Ver: 4.7.0.68 |
| **MySQL Connector** | Ver: 2.2.9    |
| **PyAudio**         | Ver: 0.2.13   |
| **Pygame**          | Ver: 2.2.0    |
| **imutils**         | Ver: 0.5.4    |
| **deepface**        | Ver: 0.0.79   |

## Repo Structure

**IMPORTANT:** The soruce code of **Monitoring System** and **Management System** are found under the **soruce** folder.

## Setup

This section explains how to deploy AI Customer Analyzer on a new computer. The system has two components: **Monitoring System** and **Management System**.

### Setup Monitoring System

**IMPORTANT:** The soruce code of the monitoring system is found under the following directory

```
ai-customer-analyzer/source/1-monitoring-system
```

#### **Install Dependencies**

This section shows how to install the dependencies easily using the **Anaconda environment** from the requirements.yml. It makes it easy to manage dependencies and create reproducible environments for the projects.

#### **Step 01: Install Anaconda**

The first step is to install Anaconda on the deployed computer: Anaconda is a free and open-source distribution of the Python programming language and a collection of pre-built packages and tools for data science and machine learning. It includes a package manager called "conda" that simplifies the installation and management of packages and dependencies.

- Official Website: https://www.anaconda.com/

#### **Step 02: Navigate to the requirements.yml file directory**

The requirements.yml file is found under this project folder; it could be in the following directory named "monitoring-system-requirements.yml". Navigate to that directory in CMD.

```
ai-customer-analyzer\source\0-resources\1-requirements\monitoring-system-requirements.yml
```

- **The requirements file link:** **[monitoring-system-requirements.yml](source/0-resources/1-requirements/monitoring-system-requirements.yml)**

#### **Step 03: Install the requirements**

**To Install:** After the navigation to the above directory in CMD then issue the following command to install it; An example screenshot is shown below.

```
 conda env create -f monitoring-system-requirements.yml
```

- Example screenshot:

- <img src="docs/github-readme-content/3-install-using-anaconda-env.jpg" alt="Install using Anaconda Environment" width="700" height="500" style="border: 1px solid black;">

**IMPORTANT:** It will take some time to install all the dependencies automatically; after the installation, an environment will be created with the name "ai_customer_analyzer" that environment contains all the required libraries; when running the AI Customer Analyzer project, **always make sure to activate that environment** which has necessary libraries.

**To activate:** Use the following command.

```
activate ai_customer_analyzer
```

**Note:** After the activation, the project can be run on top of that environment.

#### Additional Information

There is some additional information below to learn more about the Anaconda environment.

- To Install Anaconda Environment

```
  conda env create -f environment.yml
```

- To Export Anaconda Environment

```
  conda env export > environment.yml
```

- To Delete Anaconda Environment

```
  conda env remove -n ENV_NAME
```

- To Create an Anaconda Environment

```
  conda create -n ENV_NAME python=3.9
```

### Setup Management System

This section explains how to set up the management system. It is built with Laravel and can be configured quickly on shared hosting or any apache-based servers that run on PHP.

To host it locally on a computer, XAMPP control panel can be used for that. XAMPP is a free and open-source cross-platform web server solution stack package developed by Apache Friends; we can use it for local deployment of PHP-based projects.

Official Website: https://www.apachefriends.org/

**IMPORTANT 1:** The soruce code of the management system is found under the following directory

```
ai-customer-analyzer/source/2-management-system
```

**IMPORTANT 2:** Projects that are built with Laravel can be accessed by opening the **public** folder, in the source code of management system, there is a folder called public, if that opened, it could be accessed, otherwise it won't work, when deploying on servers, it is very important to point to that folder instead of pointing on index.php/index.html.

### Setup Database

The monitoring and management systems use the same database to communicate with each other. Therefore, setting up the database first is essential to make both systems work successfully.

To set the database locally, we can use the XAMPP control panel; there is a MySQL database engine and PHPMyAdmin with it. The database can be found on the following directory.

```
ai-customer-analyzer/source/0-resources/ai_customer_analyzer.sql
```

**IMPORTANT:** Give the database name as **ai_customer_analyzer**.

![MySQL Database](docs/github-readme-content/4-mysql-database-setup.jpg)

### Configuring Database with Monitoring System

This step configures the database with the monitoring system; suppose the database is hosted remotely. Letting the monitoring system know the credentials and the host is essential. Open the JSON file in the following directory to provide the database credentials and host information.

```
ai-customer-analyzer/source/1-monitoring-system/data/database-credentials.json
```

![MySQL Database Credentials](docs/github-readme-content/5-database-credentials-json.jpg)

### Configuring Database with Management System

This step configures the database with the management system; suppose the database is hosted remotely. Letting the management system know the credentials and the host is essential. Open the .env file in the following directory to provide the database credentials and host information.

```
ai-customer-analyzer/source/2-management-system/.env
```

![MySQL Database Credentials](docs/github-readme-content/23-database-management-system.jpg)

**IMPORTANT:** During the running time of the monitoring system, it sends captured information to this database; if the database is hosted somewhere other than localhost, it is important to edit this file.

### Configuring FTP with Monitoring System

When the monitoring system captures images, it uses FTP to send those images to the management panel. Therefore, setting up an FTP account with the monitoring system is essential.

**IMPORTANT 1:** Create an FTP account and point that FTP account to the following directory of the management system; the path is given below.

```
2-management-system\public\dashboard-template-assets\predictions
```

**IMPORTANT 2:** If this project is set up locally, then local FTP server can be used, there are many local FTP servers such as open-source **Filezilla server**.

**IMPORTANT 3:** There is an FTP credentials JSON file in the following directory; edit that file to change the FTP credentials.

```
ai-customer-analyzer\source\1-monitoring-system\data\ftp-credentials.json
```

![FTP Credentials](docs/github-readme-content/6-ftp-credentials.jpg)

## Execution

This section shows how to run the monitoring system and the management system.

### 01 Execution of Monitoring System

The monitoring system can be found on the following directory, "1-monitoring-system", the folder can copied to any place that it wants to be deployed.

```
ai-customer-analyzer/source/1-monitoring-system
```

- Step 01: Activate the environment

```
  conda activate ai_customer_analyzer
```

- Step 02: Execute the vision-analyzer-main.py script

```
  python vision-analyzer-main.py
```

### 02 Execution of Monitoring System with Images

- There is a project under the research folder called "test-images-monitoring-system", this is used to test the system with images to calculate the accuracy, the project is found under the following directory.

  ```
    ai-customer-analyzer\research\test-images-monitoring-system
  ```

- Step 01: Navigate to the following directory to execute the monitoring system to run with images.

```
  ai-customer-analyzer\research\test-images-monitoring-system
```

- Step 02: Place testing images inside the "**input-images**" directory of the project.

```
  ai-customer-analyzer\research\test-images-monitoring-system\input-images\
```

- Step 03: Activate the environment (**Note:** if there is no environment created, no need to activate)

```
  conda activate ai_customer_analyzer
```

- Step 04: Execute the image-analyzer-main.py script

```
  python image-analyzer-main.py
```

![Test with images](docs/github-readme-content/20-tets-with-images.jpg)

### 03 Execution of Audio Processing Script (Monitoring System)

- Step 01: Activate the environment (**Note:** if there is no environment created, no need to activate)

```
  conda activate ai_customer_analyzer
```

- Step 02: Execute the audio-analyzer-main.py script

```
  python audio-analyzer-main.py
```

### 04 Execution of Management System

The management system can be opened using a web browser; it is based on where it is deployed; if it is deployed on localhost, it can be accessed by http://localhost/ and navigate to the **public** folder.

#### Management System Credentials

- Username: **admin**
- Password: **admin**

## Demonstration

This section shows demos of the projects on the monitoring and management systems; some screenshots and demo videos of the project are given below.

#### Login Page

#### Management System Credentials

- Username: **admin**
- Password: **admin**

![Login Page](docs/github-readme-content/13-login-page.jpg)

#### Home Page

![Home Page 1](docs/github-readme-content/14-home-page.jpg)

![Home Page 2](docs/github-readme-content/15-home-page.jpg)

#### Vision Data Page

#### Audio Data Page

![Vision Data Page 1](docs/github-readme-content/18-audio-data-page.jpg)

#### Settings

![Vision Data Page 1](docs/github-readme-content/19-settings-page.jpg)
