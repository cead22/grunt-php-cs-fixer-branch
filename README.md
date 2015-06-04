# grunt-php-cs-fixer-branch

> Grunt plugin for running [PHP Coding Standards Fixer](https://github.com/fabpot/PHP-CS-Fixer) just in 
the modified files of the current git branch

> Heavily inspired/copied from https://github.com/mgmcintyre/grunt-php-cs-fixer

## Installation

1. Install grunt-php-cs-fixer-branch
```
npm install grunt-php-cs-fixer-branch --save-dev
```

2. [Install PHP Coding Standards Fixer](https://github.com/fabpot/PHP-CS-Fixer)

3. Include the task in your Gruntfile with a line like this
```
grunt.loadNpmTasks('grunt-php-cs-fixer-branch');
```

## Usage Example

_To be included in your Grunt `initConfig`._

```js
phpcsfixer: {
	app: {},
	options: {
		bin: 'vendor/bin/php-cs-fixer',
		ignoreExitCode: true,
		level: 'all',
		quiet: true
	}
}
```

__This task is a [multi task][] so any targets, files and options should be specified accordingly.__

[multi task]: http://gruntjs.com/creating-tasks#multi-tasks

## Target Properties

###Options

#### bin
Type: `String`  Default: `'php-cs-fixer'`

_The path to `php-cs-fixer`._  
_(For composer, use `vendor/bin/php-cs-fixer`)._

#### ignoreExitCode
Type: `Boolean` Default: `false`

_Don't fail even if we get a non-zero return._

#### verbose
Type: `Boolean` Default: `false`

_Output full info including warnings and a list of changes._

#### diff
Type: `Boolean` Default: `false`

_Show a diff for the proposed changes._

#### dryRun
Type: `Boolean` Default: `false`

_Don't effect the proposed changes (useful when combined with `--verbose` and `--diff`)._

#### level
Type: `String` Default: `all`

_Chooses preset list of fixers, options are `psr0`, `psr1`, `psr2`, `all`._

#### fixers
Type: `String|Array` Default: `null`

#### framework
Type: `String` Default: `default`

_Chooses option customizes the files to analyse, based on some well-known frameworks directory structures, options are `magento`, `sf20`, `sf21`._

_Comma-separated string, or array of fixers to use._  
_@see [https://github.com/fabpot/PHP-CS-Fixer](https://github.com/fabpot/PHP-CS-Fixer)._

#### branch
Type: `String` Default: `master`

_The git branch to compare against_


#### ignored
Type: `String` Default: `null`

_Pattern to ignore files_
