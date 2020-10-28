# sqltableconv
usage
```
import (
	"fmt"
	"github.com/huangzhiran/sqltableconv"
)

func main() {
	SQL := "select * from student"

	convFunc := func(s string) string {
		return s + "_change"
	}

	c, err := sqltableconv.Conv(SQL, convFunc)
	if err != nil {
		panic(err)
	}
	fmt.Println(c)
}
```
