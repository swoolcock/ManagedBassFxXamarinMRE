# ManagedBassFx Xamarin iOS Test

Minimal reproducible example of ManagedBass.Fx ignoring `app.config` on Xamarin.iOS.

This solution should compile and run fine since the config has been renamed to `ManagedBass.Fx.dll.config`.
However, one would expect it to read the dllmap from `app.config` instead.  Note that ManagedBass itself does not need a dllmap entry.

Failing case can be tested by renaming `ManagedBass.Fx.dll.config` to `app.config`, in which case the deployed app will immediately crash on run (tested on 3rd generation 12.9" iPad Pro).
