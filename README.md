# Circle Creative Responsive MikroTik Template / Themes

Free Responsive Mikrotik Template / Themes Based on Bootstrap 4, you can customize the logo, text and etc.
Just plug and play on your MikroTik router.

## Installation

- Open winbox and login to your MikroTik router
- Open the filesystem and upload this theme
- Check your hotspot page

## Local development

To get started working on this project in a local dev environment, follow the below instructions.

Make sure you have the `Live Sass Compiler extension` installed by Glenn Marks to compile your scss to scss. Download it from your IDE.

installed the `Live Server` extension by Ritwick Dey to run a local dev server. it works just like nodemon.

after having the above mentioned extensions installed, you should configure a savePath to compile all the scss files into css.

**NOTE**: This project uses `scss`. Writing your CSS styles directly in the CSS directory is not advisable, as they will be replaced when `scss` is compiled.

## Configuring a savePath or dir

1. Go to settings or press `ctrl + ,` on Mac `Command + ,`
2. Search for `Live Sass Compiler`. Make sure you have it installed
3. under `Live Sass Compile › Settings: Autoprefix` click on the `Edit in settings.json`
4. In the settings.json file find:

```json

"liveSassCompile.settings.formats": [
  {
   "extensionName": ".css",
   "savePath": "/assets/css",
   "savePathReplacementPairs": null
  }
 ],

```

and change the `savePath` to **/assets/css**

**NOTE**: It is preferred to use `/assets/css` specifically for this project. Setting a new savePath will create a duplicate compilation dir.

## Compiling the SCSS files to CSS

- Find the watch sass button at the bottom of the terminal bar and click on it to compile your scss files.

![watch sass](readme.png)

If you cant find watch sass, open your command palette by pressing `ctrl + P` on Mac `Command + P`. and then type `> watch sass`.

Make sure you have the compilation directory specified to this projects required dir or a new location will be used for the compilation of the css files. [How to configure the savePath](#configuring-a-savepath-or-dir)

If in your console, the output is `watching` then it means everything is working fine.

## Running the local dev server

- Find the Go live button at the bottom of the terminal and click on it to run the dev server. Make sure you have `Live Server` extension by Ritwick Dey installed.

If you cant find Go Live at the bottom of the terminal open your command palette by pressing `ctrl + P` on Mac `Command + P`. and then type `> live sass`.

## An overview of how the scss folder is structure

The **theme.scss** imports all of the scss files in the \_partials and \_pages directory and compiles them into the css directory.

inside the **\_pages** directory, each file includes styles for a page. e.g the **\_dashboard.scss** includes the styles for the **dashboard page**. Noticed there is an `_index.scss` file in the root. The **index.scss** `@forwards` all the files in a directory and includes them in the `theme.scss` file so that it compiles them.

## Creating a new stylesheet for a page

To create a new stylesheet for a page, get into the scss directory and inside `_pages` create your file. **e.g demo.scss**

after creating a stylesheet, open the `_index.scss` file located at the root of that directory and `@forward "./demo";`. ignore the extension.

**NB**: Do the above for every stylesheet you add.

## Screenshots

### Mobile Friendly

![alt login](https://github.com/teguhrianto/responsive-mikrotik-template-bootstrap4/raw/master/screenshot/circlecreative-mikrotik-template.png)

### Login

![alt login](https://github.com/teguhrianto/responsive-mikrotik-template-bootstrap4/raw/master/screenshot/desktop.png)

### Status

![alt status](https://github.com/teguhrianto/responsive-mikrotik-template-bootstrap4/raw/master/screenshot/status.png)

## Ideas and Suggestions

Please kindly mail me at [teguh@circle-creative.com](mailto:teguh@circle-creative.com])
