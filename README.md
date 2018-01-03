# UI-Testing-mocha-chai-sinon
1. Install mocha and chai -- create a directory as root directory and run
  npm install mocha chai --save-dev        // To test code in browser
  sudo npm install -g mocha                // To also test code in Node.js
  
  These 2 commands will install mocha and chai.  Mocha is the library to allow running test while Chai includes
  helpful functions to verify test results.
2. Testing in the browser
  Create a test runner file under the root directory.  The test runner should look like this.
  testRunner.html
  
<!DOCTYPE html>
<html>
  <head>
    <title>Mocha Tests</title>
    <link rel="stylesheet" href="node_modules/mocha/mocha.css">
  </head>
  <body>
    <div id="mocha"></div>
    <script src="node_modules/mocha/mocha.js"></script>
    <script src="node_modules/chai/chai.js"></script>
    <script>mocha.setup('bdd')</script>

    <!-- load code you want to test here -->

    <!-- load your test files here -->

    <script>
      mocha.run();
    </script>
  </body>
</html>

  Create a directory structure for tests. To simplify, create a test/ directory under the root directory.  Then
  insert test files in this test directory.
  
3. Testing in Node.js
  There is no need for the test runner.  Just remember to add the line var chai = require('chai'); at the top of the
  test files.


  
  
