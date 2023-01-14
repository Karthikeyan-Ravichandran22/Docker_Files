FROM continuumio/miniconda3

LABEL maintainer="Jonathan Fernandes <theolympicsguy@gmail.com>"
LABEL description="Dev environment for machine learning and data science team \
                  with access to shared data in network drive."

WORKDIR /data

RUN conda install jupyter -y && \
    conda install python==3.10 -y && \
    conda install pandas==1.5.2 -y && \
    conda install seaborn==0.12.2 -y && \
    conda clean -y -all

EXPOSE 8888

VOLUME /data

CMD ["jupyter","notebook","--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]
