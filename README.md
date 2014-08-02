# Jon Ward Portfolio Site

####Introduction

Minimalist Responsive Grid Site designed by Jon Ward, Developed By Owain Llewellyn

#### Requirements
Make sure your have the following installed with these versions or greater when running the bootstrap

* ```Node v0.10.26```

#### Installation

There are several hoops you may have to jump through to get all dependencies installed, but hopefully alot of this stuff will be on your machine anyway.

##### Installing Ruby dependencies

First we need to install bundler

```
gem install bundler
```

Then we need to get the rest of our ruby dependencies (Sass, Neat Bourbon)

```
bundle install
```

#### Installing Tooling dependencies (Grunt tasks, Bower)

```
npm install
```

To require libraries that are not in the commonjs format we are going to use napa to get them and wrap them for easy inclusion with browserify.

```
npm install -g napa
```

#### Library dependencies (Client Libraries)

```
bower install
```

#### Image optimisation dependencies

To run optimisations over images we use GraphicsMagick, to install we need to use brew. If your on mac and do not have brew installed you'll need to go ahead and get that setup.

```
ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"
```

If your on windows you will need to download the binary and install it manually on your machine. You can get the binary [here](http://www.graphicsmagick.org/download.html).

Now we can install GraphicsMagick


```
brew install GraphicsMagick
```

#### Running Tests

To run tests we need PhantomJS and jasmine



Jasmine will come installed as part of the ```npm install``` task. PhantomJS, will need to be installed using brew, see previous step to install Brew if you don't already have it.

 ```
 brew install phantomjs
 ```

#### Starting grunt

We have five targets we can run ```dev```, ```dist```, ```server```, ```styleguide``` and ```docs```.

```dev``` is pretty optimised but gives you source maps and does not optimise images as much as ```dist```. The dist target is highly optimised and is production ready. Use this when building to a production server. Spinning up a simple http server you'll use the ```server``` target. It comes with live reload turned on. The final target ```docs``` produces a one time hit of the yui docs and places it in the dist folder. this same task will also run as part of the ```dist``` task mentioned previously.

The style guide task generates a folder named ```style_guide``` and is a base for building out your ui elements. Elements can be styled and catalogued here for use in the main dev folder. For more information around style guides look no further than [Twitter bootstrap](http://getbootstrap.com/).


The tasks are pretty self explanatory, but for the purpose of this documentation I've listed them below:

#### Development target

```
grunt dev
```

#### Production target

```
grunt dist
```

#### Server target

```
grunt server
```

#### Style Guide target

```
grunt styleguide
```

#### Docs target

```
grunt docs
```

