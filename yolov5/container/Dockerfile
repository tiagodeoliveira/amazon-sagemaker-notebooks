ARG BASE_IMG=${BASE_IMG}
FROM ${BASE_IMG} 

ENV PATH="/opt/code:${PATH}"

RUN cd opt && git clone https://github.com/ultralytics/yolov5
RUN pip install -r /opt/yolov5/requirements.txt

ENV PATH="/opt/yolov5:${PATH}"

WORKDIR /opt/code
COPY train /opt/code
COPY predict /opt/code