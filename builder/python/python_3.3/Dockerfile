FROM bradrydzewski/virtualenv
WORKDIR /home/ubuntu
USER ubuntu
ADD python.sh /etc/drone.d/

# install python 3.3
RUN sudo apt-get update && sudo apt-get install python3.3 python3.3-dev

# setup default virtualenv for python 3.3
RUN virtualenv --python=/usr/bin/python3.3 /home/ubuntu/virtualenv/python3.3 --system-site-packages && \
		. /home/ubuntu/virtualenv/python3.3/bin/activate && \
		pip install --use-mirrors nose && \
		pip install -U pytest