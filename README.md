> # WebService

Description:..

***


> Requirements
```bash
# redis
go get github.com/go-redis/redis
# receiver
go get github.com/YuranIgnatenko/WebReceiver
```
***

> Install
```
go get github.com/YuranIgnatenko/WebService

```
***

> Use

```bash 
go run main.go -host=127.0.0.1 -port=6379
#(host, port redis database)
```
***

> Test api 
* All   `/cmd/curl_stress.go` 
* set value in DB `/cmd/test1.go`
* increment value `/cmd/test2.go`

***

> test 1
```js
// example request
{
	"key":"k",
	"value":"1"
}

// returned
{
	"k":"13628"
}
```

> test 2
```js
// example request
{
	"s":"line text",
	"key":"sekret key"
}

// returned
{
	"HMAC-SHA512":"d2f6c4639127932d89a22528f84fd2e287134e19ff46852055ae78eec4c748f7"
}
```


*** 

> test 3
``` js
// example request
	[
	  {
	    "a": "99",
	    "b": "2",
	    "key": "x"
	  },
	  {
	    "a": "11",
	    "b": "2",
	    "key": "y"
	  }
	]

// returned
{
	"x": "188",
	"y": "22"
}
```

> Download Receiver

* [WebReceiver](http://github.com/YuranIgnatenko/WebReceiver)