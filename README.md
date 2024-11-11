# BundlerAssetTest

Demo of difference in behaviour of `application` (esbuild) vs `browser` (webpack) builders when handling asset URLs in CSS.

The app contains an image file and a CSS rule in the styles.scss file that uses it as a background image.

The app has two builders configured in angular.json: `build` for the `application` builder, and `build-webpack` for the `browser` builder.

Run `npm run build-webpack` to build with the `browser` builder; build should be successful.
Run `npm run build` to build with the `application` builder; build will fail with an error `Could not resolve "^smile.svg"`. 

Expectation is that the `application` and `browser` builders should be interoperable with the same source code when not using SSR.
