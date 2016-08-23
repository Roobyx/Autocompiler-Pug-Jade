# Autocompiler-Pug-Jade

Compile .PUG and .JADE files directly in Atom

[Atom package site](https://atom.io/packages/jade-autocompile)

## Be aweare that the PUG compiling is still work in progress and some features might not work

* In the pug files multiple line comments MUST start with "//" at every new line

## Set up
The two first comment blocks of file can be used to pass parameters to the compiler.

* The first one must have the name of the output html file, like this:

  ```.jade / .pug
  //output:output.html
  ```
  If you avoid this comment, the file is omitted by the compiler.

  The output parameter supports relatives paths and two variables replacement.
  * $1: Name of the original jade file
  * $2: Extension of the original file.

  Also you can add other properties to the compiler, like this:
  ```.jade / .pug
  //output:output.html, pretty:false
  ```

* The second block can have a javascript object to be used as locals for the compiler.

  ```jade
  //{
      name: 'Jack',
      date: new Date,
      myFunc: function(){
        return true;
      }
    }
  ```

## This package is built on top of jade-autocompile Atom extension by Manuel Rueda" - https://atom.io/users/ManRueda

## License
  The MIT License (MIT)

  Copyright (c) 2016 Marian Radev

  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in all
  copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
  SOFTWARE.
