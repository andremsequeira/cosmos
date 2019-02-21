# Cosmos
A responsive, utility-first SASS framework that expands according to your needs.
Cosmos contains all the handlers and utilities needed to give you a huge head start implementing your project, even though it being different from other known frameworks in that it is **NOT a UI Kit**(!).

&nbsp;

---
## Getting Started
These instructions will make you understand the folders structure as well as the prerequisites for a good and uniformed coding.

&nbsp;

### Installing
A step by step series of examples that tell you how to get sass up and running

&nbsp;

* **Install SASS**

Install Anywhere (npm)
```
npm install -g sass
```

Install on Windows (Chocolatey)
```
choco install sass
```

Install on Mac OS X (Homebrew)
```
brew install sass/sass/sass
```

&nbsp;

* **Compiling CSS**

From the project root, run
```
sass --watch scss/:css/
```

A folder CSS will be created on the project root for all the compiled styles.
(If you want to send this files somewhere else, change the path on the command accordingly).

&nbsp;

---
## Folder structure
The structure is divided in three major folders.


`/base` - Contains all the core files like mixins and modifiers. These files are not supposed to be touched as they are already built and dynamic.

`/config` - Contains all the values and vars files. Will populate all the base files

`/theme` - Contains all Sass files for the project theme

&nbsp;

---
## **Using Cosmos**
Cosmos is a collection of CSS classes. It doesn't have a default theme and there are no UI components created.
It's syntax is simple to understand and memorize (as it uses really descriptive classes). It may seem unecessary but it's going to help on the long run.

&nbsp;

## Prerequisites
Getting to know BEVM naming convention (with a small fix).
Instead of double underscore (__) or double dash (--), use only one of both... Some browsers fail to render styles with this variations

```
block_element-variation -modifier
```

&nbsp;

---
<!-- base folder -->
## **Layout**
In the **`base folder`** is where you'll find all the utlity classes that build the core of Cosmos. All the mixins, functions and modifiers that, by themselves, don't impose design decisions and are abstract to all the UI your project has.

&nbsp;

### **Modularity**
At the moment, Cosmos imports all the files into one single file. This means you have everything available.
On the flip side, this means you have a lot of code you don't necessarily use.
In the near future, the behaviour is to be changed. Separate everything, so that you can import what you need individually.

&nbsp;

### **Responsiveness**
Cosmos is mobile-first by default. This means everything will be stacked to improve reading in your mobile device.
Unless you append the responsive helper classes. Cosmos has 4 breakpoints that are used in functions you can use to build responsive designs.

&nbsp;

### **Mixins**
To prevent overhead selectors, we use Mixins from Sass, which hook into predefined selectors from the UIkit source and inject additional properties. Selectors don't have to be repeated throughout all documents and global changes can be made much more easily.

&nbsp;

### **Modifiers**
There's a bunch of modifiers by default that you can use by appending the **modifier classes**.
These clases all start with ```-is-``` or ```-has-```.

&nbsp;

---
## Variables
In the **`config folder`** you define every generic variable that will be used white constructing your project.
This way you don't need to edit all the base files as they will be populated with these vars.
Since Cosmos is based on Atomic Design, then all the elements should have specific variables inside their SCSS files, preventing unwanted overrides of already declared generic variables that may affect the entire project.

&nbsp;

---
## Customize
Cosmos has a **`theme folder`** in which you should create all the custom styles for the project you're working in right now.
By default it should be empty, as each project is unique.

&nbsp;

### Syntax
The syntax used in Cosmos follows a structure based on [Atomic Design](http://bradfrost.com/blog/post/atomic-web-design/).
All the HTML created should follow the naming convention created to mantain an organized and user-friendly environment.
To apply the convention you only need to append the different classes.

&nbsp;

**Elements - `.el_example`**

&nbsp;
Elements are the basic building blocks of the cosmos. They are HTML tags like label, input or button.
```
<label class="el_label"></label>
<input type="text" class="el_input">
<button class="el_button"></button>
```

&nbsp;

**Components - `.co_example`**

&nbsp;
Components are groups of elements bonded together. Components take on their own properties and serve as the backbone of our design systems.
```
<div class="co_input">
    <label class="el_label"></label>
    <input type="text" class="el_input">
    <button class="el_button"></button>
</div>
```

&nbsp;

**Modules - `.mo_example`**

&nbsp;
Components give us some building blocks to work with, and we can now combine them together to form Modules. Modules are groups of components joined together to form a relatively complex, distinct section of an interface.
```
<div class="mo_login">

    <div class="co_input">
        <label class="el_label"></label>
        <input type="text" class="el_input">
        <button class="el_button"></button>
    </div>
    <div class="co_input">
        <label class="el_label"></label>
        <input type="text" class="el_input">
        <button class="el_button"></button>
    </div>
    <button class="el_button -submit"></button>

</div>
```

&nbsp;

**Layout - `.la_example`**

&nbsp;
Layout are reusable patterns to display modules. Layouts consist mostly of groups of modules stitched together to form pages.
```
<div class="la_overlay">
    <div class="mo_login">

        <div class="co_input">
            <label class="el_label"></label>
            <input type="text" class="el_input">
            <button class="el_button"></button>
        </div>
        <div class="co_input">
            <label class="el_label"></label>
            <input type="text" class="el_input">
            <button class="el_button"></button>
        </div>
        <button class="el_button -submit"></button>

    </div>
</div>
```

&nbsp;

**Pages - `.pa_example`**

&nbsp;
Fixed pages that adopt layouts. These specific instances are the highest level of fidelity.
```
<div class="pa_login">
    <div class="la_overlay">
        <div class="mo_login">

            <div class="co_input">
                <label class="el_label"></label>
                <input type="text" class="el_input">
                <button class="el_button"></button>
            </div>
            <div class="co_input">
                <label class="el_label"></label>
                <input type="text" class="el_input">
                <button class="el_button"></button>
            </div>
            <button class="el_button -submit"></button>

        </div>
    </div>
</div>
```

<!-- &nbsp; -->

<!-- --- -->
<!-- ## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us. -->

&nbsp;

---
## Authors

* **André Sequeira** - [andresequeira__](https://github.com/andresequeira__)
* **António Ferreira** - [isaydesign](https://github.com/isaydesign)
* **Luís Soares** - [luisjs](https://github.com/luisjs)

&nbsp;

---
## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
