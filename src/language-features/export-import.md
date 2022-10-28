## export - Exposing to Other Files

From [Exercism.org](https://exercism.org/tracks/javascript/concepts/basics)

To make functions, constants, or variables available in other files, they need to be exported using the `export` keyword. Another file may then import these using the `import` keyword. This is also known as the module system.

A great example is how all the tests work. Each exercise has at least one file, for example `lasagna.js`, which contains the implementation. Additionally, there is at least one other file, for example `lasagna.spec.js`, that contains the tests.

This file imports the public (i.e. exported) entities to test the implementation.

### Using the default export
From [Developer.Mozilla.org](https://developer.mozilla.org/en-US/docs/web/javascript/reference/statements/export#using_the_default_export).

If we want to export a single value or to have a fallback value for your module, you could use a default export:

```
// module "my-module.js"

export default function cube(x) {
  return x * x * x;
}
```
Then, in another script, it is straightforward to import the default export:
```
import cube from './my-module.js';
console.log(cube(3)); // 27
```
