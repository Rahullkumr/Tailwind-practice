# Learning Tailwind



## 1. Resources for Tailwind

- [Tailwind Playground](https://play.tailwindcss.com/)

- [Ready to use resources](https://tailblocks.cc/)


## How to setup Tailwind CSS

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

6. Include the src/output.css file to html file by using `<link rel="stylesheet" href="src/output.css">` <br><br>

7. Running the Tailwind CSS Build Command

    Run the following command (this command should continue running in the background)::

    ```
    npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
    ```

    - `npx tailwindcss` : Executes Tailwind CSS via `npx` without installing it globally.

    - `-i` : Specifies the input file (./src/input.css), where you have your Tailwind CSS directives.

    - `-o` : Specifies the output file (./src/output.css), where the compiled CSS will be saved.

    - `--watch` Continuously watches for file changes and recompiles the CSS whenever files are updated, eliminating the need to run the command manually every time you make changes

8. Aliasing the above long command into short form

    - To avoid typing this long command repeatedly, let's create an alias for it in `package.json` file. This allows to run the command using a simple `npm run build`.

    - step 1: Open the package.json file.

    - step 2: Inside the "scripts" section, add the following line:

        ```
        "build": "npx tailwindcss -i ./src/input.css -o ./src/output.css --watch"
        ```
    - step 3: Now, instead of running the full command, simply run:

        ```
        npm run build
        ```
