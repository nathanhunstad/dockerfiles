
FROM demisto/python3:3.7.5.4583

# No python deps for now
# COPY requirements.txt .

# RUN apk --update add --no-cache --virtual .build-dependencies python-dev build-base wget git \
#  && pip install --no-cache-dir -r requirements.txt \
#  && apk del .build-dependencies

RUN apk --update add --no-cache openssh-client

