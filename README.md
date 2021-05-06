## To run the application and see the error "chunk runtime-main [entry] Cannot convert undefined or null to object":

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

## To run the application without 'web-vitals' (without 'web-vitals' you won't get any error when building):
1. `git checkout web-vital-uninstalled`
2. `npm install`
3. `npm run build`