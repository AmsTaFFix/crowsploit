# crowsploit
A hack tool for the game greyhack aimed to be the gmod of tools.

# This project is officially discontinued

## Building crowsploit

**Make sure you have the vscode greybel addon installed**

### Prerequisites

- Make sure greybel has `allow import` **TURNED OFF** in the settings
- Set `Greybel › Transpiler › Installer` to true
- Do **NOT** use obfuscation, this will destroy crowsploit

### Building interface

All you need to build the crowsploit interface, is build the `interface/crowsploit` file into the game.

### Building tools

All tools must have toolkernel as an import, and `tool.init()` at the bottom.

Additional tools can be imported into the same tool by just using `import_code(tool_path)` at the end of the file (Make sure to do this AFTER the .init)

All tools, including the base ones, are to be placed into /etc/crow/tools after setup for crowsploit to load them

### Building Devtools

Turn ON the allow import in greybel settings, before building the devtools

***MAKE SURE TO TURN IT RIGHT BACK OFF AFTERWARDS***

# NOTE: This technically still a beta version. And thus, lots of bugs, weird structures and just general inconsistencies are expected.

## interface/crowsploit
```shell
greybel build ./interface/crowsploit.src ./build/interface -id "/bin" -i -ac -ci -pt 7777
```

## interface/test
```shell
greybel build ./src/interface/test.src ./build/interface/test -id "/bin" -i -ac -ci -pt 7777
```

## tool/system
```shell
greybel build ./tools/system.src ./build/tool/system -id "/etc/crow/tools" -i -ac -ci -pt 7777
```

## tool/crack
```shell
greybel build ./src/tool/crack.src ./build/tool/crack -id "/etc/crow/tools" -i -ac -ci -pt 7777
```

## tool/exploit
```shell
greybel build ./src/tool/exploit.src ./build/tool/exploit -id "/etc/crow/tools" -i -ac -ci -pt 7777
```
