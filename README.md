# Angular2 + Wordpress

[![Build Status](https://travis-ci.org/smartbiz/angular2-wordpress.svg?branch=master)](https://travis-ci.org/smartbiz/angular2-wordpress)
[![Build Status](https://ci.appveyor.com/api/projects/status/cbpp0xtht82i6wco/branch/master?svg=true)](https://ci.appveyor.com/project/smartbiz/angular2-wordpress)
[![GPLv3+ License](https://img.shields.io/badge/license-GPLv3+-brightgreen.svg)](http://opensource.org/licenses/MIT)
[![Join the chat at https://gitter.im/smartbiz/angular2-wordpress](https://badges.gitter.im/smartbiz/angular2-wordpress.svg)](https://gitter.im/smartbiz/angular2-wordpress?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

> Build a Mobile App for your WordPress based business using Angular 2.

# Development Environment

1. [Node.js](http://nodejs.org) and npm installed. I recommend using [nvm](https://github.com/creationix/nvm). I used nvm v0.31.0, node v4.4.2 & npm 2.14.7

```
  xcode-select --install
  curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh | bash
  nvm install 4.2.2
```

1. Install ts-node for TypeScript:

```
  npm install -g ts-node
```

1. [Git](http://git-scm.com "Git distributed version control system") installed. I recommend using [SourceTree](https://www.sourcetreeapp.com)
```
  git clone --depth 1 https://github.com/smartbiz/angular2-wordpress.git
```

1. Install the project's dependencies:
```
  cd angular2-wordpress
  # install the project's dependencies
  npm install
  # watches your files and uses livereload by default
  npm start
  # api document for the app
  npm run docs

  # dev build
  npm run build.dev
  # prod build
  npm run build.prod
```

# Main features


# Changelog
## Version 1.0
- Ready to go, statically typed build system using gulp for working with TypeScript.
- Production and development builds.
- Sample unit tests with Jasmine and Karma.
- End-to-end tests with Protractor.
- Development server with Livereload.
- Experimental hot loading support.
- Following the [best practices for your application’s structure](https://github.com/mgechev/angular2-style-guide).
- Manager of your type definitions using [typings](https://github.com/typings/typings).
- Basic Service Worker, which implements "Cache then network strategy".
.
├── src
│   ├── main.ts 
│   ├── app
│   │   └── components
│   │       └── app.component.ts
│   ├── search
│   │   └── *.*
│   ├── shared
│   │   ├── services
│   │   │   └── search.service.ts
│   │   └── data
│   │       └── menu.json

### Directory Structure

```
.
├── LICENSE
├── README.md
├── gulpfile.ts                <- configuration of the gulp tasks
├── karma.conf.js              <- configuration of the test runner
├── package.json               <- dependencies of the project
├── protractor.conf.js         <- e2e tests configuration
├── src                        <- source code of the application
│   ├── home
│   │   └── components
│   ├── index.html
│   ├── main.ts                <= 
│   ├── shared
│   │   └── services
│   │       ├── name-list...
│   │       └── name-list...
│   └── sw.js                  <- sample service worker
├── test-main.js               <- testing configuration
├── tools
│   ├── README.md              <- build documentation
│   ├── config
│   │   ├── project.config.ts  <- configuration of the specific project
│   │   ├── seed.config....
│   │   └── seed.config.ts     <- generic configuration of the seed project
│   ├── config.ts              <- exported configuration (merge both seed.config and project.config, project.config overrides seed.config)
│   ├── debug.ts
│   ├── manual_typings
│   │   ├── project            <- manual ambient typings for the project
│   │   │   └── sample.pac...
│   │   └── seed               <- seed manual ambient typings
│   │       ├── merge-stre..
│   │       └── slash.d.ts
│   ├── tasks                  <- gulp tasks
│   │   ├── project            <- project specific gulp tasks
│   │   │   └── sample.tas...
│   │   └── seed               <- seed generic gulp tasks. They can be overriden by the project specific gulp tasks
│   ├── utils                  <- build utils
│   │   ├── project            <- project specific gulp utils
│   │   │   └── sample_util...
│   │   ├── project.utils.ts
│   │   ├── seed               <- seed specific gulp utils
│   │   │   ├── clean.ts
│   │   │   ├── code_change...
│   │   │   ├── server.ts
│   │   │   ├── tasks_tools.ts
│   │   │   ├── template_loc...
│   │   │   ├── tsproject.ts
│   │   │   └── watch.ts
│   │   └── seed.utils.ts
│   └── utils.ts
├── tsconfig.json              <- configuration of the typescript project (ts-node, which runs the tasks defined in gulpfile.ts)
├── tslint.json                <- tslint configuration
├── typings                    <- typings directory. Contains all the external typing definitions defined with typings
├── typings.json
└── appveyor.yml
```
