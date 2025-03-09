# Learning Tailwind CSS

Creator of Tailwind CSS: *Adam Wathan*

![](https://i.ytimg.com/vi/1x7HlvSfW6s/maxresdefault.jpg)



## 1. Resources for Tailwind

- [Tailwind Playground](https://play.tailwindcss.com/)

- [Ready to use resources](https://tailblocks.cc/)

- [Youtube video](https://www.youtube.com/watch?v=WvBnTJK7Khk)

- [Let's learn Tailwind](https://rahullkumr.github.io/Tailwind-practice/)

## 2. How to setup Tailwind CLI

1. `npm init -y`

    > used to quickly create a new package.json file for a Node.js project with default settings


   -  `npm init` : This command is used to initialize a new Node.js project by creating a package.json file, which holds information about your project, dependencies, and scripts.

   -  `-y` : This flag automatically answers "yes" to all prompts, accepting default values for the project configuration (name, version, description, etc.).

2. `npm install -D tailwindcss`

   - `npm install` : Installs a package.

   - `-D` : Adds the package as a development dependency. This means it's only required during development and will not be included in the production build.

   - `tailwindcss` : This is the actual package name for Tailwind CSS, a utility-first CSS framework.

3. `npx tailwindcss init` 

    -  used to generate a default configuration file for Tailwind CSS, named tailwind.config.js, in the project. 
    
    - This file allows to customize the default Tailwind settings like theme, colors, fonts, breakpoints, and more.

4. Update tailwind.conf.js file to include following line:

    ```
    content: ["*.html"]
    ```

5. Create src/input.css to include

    ```
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    ```

    ## complete it asap
