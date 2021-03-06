# XCIncreaseBuildVersion

This script automates the increment of Build numbers in Xcode projects.

The script searches the `Info.plist` in the current path and increases the build version number. 

If you want to read a more detailed explanation, you can check the article here:

[https://rderik.com/blog/automating-build-and-testflight-upload-for-simple-ios-apps/](https://rderik.com/blog/automating-build-and-testflight-upload-for-simple-ios-apps/)

# Usage

```bash
Usage:
xcibversion --path=PATH [--interactive|-i] [--build=SPECIFIC_BUILD] [--dry-run]
```

## Interactive

The interactive mode will prompt for confirmation for each `Info.plist` file it encounters.

## Specify a build number

Using the `--build` argument, you can specify the build number the replace the current build number.

For example:

```bash
$ ./xcibversion --path=./myProject/ --build=15
```


## Define the path to search for `Info.plist` files

The `--path` argument is mandatory. The script will search in that path for `Info.plist` files for processing.

## Dry run

When the script is executed with the `--dry-run` flag, the script won't make any changes. A dry run will only display the changes that would be made, it can be used at first to verify if the script will work as you expect.

