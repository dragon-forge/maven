# Dragon Forge Maven


But hey! How do I add **X** artifact?
Quite simply, add this repository to the build path as following:
```gradle
repositories {
    maven {
        name = "DragonForge"
        url = "https://raw.github.com/dragon-forge/maven/master"
    }
}
```
(needs to be done only once)

And then add the following line to dependencies:
```gradle
dependencies {
	deobfCompile "tk.zeitheron.X:X-MC:MV:deobf"
}
```
(where X might be anything, MC is minecraft version and MV is mod version)

HammerLib example for 1.12.2:
```gradle
repositories {
    maven {
        name = "DragonForge"
        url = "https://raw.github.com/dragon-forge/maven/master"
    }
}

dependencies {
	deobfCompile "tk.zeitheron.HammerLib:HammerLib-1.12.2:2.0.6.14:deobf"
}
```

## WARNING: After you've added the library, YOU MUST run `setupDecompWorkspace` on 1.12.2 or reimport the project in 1.13+ to update the dependency
