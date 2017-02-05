FROM floydhub/dl-docker:cpu
MAINTAINER mynameisvinn

# copy script and models_places dir into working directory
COPY . /root/caffe

# fetch pretrained model prototxt and weights
WORKDIR /root/caffe
RUN wget http://places2.csail.mit.edu/models_places365/resnet152_places365.caffemodel
RUN wget https://raw.githubusercontent.com/SumanthReddyKaliki/places365/master/deploy_resnet152_places365.prototxt
RUN mv resnet152_places365.caffemodel deploy_resnet152_places365.prototxt models_places

# clean up
# RUN rm -rf matlab models scripts docker examples docs cmake data python src tools
RUN rm INSTALL.md Dockerfile Makefile Makefile.config.example CMakeLists.txt LICENSE CONTRIBUTORS.md README.md 
