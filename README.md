# simple kotlin

trying to get autocomplete and command line compiler for kotlin and kotlin native

## requirement

- brew
- java 17

## installing

For mac:

```bash
brew install kotlin kotlin-native
```

## working with the compiler

enter the sample code folder and use the desired compiler:

```bash
cd 00-hello-world
kotlinc Hello.kt -include-runtime -d Hello.jar # for jvm 
kotlinc-native Hello.kt -o Hello # for native executable
```

## known issues

```bash
exception: java.lang.UnsatisfiedLinkError: Library /opt/homebrew/Caskroom/kotlin-native/1.9.10/kotlin-native-macos-aarch64-1.9.10/konan/nativelib/libcallbacks.dylib can't be loaded.
        This can happen because library file is marked as untrusted (e.g because it was downloaded from browser).
        You can trust libraries in distribution by running
                xattr -d com.apple.quarantine '/opt/homebrew/Caskroom/kotlin-native/1.9.10/kotlin-native-macos-aarch64-1.9.10/konan/nativelib'/*
        command in terminal
```

## further reading

- <https://kotlinlang.org/docs/native-command-line-compiler.html#obtain-the-compiler>
- <https://kotlinlang.org/docs/command-line.html#create-and-run-an-application>
