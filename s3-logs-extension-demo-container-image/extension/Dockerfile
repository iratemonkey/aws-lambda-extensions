FROM python:3.8-alpine AS installer
#Layer Code
COPY extensionssrc /opt/
COPY extensionssrc/requirements.txt /opt/
RUN pip install -r /opt/requirements.txt -t /opt/extensions/lib

FROM scratch AS base
WORKDIR /opt/extensions
COPY --from=installer /opt/extensions .