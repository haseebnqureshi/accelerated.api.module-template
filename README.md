
## Quick Start
This repo is an easy-to-use npm template to create modules for accelerated.api. Start by simply cloning this repo and updating your git remote origin:

1. Clone the template to your directoy with ```git clone https://github.com/haseebnqureshi/accelerated.api.module-template.git ./{YOUR_DIRECTORY}```;

2. Remove the existing project's git origin with ```git remote remove origin```;

3. Add your git origin with ```git remote add origin {YOUR_REPOSITORY_URL}```;

4. And then push the codebase up to your git repo with ```git push -u origin master```.

You're ready for some changes! Then in your new directory and git repo, do the following:

1. Change your ```moduleKey``` and ```moduleName``` in index.js. (```moduleKey``` is a key that uniquely identies your module in the context of your app.)

2. Update your ```package.json``` with your information and module information.

3. Now actually create your module by utilizing the three CommonJS modules in this repo, ```middleware```, ```model```, and ```route```. Please note the structure and direct injected variables in each CommonJS module and what each is returning.

4. Run ```npm publish``` in your command line to publish directly onto npm, and viola! You've got a npm packaged module for accelerated.api.

## Using in accelerated.api
Okay, so how do you use this module in your accelerated.api project? Here's an example:

```

var api = require('accelerated.api');

var example = require('acceleratd.api.module');

api.useMiddlewares([ 
	[example.key, example.middleware]
]);

api.useModels([
	[example.key, example.model]
]);

api.useRoutes([
	[example.key, example.route]
]);

api.run();

```
