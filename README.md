# New

New is an easy-peasy shell script for creating new directories and files.

The script itself is intentionally verbose with comments, because shell scripts can be dangerous if you don't understand what's going on, and I want even beginners to be able to understand it.

## Usage

So let's say you need to manually create the directories **/src/** and **/public/** with the files **index.css** and **index.js** in one and **index.html** in the other. Previously, you might have handled it something like this:

```shell-script
$ mkdir src public
$ touch src/index.css src/index.js public/index.html
```

Ok, but let's say you want to create the directories **/this/is/just/an/example/**, **/this/one/too/**, **/this/is/necessary/** and **/src/**, and create a bunch of files within each. How many different commands would you have to enter? Too many, is what I presuppose.

Well, with **new**, you'd be able to take care of it with a single command!

```shell-script
$ new src/index.css,index.js public/index.html
```

But **new** is especially useful when creating a complicated bunch of files within subdirectories, like this:

```shell-script
$ new this/is/just/an/example/one.html,one.css,one.js this/one/too/two.jsx,two.scss this/is/necessary/ src/three.c
```

Just group all your subdirectories together, separated by '**/**', and append the argument with all the files you want to create within, separated by '**,**'. You can write as many arguments as you'd like, or write a different command for each. Nothing will be overwritten, nothing will be duplicated—it just works!

## Installation

