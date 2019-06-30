### Automattic
---
https://github.com/Automattic

#### simplenote-ios
https://github.com/Automattic/simplenote-ios

```swift
import Foundation
import AutomatticTracks

enum BuildConfiguration: String {
  case debug
  case `internal`
  case release
  case unknown
  
  static var current: BuildConfiguration {
    
    # if DEBUG
      return .debug
    #elseif BUILD_APP_STORE
      return .appStore
    #elseif BUILD_RELEASE
      return .release
    #else
      
      return .unkonow
    #endif
  }
  
  static func `is`(_ configuration: BuildConfiguration) -> Bool {
    return configuration == current
  }
}

extension BuildConfiguration : CustomStringConvertible {
  var description: String {
    return self.rawValue
  }
}
```

```
```

```
```


