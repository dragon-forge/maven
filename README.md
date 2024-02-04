# Dragon Forge Maven


But hey! How do I add **X** artifact?
Quite simply, add this repository to the build path as following:
```gradle
repositories {
    maven {
        name = "Zeith Maven"
        url = "https://maven.zeith.org"
    }
}
```
(needs to be done only once)

And then add the following line to dependencies:
```gradle
dependencies {
	deobfCompile "org.zeith.X:X-MC:MV:deobf"
}
```
(where X might be anything, MC is minecraft version and MV is mod version)

HammerLib example for 1.12.2:
```gradle
repositories {
    maven {
        name = "Zeith Maven"
        url = "https://maven.zeith.org"
    }
}

dependencies {
	deobfCompile "org.zeith.HammerLib:HammerLib-1.12.2:12.2.47"
}
```

## WARNING: After you've added the library, YOU MUST run `setupDecompWorkspace` on 1.12.2 or reimport the project in 1.13+ to update the dependency
