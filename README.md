# trap

```
var data []byte
s = bufio.NewScanner(reader)
for s.Scan {
  b := v.Bytes() // 内部实现是 s.token
  data = append(data, b)
}
// 数据量超过一定值,比如100时 data 的数据是重复的
// 因为data 是切片,切片保存的是指针, 而 s.token 在 s.Scan() 的过程中已经被修改了
```
