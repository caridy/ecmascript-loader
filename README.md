##  ES7 spec proposal for `Reflect.Loader` and `Reflect.Module`

__NOTE: This spec is a copy of the corresponding section from https://github.com/whatwg/loader as part of the uplifting process for anything under `Reflect`.__

This proposal was drafted by [@dherman](https://github.com/dherman), [@allenwb](https://github.com/allenwb), [@wycats](https://github.com/wycats) and [@caridy](https://github.com/caridy).

_note: after gathering input from [@erights](https://github.com/erights) we have decided to move `Loader` and `Module` classes under `Reflect`._

### Rationale

`Reflect` does not provide any ability to cause I/O. If transitively frozen, it provides no access to mutable state, and so can be shared among subgraphs in the same realm that should not be able to communicate.

`Reflect.Loader` and `Reflect.Module` are classes for making loaders and modules. A class (or any kind of factory) that, given functions for all four traps, makes a fresh loaders or modules, would not itself provide any authority. If `Loader` constructor and `Module` constructor are authority-free, they can be under `Reflect`.

### Details

 * https://github.com/whatwg/loader/issues/34#issuecomment-126768933
 * https://github.com/whatwg/loader/issues/76

### Render Spec

To render the spec, follow these steps:

```bash
git clone https://github.com/caridy/ecmascript-loader.git
cd ecmascript-loader
npm install
npm run build
open index.html
```
