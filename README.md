# Noder - project structure manager for Express applications
Have you ever wondered if manually creating files in your Express apps is optimal? Probably not. But you never really cared. 
Now you can start caring because __this tool does it for you__.

## Noder is global now!
You can use noder in your terminal just like any npm package installed globally:
```
$ npm i -g .
$ noder
```

## Project scope with noder init
Each project can have its own noder configuration. Run `noder init` in your project root to generate a `.noder/config.js` file:
```
$ noder init
> [OK] .noder/config.js created.
```
This file lets you customize directory names per project:
```js
module.exports = {
    directoryNames: {
        controller: 'Controllers',
        middleware: 'Middleware',
        model:      'Models',
        route:      'Routes',
        service:    'Services',
        validator:  'Validators',
        config:     'Config',
        migration:  'Migrations',
        seeder:     'Seeders',
    }
};
```
Change any value to fit your project structure. Fields you omit will fall back to the defaults above. If `.noder/config.js` is not present, noder uses the defaults for everything.

## Usage
It's simple really. Take a look:
```
$ node noder command:action arg1
```
## Currently supported commands
```
list                   Show all available commands
init                   Create .noder/config.js in current project
make:controller        Create a new controller file
make:middleware        Create a new middleware file
make:model             Create a new model file
make:route             Create a new route file
make:service           Create a new service file
make:validator         Create a new validator file
make:config            Create a new config file
make:migration         Create a new migration file
make:seeder            Create a new seeder file
```

## Examples
Make controller
```
$ node noder make:controller AuthController
> [OK] src/Controllers/ExampleController.js
```
Make middleware:
```
$ node noder make:middleware AdminGuard
> [OK] src/Middleware/AdminGuard.js
```
