# Flask + ReactJS + Webpack + Bootstrap + Socket.IO + Subprocess

Buzzwords...


But this is the truth: By cloning this repo and following the
instructions you might get a working flask app that can ping arbitrary
domains when the client asks for it.

The client is a [webpack-powered](https://webpack.github.io/),
[ReactJS](https://facebook.github.io/react/) app styled by
[bootstrap](http://getbootstrap.com).


## Get it running in less than 300 seconds


#### step 1/4: install python dependencies

please be tidy, do this in a [virtualenv](https://virtualenv.pypa.io/en/latest/)

```bash
mkvirtualenv flask-react
pip install -r requirements.txt
```


#### step 2/4: install npm dependencies

and enure that the executables are visible in the `PATH`

```bash
npm install
export PATH=`pwd`/node_modules/bin:$PATH
```

#### step 3/4: compile assets with webpack

webpack will turn the

```bash
make static
```

#### step 4/4: run the app

this will also serve the static files

```bash
make run
```


# FAQ


### How do I deploy this stuff ?

**Check the [`Makefile`](Makefile) it has a `web` target that calls gunicorn**

Also: https://flask-socketio.readthedocs.org/en/latest/