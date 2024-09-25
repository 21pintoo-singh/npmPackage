How to Create and Publish an NPM Package – a Step-by-Step Guide
1. Install Node 1st step
2. Initialize a Git Repository
git init
3. Initialize NPM in Your Project
npm init
4. Add Your Code
Now, you can go ahead and add the code for your package.

First, you need to create the file that will be loaded when your module is required by another application. For this tutorial, that will be the index.js file.

Inside the index.js file, add the code for your package.

For this tutorial, I will be creating a simple package called first-hello-npm. This package returns the string "Hello NPM!".
After creating your function, you should export it like in the example above. That way, anyone who downloads your package can load and use it in their code.

If you have been following along, you should now have your package created. But before you publish, you need to test your package. Testing your package reduces the chances of publishing bugs to the NPM registry.
How to Test Your NPM Package
Testing ensures that your NPM package works as expected. There are many ways to test your package. In this tutorial, you will learn one of the simplest ways of testing.

First, navigate to the root of your package project. Then, run the following command:

<npm link>
This will make your package available globally. And you can require the package in a different project to test it out.

Create a test folder. And inside that test folder, add a litmus.js file.
In the example above, the test folder contains only the script.js file. It does not yet contain the package. To add the package you created to your test folder, run the command below:

<npm link <name-of-package>

In the case of the test folder for this tutorial, I will run the following command:

<npm link pintoosingh>
This will create a node-modules folder. And it'll add all the files and folders from your package.

In the litmus.js file, you can now require your package and use it for the test.

The first-hello-npm package is expected to return the string "hello NPM!". As you can see from the screenshot below, the package works as expected when I run the script.
After testing your package and ensuring it works as expected, you can now publish it on the NPM registry.

<npm login>
You will get a prompt to enter your username and password. If login is successful, you should see a message like this:

Logged in as <your-username> on https://registry.npmjs.org/.

You can now run the following command to publish your package on the NPM registry:

<npm publish>

ou can visit the NPM website and run a search for your package. You should see your package show up in the search results.

How to Publish Scoped NPM Packages
If an existing package has the same name you would like to use, the workaround is to publish a scoped package.

When you publish a scoped package, you have the option to make it public or private. If it's private, you can choose who you want to share the package with.

How to Create a Scoped NPM Package
To create a scoped package, first navigate to the root of your package directory.

Then, run the npm init command and pass your username as the value to the scope flag:
<npm init --scope=@your-username
Respond to the prompts to create a package.json file. For your package name, the format should be @your-username/package-name.

For example <@benjaminsemah/pintoosingh>

You can now add the code for your package and test it. The process is the same as already explained above.
Then, to publish your scoped package, run the following command in your terminal.
<npm publish --access public
You can change from public to private if you don't want to make the package available for public use.

https://www.npmjs.com/search?q=pintoosingh
