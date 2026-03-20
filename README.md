# Noder - project structure manager for Express applications
Have you ever wondered if manually creating files in your Express apps is optimal? Probably not. But you never really cared. 
Now you can start caring because __this tool does it for you__.

## Usage
It's simple really. Take a look:
```
$ node noder command:action arg1
```
## Currently supported commands
We currently support `make` command. You can make `controller` or `middleware`.

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
