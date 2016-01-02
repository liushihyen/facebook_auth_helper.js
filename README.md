# Login with Facebook Javascript SDK helper v1.0.0

### 相依

* jQuery（只能跪了...）

### 使用方法

#### 初始化

```
facebookAuthModule.loadSDK().initSDK({
	appId : '這裏放你的Facebook app id',
	version : 'v2.5'
});
```

#### 驗證使用者是否授權你的App，如果授權過，便會傳回使用者的資料

```
$('#js-doFbLogin').on('click', '', {}, function(event) {
	event.preventDefault();
	facebookAuthModule.doFbAuth().then(function(user) {
		console.dir(user);
	});
});
``` 