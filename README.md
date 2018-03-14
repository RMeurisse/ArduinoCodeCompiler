This repository is part of the [codebender.cc](http://www.codebender.cc) maker and artist web platform.

## And what's that?

codebender fills the need for reliable, easy to use tools for makers, a need that couldn't be completely fulfilled by any existing solution according to our experience. 

Things like installing libraries or the IDE and updating software sometimes were (and still are) quite a painful process. But in addition to the above, the limited features provided (e.g. insufficient highlighting, indentation and autocompletion) got us to start codebender, a completely web-based IDE that requires virtually no installation and offers a great code editor. Plus it stores your sketches on the cloud. Yeah!

With your code on the cloud, you can access your sketches safely even if your laptop is stolen or your hard drive fails! codebender also compiles your code giving you extremely descriptive error descriptions on terrible code. There's even more, you can upload your code to your Arduino straight from the browser.

## How does the compiler come into the picture?

The compiler repository includes all the necessary files needed to run the compiler as a service. It receives the code as input and outputs the compiled output if the compilation was successful or the errors present in the code. We provide an easy interface to send the code to the compiler.

Here's a list of open source projects we use
* Clang
* gcc-avr
* avr binutils (avrsize)

For development we've run it on a variety of Linux and Mac OS X machines.

## How to install

Check out the code in any directory you wish

`git clone https://github.com/RMeurisse/ArduinoCodeCompiler.git`

Then cd in the created directory (if you run the command as is above, it would be named `compiler`) and run

`cd ArduinoCodeCompiler`
`bash scripts/install.sh`

(don't cd into scripts directory and run install.sh from there, it won't work)

If you now visit `http://localhost/status` you'll see a JSON response telling you everything's ok: 
`{"success":true,"status":"OK"}`

## Making changes
It is important to install composer to make changes to the project! 
If you made changes, recommended to run `app/console cache:clear`.
Starting the server can be done by running `app/console server:run`.

## What's next?

Visit the [wiki](https://github.com/codebendercc/compiler/wiki) for more information.
