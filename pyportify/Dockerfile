ARG BUILD_FROM
FROM $BUILD_FROM

RUN apk add --no-cache python3 && \
    python3 -m ensurepip && \
    rm -r /usr/lib/python*/ensurepip && \
    pip3 install --upgrade pip setuptools && \
	pip3 install pyportify 
   




COPY run.sh /
RUN chmod a+x /run.sh

VOLUME /data

EXPOSE 3132

CMD [ "/run.sh" ]

