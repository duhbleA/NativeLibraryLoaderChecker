# NativeLibraryLoaderChecker
A custom gradle task that takes a native library and determines if it can be loaded successfully

### Example
```
import me.duhblea.nativelibraryloaderchecker.NativeLibraryLoaderChecker
task validateDeployedTenaLibraries(type: NativeLibraryLoaderChecker) {

    // Throw an exception if a DLL is missing, or log an error instead
    shouldThrowException = true

    // Add additional search paths for native libraries and their dependencies
    additionalSearchPaths.add("some-path-to-library".toString())
    
    // Libraries to search for, without pathing or file suffix
    librariesToCheck.add("some-library-name-v1.0")
}
```