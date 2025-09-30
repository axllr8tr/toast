# axllr8tr/toast

An enhanced Go package for toast notifications in Windows 10 (and newer?).  
Based on <https://github.com/go-toast/toast>

## Example

```go
package main

import (
  "github.com/axllr8tr/toast"
  _ "embed"
)

//go:embed "gopher.png"
var gopher []byte // file must exist

func main() {
  notification := toast.Notification{
    IconBytes: gopher, // or `Icon` for standard behavior, or `IconPath` to also copy it to %temp%
    IconCrop: "circle",
    HeroPath: "C:\\Windows\\Web\\Wallpaper\\Windows\\img0.jpg", // can be an absolute or a relative path
    AppID: "Notification test",
    Title: "Hello, world!",
    Message: "I think it's working as expected, and that's cool",
    Attribution: "via toast package",
  }
  notification.Push()
}
```

## Screenshots
<img width="395" height="401" alt="image" src="https://github.com/user-attachments/assets/6f8d92da-fb30-435a-a5bb-e84135ea5f24" />
