## To build the application and see the error "chunk runtime-main [entry] Cannot convert undefined or null to object":

1. `npm install`
2. `npm run build`
3. you should see something like the following:
```
% npm run build                   

> myapp@0.1.0 build /Users/mohammad.hunan/Desktop/web-vitals-bug/myapp
> craco build

Creating an optimized production build...
Failed to compile.

chunk runtime-main [entry]
Cannot convert undefined or null to object


npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! myapp@0.1.0 build: `craco build`
npm ERR! Exit status 1
npm ERR! 
npm ERR! Failed at the myapp@0.1.0 build script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/mohammad.hunan/.npm/_logs/2021-05-06T00_36_37_297Z-debug.log
```

## To build the application without 'web-vitals' (without 'web-vitals' you won't get any error when building):
1. `git checkout web-vital-uninstalled` # web-vital-uninstalled, not web-vitals-uninstalled with an s
2. `rm -rf node_modules` # to delete your existing node_modules from the master branch (which includes 'web-vitals')
3. `npm uninstall web-vitals`
4. `npm run build`
5. you should see something like the following: 
```
% npm run build

> myapp@0.1.0 build /Users/mohammad.hunan/Desktop/web-vitals-bug/myapp
> craco build

Creating an optimized production build...
Compiled successfully.

File sizes after gzip:

  770 B  build/static/js/runtime-main.a1094267.js
  574 B  build/static/css/main.9d5b29c0.chunk.css
  514 B  build/static/js/main.6e17e97a.chunk.js

The project was built assuming it is hosted at ./.
You can control this with the homepage field in your package.json.

The build folder is ready to be deployed.

Find out more about deployment here:

  https://cra.link/deployment
```
6. To run the application: `npm start`
