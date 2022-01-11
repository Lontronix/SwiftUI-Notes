
Note: `BindableObject` was renamed to `ObservableObject`

this:
```swift
class User: ObservableObject {
	let objectWillChange = ObservableObjectPublisher()
	var username = "Lontronix" { didSet { didChange.send() } }
	var password = "charly123" { didSet { didChange.send() } }
	var emailaddress = "fake-email@fakedomain.con" { didSet { didChange.send() } }
}
```

can be simplified to this:
```swift
class User: ObservableObject {
	@published var username = "Lontronix" { didSet { didChange.send() } }
	@published var password = "charly123" { didSet { didChange.send() } }
	@published email = "fake-email@fakedomain.com" { didSet { didChange.send() } }
}
```
* SwiftUI can automatically synthesize `objectWillChange`
* `@Published` adds the property observer



Resources: 
- https://www.pointfree.co/blog/posts/30-swiftui-and-state-management-corrections
- https://www.youtube.com/watch?v=stSB04C4iS4

