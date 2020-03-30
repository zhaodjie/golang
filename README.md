# Golang code

####这个仓库是平日里上传一些随手写的GOLANG的代码

---
```go
package main

import (
	"fmt"
	"io/ioutil"
	"net/http"
)

func main() {
	resp, err := http.Get("https://zhuanlan.zhihu.com/p/55039990")
	if err != nil {
		fmt.Println("http Get error!", err)
		return
	}
	body, err := ioutil.ReadAll(resp.Body)
	if err != nil {
		fmt.Println("Read body error!", err)
		return
	}
	fmt.Println(string(body))
}
```

