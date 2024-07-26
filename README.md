# Rohit-New-Portfolio

Live Link : https://rohit-portfolio-wcvt.onrender.com/

Adding Tailwind CSS to HTML can be done using more methods, such as using a CDN, or the recommended method by getting Tailwind via a package manager and using PostCSS to process the configuration file.

Include Tailwind CSS via CDN
If you want to quickly get started using Tailwind CSS and play around with the utility-first classes, just include the following CDN link inside the <head> tag of your HTML template:

    
<link href="https://unpkg.com/tailwindcss@^1.0/dist/tailwind.min.css" rel="stylesheet">
    
After you’ve done that, you should be able to use the classes from Tailwind CSS. Check out our latest Tailwind CSS tutorial where we show you can build a responsive navigation bar and hero section with a sign up form using the utility-first classes from Tailwind CSS.

Install Tailwind CSS via NPM and process the configuration file using PostCSS
Although it requires a bit more setup and it requires further knowledge of the terminal and JavaScript, it is most definitely the best way to make use of all of the features that Tailwind CSS can provide.

First of all, you need to make sure that you have Node and NPM installed on your machine. If you do, run the following command in the root directory of your project to initialize the NPM configuration file:

    
npm init
    
You will be asked some questions regarding the project title, description, versioning and so on. The package.json file will mostly hold information about your project and the dependencies that you need, such as Tailwind CSS.

Afterward, install Tailwind CSS using the following command:

    
npm install tailwindcss --save
    
This will add Tailwind CSS as a project dependency, and also install the library files inside the node_modules folder. The --save tag ensures that the library is added to the package.json file.

Create a CSS file and include the Tailwind CSS directives
Now that you have Tailwind CSS installed locally, create a main.css file and add the following code to inject the Tailwind CSS code:

    
@tailwind base;

@tailwind components;

@tailwind utilities;
    
These directives will be swapped by the actual Tailwind CSS classes when using PostCSS later in this guide.

Setup the Tailwind configuration file
This is an important step to set up a configuration file for Tailwind CSS so that you can later easily customize the classes by modifying and adding new colors, fonts, sizings, shadows and so on.

This is a huge advantage compared to using only the CDN of the framework, because using the configuration file you can actually change the framework based on your needs, whereas if you only use the CDN you would need to write extra classes, overriding the default Tailwind CSS classes.

Run the following command in your terminal to generate a tailwind.config.js file:

    
npx tailwindcss init
    
By running this command, a new configuration file called tailwind.config.js will be generated with the following code:

    
// tailwind.config.js
module.exports = {
    future: {},
    purge: [],
    theme: {
    extend: {},
    },
    variants: {},
    plugins: [],
}
    
Processing Tailwind CSS
The last step to include Tailwind CSS into HTML using the recommended PostCSS method is to add the following to plugins inside the configuration file and then run the command that will process your configuration file and the main.css file:

    
module.exports = {
    plugins: [
    // ...
    require('tailwindcss'),
    require('autoprefixer'),
    // ...
    ]
}
    
And run the following command in your terminal to process your files:

    
npx tailwindcss build main.css -o output.css
    
This will generate a new CSS file called output.css which you need to include in your HTML file. All you need to do now is to add the following code in your HTML template:

    
<link href=”./output.css” rel=”stylesheet”>
    
Congratulations! Now you should have Tailwind CSS included in your HTML using the recommended method. If you want to learn more about how to use Tailwind CSS you can read our latest Tailwind CSS tutorial where we cover many aspects of the framework.



 # Preview 
[Rohit Portfolio.webm](https://github.com/user-attachments/assets/cab36b2d-a811-4266-9999-9ac8e7dd1711)
