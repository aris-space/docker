FROM nikolaik/python-nodejs:python3.8-nodejs13

RUN git clone https://github.com/aris-space/aris-euler-sim-con

WORKDIR /aris-euler-sim-con

RUN python3 -m pip install --user --no-cache-dir -r requirements-py.txt

RUN npm install
RUN ./node_modules/.bin/webpack --config build/webpack.dev.conf.js

EXPOSE 80

CMD bash -c "python3 manage.py runserver 0.0.0.0:80"
