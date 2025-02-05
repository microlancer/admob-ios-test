The `master` branch is a bare Godot 4.3 project with iOS export.
It contains a .github/workflows/build-ios.yml file that will trigger the GitHub Actions to build a iOS .ipa file and it will *successfully build* as shown here:
https://github.com/microlancer/admob-ios-test/actions/runs/13151169418

However, the `with-admob` branch is the same project with the AdMob plugin enabled.
This does not build successfully, as it contains various errors.
https://github.com/microlancer/admob-ios-test/actions/runs/13151372574/job/36699305498

The error is:
```
ld: warning: search path '/Users/runner/Library/Developer/Xcode/DerivedData/empty-test-dctfsyiaclxjiwfnhpypboqxrqnj/Build/Intermediates.noindex/ArchiveIntermediates/empty-test/BuildProductsPath/Debug-iphoneos/XCFrameworkIntermediates/Google-Mobile-Ads-SDK' not found
ld: warning: search path '/Users/runner/Library/Developer/Xcode/DerivedData/empty-test-dctfsyiaclxjiwfnhpypboqxrqnj/Build/Intermediates.noindex/ArchiveIntermediates/empty-test/BuildProductsPath/Debug-iphoneos/XCFrameworkIntermediates/GoogleUserMessagingPlatform' not found
ld: framework 'Pods_empty_test' not found
clang: error: linker command failed with exit code 1 (use -v to see invocation)

** ARCHIVE FAILED **


The following build commands failed:
	Ld /Users/runner/Library/Developer/Xcode/DerivedData/empty-test-dctfsyiaclxjiwfnhpypboqxrqnj/Build/Intermediates.noindex/ArchiveIntermediates/empty-test/InstallationBuildProductsLocation/Applications/empty-test.app/empty-test normal (in target 'empty-test' from project 'empty-test')
(1 failure)
Error: Process completed with exit code 65.
```

