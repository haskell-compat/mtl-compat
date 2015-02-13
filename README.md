# `mtl-compat` [![Hackage version](https://img.shields.io/hackage/v/mtl-compat.svg?style=flat)](http://hackage.haskell.org/package/mtl-compat) [![Build Status](https://img.shields.io/travis/RyanGlScott/mtl-compat.svg?style=flat)](https://travis-ci.org/RyanGlScott/mtl-compat)

This package backports the `Control.Monad.Except` module from `mtl` (if using `mtl-2.2.0.1` or earlier), which reexports the `ExceptT` monad transformer and the `MonadError` class.

This package should only be used if there is a need to use the `Control.Monad.Except` module specifically. If you just want `mtl` class instances for `ExceptT`, use `transformers-compat` instead, since `mtl-compat` does nothing but reexport the instances from that package.

Note that unlike how `mtl-2.2` or later works, the `Control.Monad.Except` module defined in this package exports all of `ExceptT`'s monad class instances. Therefore, you may have to declare `import Control.Monad.Except ()` at the top of your file to get all of the `ExceptT` instances in scope.
