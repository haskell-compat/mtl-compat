### 0.2.1.3
* A specific build with no flags explicitly enabled, intended for use with the latest version of `mtl`. This is a workaround for `cabal` backtracker bugs.

### 0.2.1.2
* A specific build with the `-ftwo-point-two` flag explicitly enabled. This is a workaround for `cabal` backtracker bugs.

### 0.2.1.1
* A specific build with the `-ftwo-point-one` flag explicitly enabled. This is a workaround for `cabal` backtracker bugs.

## 0.2.1
* Require use of `transformers-compat-0.4` or greater when building with `mtl-2.1.3.1` or earlier. `transformers-compat-0.4.0.*` adds the missing `ExceptT` instances, which means that `mtl-compat`'s only purpose is to backport the `Control.Monad.Except` module for those who want an `mtl`-style import for `ExceptT` and/or `MonadError`.
  
  I would recommend just using `Control.Monad.Trans.Except` from `transformers-compat-0.4.0.*` and `Control.Monad.Error.Class` instead, since they accomplish the same thing as `mtl-compat` without an extra dependency.

## 0.1.1
* Allowed the `two-point-one` flag to toggle on/off automatically

# 0.1
* Initial commit
