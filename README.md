
Cloud Chatbot is a personal demo project built with PyTorch. It is an AI agent capable of holding meaningful conversations about images. Given an image, dialog history, and a follow-up question, it generates an answer using both visual and textual context. This project demonstrates a fully working visual chatbot running locally on your machine.

The project requires Python 3.6+, Redis Server, RabbitMQ Server, and PyTorch. You can optionally use Anaconda or Miniconda to manage the Python environment. To set up the necessary build essentials and libraries, install git, python-pip, python-dev, autoconf, automake, libtool, libgflags-dev, libgoogle-glog-dev, liblmdb-dev, libprotobuf-dev, libleveldb-dev, libsnappy-dev, libopencv-dev, libhdf5-serial-dev, protobuf-compiler, redis-server, and rabbitmq-server. Enable the RabbitMQ management plugin and restart both Redis and RabbitMQ services.

Create a Python environment and install the required dependencies using pip. Download pretrained models for BUTD, Mask-RCNN, and VisDial, and set up project submodules as needed. Install additional submodules and dependencies including fastText, Pythia for the BUTD captioning model, and Mask-RCNN benchmark for feature extraction. Optionally, install CUDA and cuDNN if you plan to use GPU acceleration. Download the NLTK Punkt tokenizer to enable sentence tokenization.

Set up the database by running the necessary migrations. To run the project, start the worker process and then the development server. Visit http://127.0.0.1:8000 in your browser to interact with Cloud Chatbot. 

The developer of this project is Isha Pal. This project uses the BUTD captioning model from Pythia, the Mask-RCNN feature extractor from maskrcnn-benchmark, and the VisDial model. License: BSD. Credits include the beam-search implementation from AllenNLP and the vqa-maskrcnn-benchmark code. Visual Chatbot images are licensed under CC BY-SA 4.0. All other code and models have been integrated and configured as part of this personal project.

