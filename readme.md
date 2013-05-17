speedcoach
==========

Benchmark node.js modules to make them faster and lighter

Installation:

    npm install speedcoach

Command line usage:

    speedcoach express
    speedcoach space
    speedcoach fs 

Using in a script:

    var speedcoach = require('speedcoach')
    speedcoach('start')
    
    var numbers = []
    for (i = 0 ; i < 99999; i++) {
      numbers.push(i)
    }
    
    speedcoach('array initialized')
    
    var string = ''
    for (i = 0 ; i < 99999; i++) {
      string += i
    }
    
    speedcoach('string created')
    
    console.log(speedcoach.times())

Running that script:

    node example.js

Example output:

    0.1S array initialized to string created +10.9MB 
    0.0S start to array initialized +0.9MB