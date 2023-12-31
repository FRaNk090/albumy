# Albumy

*Capture and share every wonderful moment.*

> Example application for *[Python Web Development with Flask](https://helloflask.com/en/book/1)* (《[Flask Web 开发实战](https://helloflask.com/book/1)》).

Demo: http://albumy.helloflask.com

![Screenshot](https://helloflask.com/screenshots/albumy.png)

## Installation

**Clone:**
```
$ git clone https://github.com/greyli/albumy.git
$ cd albumy
```

**Prerequisites for using Azure API:**

* An Azure subscription - *[Create one for free](https://azure.microsoft.com/en-us/free/ai-services/)*
* *[Python 3.x](https://www.python.org/)*
  * Your Python installation should include *[pip]*(https://pip.pypa.io/en/stable/). You can check if you have pip installed by running ```pip --version``` on the command line. Get pip by installing the latest version of Python.

* Once you have your Azure subscription, *[create a Vision resource](https://portal.azure.com/#create/Microsoft.CognitiveServicesComputerVision)* in the Azure portal to get your key and endpoint. After it deploys, select Go to resource.
  * You need the key and endpoint from the resource you create to connect your application to the Azure AI Vision service.
  * You can use the free pricing tier (F0) to try the service, and upgrade later to a paid tier for production.

**Create environment variables:**
* Go to the Azure portal. If the resource you created in the Prerequisites section deployed successfully, select **Go to resource** under **Next Steps**. You can find your key and endpoint under **Resource Management** in the **Keys and Endpoint** page. Your resource key isn't the same as your Azure subscription ID.

* To set the environment variable for your key and endpoint, open a console window and follow the instructions for your operating system and development environment.

1. To set the VISION_KEY environment variable, replace your-key with one of the keys for your resource.
2. To set the VISION_ENDPOINT environment variable, replace your-endpoint with the endpoint for your resource.
```
export VISION_KEY=your-key
export VISION_ENDPOINT=your-endpoint
```

**Create & activate virtual env then install dependency: with conda**

```
$ conda create --name albumy python=3.8
$ conda activate albumy
$ pip install -r requirements.txt
```

**Installing Vision API**
```
$ pip install --upgrade azure-cognitiveservices-vision-computervision
```
**Generate fake data then run:**
```
$ flask forge
$ flask run
* Running on http://127.0.0.1:5000/
```
**Test account:**
* email: `admin@helloflask.com`
* password: `helloflask`

## License

This project is licensed under the MIT License (see the
[LICENSE](LICENSE) file for details).
