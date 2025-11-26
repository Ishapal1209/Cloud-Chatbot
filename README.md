
Cloud Chatbot is a personal demo project upgraded to PyTorch. 
Cloud Chatbot is an AI agent capable of holding meaningful conversations about images.
Given an image and a follow-up question, it generates an answer using both visual and textual context.
This project demonstrates a visual chatbot running locally on your machine. 

The project requires Python 3.6+, Redis Server, RabbitMQ Server, and PyTorch. You can optionally use Anaconda or Miniconda for managing the environment. To set up build essentials and libraries on Linux, run: sudo apt-get update; sudo apt-get install -y git python-pip python-dev; sudo apt-get install -y autoconf automake libtool; sudo apt-get install -y libgflags-dev libgoogle-glog-dev liblmdb-dev; sudo apt-get install -y libprotobuf-dev libleveldb-dev libsnappy-dev libopencv-dev libhdf5-serial-dev protobuf-compiler; sudo apt-get install -y redis-server rabbitmq-server; sudo rabbitmq-plugins enable rabbitmq_management; sudo service rabbitmq-server restart; sudo service redis-server restart. 

Clone this repository and download its submodules using: git clone https://github.com/Ishapal1209/Cloud-Chatbot.git and git submodule update --init --recursive. Create and activate a Python environment and install all required dependencies using: conda create -n cloudchat python=3.6.8; conda activate cloudchat; pip install -r requirements.txt. Download pretrained models by running sh viscap/download_models.sh. Install submodules and dependencies by running: cd viscap/captioning/fastText; pip install -e .; cd ../pythia/; sed -i '/torch/d' requirements.txt; pip install -e .; cd ../vqa-maskrcnn-benchmark/; python setup.py build; python setup.py develop; cd ../../../. 

Optionally, install CUDA and cuDNN if you plan to use GPU acceleration. Download the NLTK Punkt tokenizer using python -c "import nltk; nltk.download('punkt)". Set up the database by running python manage.py makemigrations chat; python manage.py migrate. To run the project, open two terminals. In the first terminal, run python worker_viscap.py. In the second terminal, run python manage.py runserver. Visit http://127.0.0.1:8000 in your browser to interact with Cloud Chatbot. 

Developer: Isha Pal. Credits: This project uses the BUTD captioning model from Pythia, the Mask-RCNN feature extractor from maskrcnn-benchmark, and the VisDial model from visdial-starter code. License: BSD.

