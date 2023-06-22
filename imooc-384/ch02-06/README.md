# 2-6 使用 IPC 进行通信

|本期版本|上期版本
|:---:|:---:
`Thu Jun 22 11:42:29 CST 2023` | 

```javascript
const { ipcRenderer } = require('electron');

// 发送
ipcRenderer.send('message', 'hello from render')

// 接收
ipcRenderer.on('reply', (event, arg)=>{})
```


```javascript
const { ipcMain } = require('electron')

// 接收
ipcMain.on('message', (event, arg) => {
    console.log(arg)
    
    // 回复
    event.reply('reply', 'hello from main')
})
```


## Ref

* [electron12起，如何解决require is not defined的问题？](https://newsn.net/say/electron-require-is-not-defined-2.html)
* [3. Enable Context Isolation](https://www.electronjs.org/docs/latest/tutorial/security#3-enable-context-isolation)