# 2-4 创建 BrowserWindow

|本期版本|上期版本
|:---:|:---:
`Thu Jun 22 00:03:57 CST 2023` | 

```json
{
	// 单引号在一些windows机器上有问题
	// "start": "nodemon --watch main.js --exec ''"
	
	"start": "nodemon --watch main.js --exec \"electron .\""
}
```

```javascript
{
	webPreferences: {
		// 在render里面使用node 
		nodeItegration: true
	}
}
```

## Ref

* <https://github.com/remy/nodemon>