# prepublish-bug

The issue is that the files generated by `prepublishOnly` script (it works with `prepublish` though) are not published during `npm publish`.

Steps to reproduce:

- clone the project
- execute `npm publish` in the project directory
- do `npm i prepublish-bug` in some other directory
- check the `node_modules/prepublish-bug` folder: 

__Expected__: lib/index.js file is there
__Actual__: lib folder is missing

_Note_: please unpublish the module after test, so that other people can publish that again
