## How to Code and Publish Your First NPM Package🎖



## Introduction
Hello Developers
In this Article we would learn how do you Code and publish your first NPM package. 
Publishing an NPM package is easy and in this tutorial we would make a very simple package which requires very few lines of Code. 
## What is NPM? 
![logo of npm and node.js](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/f2dlthk3cfechgkgcitq.png)
NPM stands for **Node Package Manager**, as the name suggests it is a package manager, and is also the default package manager for JavaScript runtime environment Node.js.
## Prerequisites

- **Node.js and npm installed in your system**- You can install Node.js and npm(if you haven't already) from [here](https://nodejs.org/en/download/)


- **Basic knowledge of JavaScript**- The package we'll make here is simple so you don't need very high knowledge of JavaScript. 


- **Basic Terminal Commands**- I would be using a few basic terminal commands but I will explain the npm and node commands which I would use in the Article. 


- **A Code editor**- In this tutorial I would be using VS Code but you can use any editor of your choice. 

---

## Lets get Started


<br>

### Step 1: Create an account on https://www.npmjs.com/signup
![npmjs login page](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/hsjv1p7p3eced89ke46j.jpg)
<br>
### Step 2: Login to your CLI by your npm account
To do this, simply type this command in the terminal

```
$ npm login
```
And enter the following details:
![npm login](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/o1um34sl46kk9yauicad.png)
To check if you have successfully logged in, type the following command and it shall print your username:

```
$ npm whoami
```
### Step 3: Setting up the directory
You can accomplish this task by typing these commands onto your terminal/CLI:

```
$ mkdir folder_name
$ cd path/to/folder
```

- `mkdir` - mkdir command is used to create a directory or a folder directly from your Terminal. 

- `cd` - cd command is used to change the current working directory in the terminal. 

### Step 4: Package.json
To initialize the package.json file, type this command in the CLI

```
$ npm init
```
And then answer the questions asked, if you want you can skip any question by clicking Enter. <br>
**What is package.json?**
Package.json is a necessary file which contains information about your project
Such as `package name`, `version`,`author's name` etc. <br>
### Step 5: Let's Code
Now that we have a package.json file, we can get onto coding. 
Create an index.js file and write this code into it

```js
const object = {
  add: function addTwoNumbers(a,b){
    return a+b;
  }
}

module.exports = object;
```
**Code Explanation**

- **const object** - The object `object` which is exported to be used by others.

- **function addTwoNumbers()** - This is the function stored in the object which can be used by others, it is marked as 'add' and it simply returns the sum of two numbers `a` and `b`.

- **module.exports** - the object `object` is then exported by declaring this.

### Step 6: Time to Publish
To publish your newly made npm package, head over to the terminal and type this command

```
$ npm publish
```
If you get this message:

![npm publish success message](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/imri9xw7zxpu5eju86j1.png)
Then congratulations! Your NPM package has been successfully published and can be used by anyone :)
The Github Repository link of this package: https://github.com/HarshSinha17/maths-script
<br>

---

## Testing the package
So now that we have made our NPM package, we shall try it, to test the package follow these steps:
### Create a fresh directory and cd into it
This can now again be done by terminal by the following commands

```
$ mkdir folder_name
$ cd path/to/folder
```
### Initialize the package.json
Type this command on the terminal, but this time with the `-y` flag, so that we don't have to answer any questions and a default package.json file will be created.

```
$ npm init -y
```
### Install the Package
To install the package type this command

```
$ npm install maths-script
```
(Here `maths-script` is the name of the package)
Now a folder named `node_modules` and a file named `package-lock.json` must be created in the directory.
### Lets code
Create a file named `app.js` and paste this code in the file

```js
const maths = require('maths-script');

var a = maths.add(1, 2);
console.log(a);
```
**Code Explanation -**

- The code is pretty simple, first we are storing the exports of the package in a constant `maths`.

- Then we are using the function `add` of the NPM package for adding two numbers, 1 and 2, and storing it in variable `a`, and then printing the var `a` to the console.<br>

### Running the file
To run the file, type this command in the Terminal

```
$ node app.js
```
(app.js is the name of our file)
And then you should get the following output-

![output of the code](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/805nrf8g8h7c0i2nzta5.png)
So we see that the output is `3`, which means that our NPM package is working!

---

<br>
## Conclusion
So in this article we learned how to create an NPM package, hope you found the article helpful and if you face any problem in making your own package, put a comment down below so maybe I can provide any help I can

Thanks
(˵ ͡° ͜ʖ ͡°˵)



 


