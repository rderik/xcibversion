# XCIncreaseBuildVersion

This script automates the increment of Build numbers in Xcode projects.

The script searches the `Info.plist` in the current path and increases the build version number. 

# Usage

```bash
Usage:
xcibversion [--interactive|-i] [--build=SPECIFIC_BUILD] [--path=PATH] [--dry-run]
```

## Interactive

The interactive mode will prompt for confirmation for each `Info.plist` file it encounters.

## Specify a build number

Using the `--build` argument, you can specify the build number the replace the current build number.

For example:

```bash
$ ./xcibversion --build=15  --path=./myProject/
```


## Define the path to search for `Info.plist` files

If `--path` argument is used the script will search in that path for `Info.plist` files for processing.

## Dry run

When the script is executed with the `--dry-run` flag, the script won't make any changes. A dry run will only display the changes that would be made, it can be used at first to verify if the script will work as you expect.

