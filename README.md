learn-mocha [WORK IN PROGRESS . . . *DONT READ* THIS *YET*!! :-]
===========

*Quick Guide* to **mocha.js** **T**est **D**riven **D**evelopment (TDD) / 
**B**ehaviour **D**riven **D**evelopment (BDD) in **node.js**

![Cowboy Coder](https://raw.github.com/nelsonic/learn-mocha/master/images/cowboy-coder.png "Cowboy Coder")

We all know *Cowboy Coders*. (*If you don't, its you!*) 

The "*I just get things done*" developer who writes "*quick fixes*" and 
maintains "*I don't have time to write tests*" or 
"*Writing tests for my code takes longer*" ... **Utter Nonsense**!

- - -

#### Installation

```sh
sudo npm install -g mocha
```

See: http://visionmedia.github.io/mocha/#installation

#### First Tests

```sh
sudo npm install -g mocha
```

You should see some output *confirming* it *installed*:

![Mocha Installed](https://raw.github.com/nelsonic/learn-mocha/master/images/mocha-installed.png "Mocha Installed Successfully")

#### Create "./test" Directory

In your project create a new directory to hold your tests:

```sh
mkdir test
```

#### Your Tests Live in ./test/**test.js**

Now create a new file ./test/**test.js**:

```sh
vi ./test/test.js
```

and write/paste the following code:

```javascript
var assert = require("assert"); // node.js core module

describe('Array', function(){
  describe('#indexOf()', function(){
    it('should return -1 when the value is not present', function(){
      assert.equal(-1, [1,2,3].indexOf(4));
    })
  })
})
```

#### Run Test 

By typing the command **mocha** in your terminal the mocha comand line program
will look for a **/test** directory and run any **.js** files it conains:

```sh
mocha
```

![Mocha 1 Test Passes](https://raw.github.com/nelsonic/learn-mocha/master/images/mocha-1-test-passing.png "Mocha 1 Test Passes")

### A More Useful Example (Cash Register Mini Project)

While I'm the first to 


#### Module File

Create a new file for our cash register **register.js**:

```sh
vi register.js
```

And add the following code:

```javascript


```


- - -



#### What is Mocha?

Mocha is a **JavaScript test framework** running on **node.js** 
*and* the **browser**.

![Mocha Logo](https://raw.github.com/nelsonic/learn-mocha/master/images/mocha-logo.png "Mocha Logo")

Made by [TJ Holowaychuk](https://twitter.com/tjholowaychuk) creator of 
[Express](https://github.com/visionmedia/express) (*by far* the *most popular* 
node.js web framework), Mocha is TJ's answer to the problem of testing JavaScript.

- Site: http://visionmedia.github.io/mocha/
- Code: https://github.com/visionmedia/mocha

#### Why Mocha?

At last count there were 83 testing frameworks *listed* on the node.js 
modules page: https://github.com/joyent/node/wiki/modules#wiki-testing 
this is *both* a problem (*too much choice* can be
*overwhelming*) and good thing (diversity means new ideas and innovative 
solutions can flourish).

There's no hard+fast rule for "*which testing framework is the best one*?"

Over the past 3 years I've tried: 
[Assert (Core Module)](http://nodejs.org/api/assert.html),
[Cucumber](https://github.com/cucumber/cucumber-js),
[Expresso](https://github.com/visionmedia/expresso)
[Jasmine](https://github.com/mhevery/jasmine-node), 
[Mocha](http://visionmedia.github.io/mocha/), 
[Nodeunit](https://github.com/caolan/nodeunit), 
[Should](https://github.com/visionmedia/should.js), and
[Vows](https://github.com/cloudhead/vows)

My **criteria** for chosing a testing framework: 

- **Simplicity** (one of TJ's *stated aims*)
- **Elegance** (*especially when written in CoffeeScript*)
- **Speed** (Mocha is *Fast*. 300+ tests run in under a second)
- **Documentation** (plenty of real-world examples: http://visionmedia.github.io/mocha/)
- **Maturity** (*Battle-tested* by *thousands* of developers!)

Advanced: 

- Easy to Trouble-shoot (Plenty of *Answered* Questions on 
[stackoverflow](http://stackoverflow.com/questions/tagged/mocha?sort=frequent&pageSize=15))
- Automatic Test Running when File Changes (using 
[Watchr](https://github.com/bevry/watchr)/[Grunt](http://gruntjs.com/))
- Detailed reports of test execution (extensible reports!)


### Notes

#### Other Mocha Tutorials/Background

- DailyJS Mocha: http://dailyjs.com/2011/12/08/mocha/
- Azat's Mocha Tutorial: http://webapplog.com/test-driven-development-in-node-js-with-mocha/
- NetTuts: http://net.tutsplus.com/tutorials/javascript-ajax/better-coffeescript-testing-with-mocha/
- Code Coverage: http://stackoverflow.com/questions/16633246/code-coverage-with-mocha

- Grunt.js Mocha Plugins: http://gruntjs.com/plugins/mocha

#### Further Reading

- Testing takes "*twice as long*" (Myth): http://googletesting.blogspot.co.uk/2009/10/cost-of-testing.html
- Estimating Testing Effort as % of Development Time: http://stackoverflow.com/questions/1595346/estimating-of-testing-effort-as-a-percentage-of-development-time
- Technical Debt (Bad Code): http://jessewarden.com/2010/07/agile-chronicles-12-technical-debt.html
- Agile = an excuse for cowboys? Discussion: http://programmers.stackexchange.com/questions/11188/is-the-agile-approach-too-much-of-a-convenient-excuse-for-cowboys
- TDD Examples: http://stackoverflow.com/questions/1920259/recommend-good-online-sample-walkthrough-of-tdd/7213630#7213630

- - -

#### Trying to think of a good example for TDD ...

- Bowling: http://www.objectmentor.com/resources/articles/xpepisode.htm
- Sudoku: http://johannesbrodwall.com/2010/04/06/why-tdd-makes-a-lot-of-sense-for-sudoko/
- Vending machine.
- Cash Register.
- Roman Numerals: http://www.diveintopython.net/


#### Rant

Code without tests is like a *building without a foundation*! 

![Building Collapse](https://raw.github.com/nelsonic/learn-mocha/master/images/building-collapse-940x627.jpg "Building Collapse")

Its only a matter of *time* before it all comes crashing down ...

Is Test Driven Development (TDD) a *silver bullet* for *all* my software
development woes? *Short answer*: **No**. 
There is a *lot* more that goes into writing *great* software than 
*just* having tests. But *without tests* reliability is *impossible*.

If you are *not* doing TDD in your projects I'm probably not going to be 
the one to change your mind by evangelizing about it. I know plenty of
people calling themesleves "developers" who stubbornly cling to the idea 
that testing is for "QA" or "That's why we have testers" and wish them 
nothing but the best of luck! I just cant't work with you or use your 
"product", no hard feelings. :-)
    