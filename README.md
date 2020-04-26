[![Contributors][contributors-shield]][contributors-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/mtaresources/scripts">
    <img src="logo.png" alt="Logo" width="128" height="128">
  </a>

  <h3 align="center">MTA Resources Scripts Repository</h3>

  <p align="center">
    A collection of scripts that you can either use freely or have generated with a simple user interface on our website.
    <br />
    <br />
    <a href="https://github.com/mtaresources/scripts">Visit MTA Resources</a>
    ·
    <a href="https://github.com/mtaresources/scripts/issues">Report an issue</a>
    ·
    <a href="https://github.com/mtaresources/scripts/issues">Request a script</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [Usage](#usage)
* [Contributing](#contributing)
* [Adding a new Script](#adding-a-new-script)
* [Handlebars Helpers](#handlebars-helpers)
  * [HEX to RGB](#hex-to-rgb)
* [License](#license)
* [Credits](#credits)



<!-- USAGE -->
## Usage

The easiest way to use our scripts is to [navigate to our website](http://comingsoon.tm), select a script, enter the required information and have the finished and usable script generated.

For those of you who prefer to do this manually, grab a script template in our repository and enter the values in the template yourself.



<!-- CONTRIBUTING -->
## Contributing

Contributions are what get the MTA community going and allows everyone to benefit from creative and new ideas. No matter if corrections of spelling mistakes, bufgixes, or even new scripts - every contribution is **highly appreciated**.

1. Fork the project
2. Create your branch with the appropriate prefix e.g `script` / `fix`  (`git checkout -b script/skycolor`)
3. Implement your changes (if you're wondering how to contribute a new script, [check these instructions](#adding-a-new-script))
4. Commit your changes (`git commit -m 'Added sky color script'`)
5. Push your new changes (`git push origin script/skycolor`)
6. Open a Pull Request



<!-- ADDING A NEW SCRIPT -->
## Adding a new Script

First of all, thank you for your interest in adding a new script to our collection! Please be aware that when you add a new script, it should be written entirely by you and you agree that anyone can edit, redistribute and use your script, whether commercial or non-commercial. Your script is then published in this repository under the MIT license just like any other script.

Also, please make sure that your script is more or less in line with [LUA best practices](https://www.mediawiki.org/wiki/Help:Lua/Lua_best_practice) so that we have consistent and clean code in our repository. Our goal is to provide small snippets, so avoid larger scripts that need to be split into multiple files, instead make smaller scripts or write your functionality as compact as possible! 

1. Write your script and make sure it works - test it extensively in MTA:SA.
2. Create a new directory in the root of this project with the name of your script. Make sure that you do not use any special characters, spaces or numbers in the name and write it in lowercase.
3. Now we need the following three files:
    - `template.hjs` - Contains your script as a template. We use [HandlebarsJS](https://handlebarsjs.com/) to create semantic templates.
    - `schema.json` - Contains the schema for your template.
    - `uiSchema.json` - Contains the UI schema for your schema.
4. Replace all the values in your script that a user can configure later, with Handlebars variables. You can use all the built-in Helpers that Handlebars provides or our custom ones, [which you can find here](#handlebars-helpers). If you need an own helper, submit your Helper code in the Pull Request description and expand the [Handlebars Helper section](#handlebars-helpers) with a small documentation about your Helper. Save your script-template as `template.hjs`.
5. Create your [JSON Schema](http://json-schema.org/) and save it as `schema.json`. You can check the [skycolor script](skycolor/schema.json) for a simple example. Make sure you also include a title and a description in your schema!
6. Create your UI Schema and save it as `uiSchema.json`. You can check the [skycolor script](skycolor/uiSchema.json) for a simple example.

Pro-tips:
 - Check if your script-template is working correctly [with this online tool](https://tqdev.com/2016-precompile-handlebars-online)
 - [This JSON Schema playground](https://rjsf-team.github.io/react-jsonschema-form/) makes it easier for you to create both, the schema and UI schema. The site also has many examples of how to create such schemes. The formData output is later passed to the handlebars template.



<!-- HANDLEBARS HELPERS -->
## Handlebars Helpers

#### HEX to RGB
- `r` - Returns the red value of the Hex-Color in decimal. e.g: `{{r '#FF0000'}}` returns `255`
- `g` - Returns the green value of the Hex-Color in decimal. e.g: `{{g '#00FF00'}}` returns `255`
- `b` - Returns the blue value of the Hex-Color in decimal. e.g: `{{b '#0000FF'}}` returns `255`



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CREDITS -->
## Credits

- [pkfln](https://github.com/pkfln)






<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/mtaresources/scripts.svg?style=flat-square
[contributors-url]: https://github.com/mtaresources/scripts/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/mtaresources/scripts.svg?style=flat-square
[forks-url]: https://github.com/mtaresources/scripts/network/members
[stars-shield]: https://img.shields.io/github/stars/mtaresources/scripts.svg?style=flat-square
[stars-url]: https://github.com/mtaresources/scripts/stargazers
[issues-shield]: https://img.shields.io/github/issues/mtaresources/scripts.svg?style=flat-square
[issues-url]: https://github.com/mtaresources/scripts/issues
[license-shield]: https://img.shields.io/github/license/mtaresources/scripts.svg?style=flat-square
[license-url]: https://github.com/mtaresources/scripts/blob/master/LICENSE
