<div align="center">
  <img alt="New logo" src="https://res.cloudinary.com/ulitroyo/image/upload/v1534282830/New_logo.svg" width=250px />
  <h1>New</h1>  
</div>

**New** is an easy-peasy shell script for creating new directories and files.

The script itself is intentionally verbose with comments, because shell scripts can be dangerous if you don't understand what's going on, and I want even beginners to be able to understand it.

- [Usage](#usage)
- [Installation](#installation)
- [Roadmap](#roadmap)

## Usage

So let's say you need to manually create the directories `/src/` and `/public/` with the files `index.css` and `index.js` in one and `index.html` in the other. Previously, you might have handled it something like this:

```shell-script
$ mkdir src public
$ touch src/index.css src/index.js public/index.html
```

Well, with **New**, you'd be able to take care of it with a single command!

```shell-script
$ new src/index.css,index.js public/index.html
```

Ok, but let's say you want to create the following directories:
 - `/this/is/just/an/example/`
 - `/this/one/too/`
 - `/this/is/necessary/`
 - `/src/`
 
Let's also say you want to create a bunch of files within each. How many different commands would you have to enter? Too many, is what I presuppose.

Lucky you! **New** is especially useful when creating a complicated bunch of files within subdirectories, like this:

```shell-script
$ new this/is/just/an/example/one.html,one.css,one.js this/one/too/two.jsx,two.scss this/is/necessary/ src/three.c
```

Just group all your subdirectories together, separated by a slash (/), and append the argument with all the files you want to create within, separated by commas (,). You can write as many arguments as you'd like, or write a different command for each. Nothing will be overwritten, nothing will be duplicated—it just works!

## Installation

**New** is a single-file script, so this is what I suggest you do:

### 1. Make a new directory for New
If you don't already have a directory where you keep all your shell scripts, make one now. I suggest `~/bin` or `~/scripts`.

### 2. Add the directory to your PATH
If you made a new directory in step 1, you probably need to add it to your PATH. To do so, you can go into your `.bashrc` or `.bash_profile` (assuming you have one, more info below), and add the line `export PATH=/your/directory:$PATH`. If you follow the example above, then, you'd add the line `export PATH=~/scripts:$PATH`.

   (If you're new to the command line, PATH is an [environment variable] that contains a list of directories. Your terminal will look inside this list when it's trying to resolve a command or script. This is useful so you don't always have to type out the directory in which the script resides, so instead of typing in `~/scripts/new`, you can just type `new`.)  
   
   (Also, `.bashrc` or `.bash_profile` is a [configuration file] for your terminal where you can add all your customizations. It's an easy an worthwhile topic, so you should familiarize yourself with it, and make some customizations of your own. By the way, `.bashrc` is just a regular text file; the dot just indicates it's hidden, as most config files are. You can view all the hidden files within a directory by adding typing `ls -a` into your terminal.)  
   
### 3. Make your New file
Copy/paste the **New** source code from the file above into your own file. I mean, you could clone the code if you really want to, but it's much easier to just create a new file in your favorite code editor and CTRL + V the code into it. Save it as 'new' without any extensions. If anything, you can change the syntax hightlighting to 'bash' or 'shell-script' but that's about it.

### 4. Make your New file executable
Go into your scripts directory where your new **New** file resides, and type:

```shell-script
$ chmod 755 new
```

This permissions setting will make **New** executable for everyone on the machine. If you want to make it executable only for yourself (its owner), you can use setting 700 instead of 755.

You're done! Enjoy **New**!

## Roadmap

The following features are in the works:

- Add help tag with usage notes
- Add jump tag to select which new directory to jump into
- Add verbose tag to log output




[environment variable]: https://codeburst.io/linux-environment-variables-53cea0245dc9
[configuration file]: https://www.maketecheasier.com/what-is-bashrc/
