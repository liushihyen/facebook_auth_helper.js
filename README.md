# Login with Facebook Javascript SDK helper v1.0.0

### 相依

* jQuery（只能跪了...）

### 使用方法

初始化

```
facebookAuthModule.loadSDK({
		locale : 'en_US'
	}).initSDK({
		appId : '686219444844546',
		version : 'v2.5'
	});
```

驗證使用者是否授權你的App，如果授權過，便會傳回使用者的資料

```
$('#js-doFbLogin').on('click', '', {}, function(event) {
	event.preventDefault();
	facebookAuthModule.doFbAuth({
		scope : ['public_profile', 'email']
	}).then(function(util, response) {
		var userDf = util.getUser(['id', 'email', 'cover', 'devices']);
		userDf.then(function(response) {
			console.dir(response);
		});
	});
});
``` 