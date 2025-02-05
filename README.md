The `master` branch is a bare Godot 4.3 project with iOS export.
It contains a .github/workflows/build-ios.yml file that will trigger the GitHub Actions to build a iOS .ipa file and it will *successfully build* as shown here:
https://github.com/microlancer/admob-ios-test/actions/runs/13151169418

However, the `with-admob` branch is the same project with the AdMob plugin enabled.
This does not build successfully, as it contains various errors.
