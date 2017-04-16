# api documentation for  [wechat (v2.1.0)](https://github.com/node-webot/wechat#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-wechat.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-wechat) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-wechat.svg)](https://travis-ci.org/npmdoc/node-npmdoc-wechat)
#### 微信公共平台Node库

[![NPM](https://nodei.co/npm/wechat.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/wechat)

[![apidoc](https://npmdoc.github.io/node-npmdoc-wechat/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-wechat/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-wechat/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-wechat/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jackson Tian"
    },
    "bugs": {
        "url": "https://github.com/node-webot/wechat/issues"
    },
    "dependencies": {
        "ejs": ">=1.0.0",
        "wechat-crypto": "0.0.2",
        "xml2js": "0.4.17"
    },
    "description": "微信公共平台Node库",
    "devDependencies": {
        "connect": "2.5.*",
        "coveralls": "*",
        "expect.js": "*",
        "istanbul": "*",
        "mocha": "*",
        "mocha-lcov-reporter": "*",
        "muk": "*",
        "rewire": "*",
        "should": "~3.0.0",
        "supertest": "*",
        "travis-cov": "*"
    },
    "directories": {
        "test": "test"
    },
    "dist": {
        "shasum": "463cfdb9ee9fd528fb3f03e85a194b5834147eec",
        "tarball": "https://registry.npmjs.org/wechat/-/wechat-2.1.0.tgz"
    },
    "files": [
        "lib",
        "index.js"
    ],
    "gitHead": "6ad9339b7fd690a35cc3ad21f0f294ff3a407806",
    "homepage": "https://github.com/node-webot/wechat#readme",
    "keywords": [
        "weixin",
        "wechat"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "jacksontian"
        }
    ],
    "name": "wechat",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/node-webot/wechat.git"
    },
    "scripts": {
        "test": "make test-all"
    },
    "version": "2.1.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module wechat](#apidoc.module.wechat)
1.  [function <span class="apidocSignatureSpan"></span>wechat (token, handle)](#apidoc.element.wechat.wechat)
1.  [function <span class="apidocSignatureSpan">wechat.</span>Event ()](#apidoc.element.wechat.Event)
1.  [function <span class="apidocSignatureSpan">wechat.</span>List ()](#apidoc.element.wechat.List)
1.  [function <span class="apidocSignatureSpan">wechat.</span>checkSignature (query, token)](#apidoc.element.wechat.checkSignature)
1.  [function <span class="apidocSignatureSpan">wechat.</span>event (fn)](#apidoc.element.wechat.event)
1.  [function <span class="apidocSignatureSpan">wechat.</span>image (fn)](#apidoc.element.wechat.image)
1.  [function <span class="apidocSignatureSpan">wechat.</span>link (fn)](#apidoc.element.wechat.link)
1.  [function <span class="apidocSignatureSpan">wechat.</span>location (fn)](#apidoc.element.wechat.location)
1.  [function <span class="apidocSignatureSpan">wechat.</span>reply (content, fromUsername, toUsername, message)](#apidoc.element.wechat.reply)
1.  [function <span class="apidocSignatureSpan">wechat.</span>reply2CustomerService (fromUsername, toUsername, kfAccount)](#apidoc.element.wechat.reply2CustomerService)
1.  [function <span class="apidocSignatureSpan">wechat.</span>session (id, req, data)](#apidoc.element.wechat.session)
1.  [function <span class="apidocSignatureSpan">wechat.</span>shortvideo (fn)](#apidoc.element.wechat.shortvideo)
1.  [function <span class="apidocSignatureSpan">wechat.</span>text (fn)](#apidoc.element.wechat.text)
1.  [function <span class="apidocSignatureSpan">wechat.</span>toString ()](#apidoc.element.wechat.toString)
1.  [function <span class="apidocSignatureSpan">wechat.</span>toXML (data)](#apidoc.element.wechat.toXML)
1.  [function <span class="apidocSignatureSpan">wechat.</span>video (fn)](#apidoc.element.wechat.video)
1.  [function <span class="apidocSignatureSpan">wechat.</span>voice (fn)](#apidoc.element.wechat.voice)
1.  object <span class="apidocSignatureSpan">wechat.</span>Event.prototype
1.  object <span class="apidocSignatureSpan">wechat.</span>List.prototype
1.  object <span class="apidocSignatureSpan">wechat.</span>session.prototype

#### [module wechat.Event](#apidoc.module.wechat.Event)
1.  [function <span class="apidocSignatureSpan">wechat.</span>Event ()](#apidoc.element.wechat.Event.Event)
1.  [function <span class="apidocSignatureSpan">wechat.Event.</span>dispatch (event)](#apidoc.element.wechat.Event.dispatch)

#### [module wechat.Event.prototype](#apidoc.module.wechat.Event.prototype)
1.  [function <span class="apidocSignatureSpan">wechat.Event.prototype.</span>_dispatch (message, req, res, next)](#apidoc.element.wechat.Event.prototype._dispatch)
1.  [function <span class="apidocSignatureSpan">wechat.Event.prototype.</span>add (event, callback)](#apidoc.element.wechat.Event.prototype.add)

#### [module wechat.List](#apidoc.module.wechat.List)
1.  [function <span class="apidocSignatureSpan">wechat.</span>List ()](#apidoc.element.wechat.List.List)
1.  [function <span class="apidocSignatureSpan">wechat.List.</span>add (name, items, head, delimiter, foot)](#apidoc.element.wechat.List.add)
1.  [function <span class="apidocSignatureSpan">wechat.List.</span>clear ()](#apidoc.element.wechat.List.clear)
1.  [function <span class="apidocSignatureSpan">wechat.List.</span>get (name)](#apidoc.element.wechat.List.get)

#### [module wechat.List.prototype](#apidoc.module.wechat.List.prototype)
1.  [function <span class="apidocSignatureSpan">wechat.List.prototype.</span>get (key)](#apidoc.element.wechat.List.prototype.get)

#### [module wechat.session](#apidoc.module.wechat.session)
1.  [function <span class="apidocSignatureSpan">wechat.</span>session (id, req, data)](#apidoc.element.wechat.session.session)

#### [module wechat.session.prototype](#apidoc.module.wechat.session.prototype)
1.  [function <span class="apidocSignatureSpan">wechat.session.prototype.</span>destroy (callback)](#apidoc.element.wechat.session.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">wechat.session.prototype.</span>save (callback)](#apidoc.element.wechat.session.prototype.save)



# <a name="apidoc.module.wechat"></a>[module wechat](#apidoc.module.wechat)

#### <a name="apidoc.element.wechat.wechat"></a>[function <span class="apidocSignatureSpan"></span>wechat (token, handle)](#apidoc.element.wechat.wechat)
- description and source-code
```javascript
wechat = function (token, handle) {
  if (arguments.length === 1) {
    return new Handler(token);
  }

  if (handle instanceof Handler) {
    handle.setToken(token);
    return handle.middlewarify();
  } else {
    return new Handler(token, handle).middlewarify();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.wechat.Event"></a>[function <span class="apidocSignatureSpan">wechat.</span>Event ()](#apidoc.element.wechat.Event)
- description and source-code
```javascript
Event = function () {
  this.events = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.wechat.List"></a>[function <span class="apidocSignatureSpan">wechat.</span>List ()](#apidoc.element.wechat.List)
- description and source-code
```javascript
List = function () {
  this.map = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.wechat.checkSignature"></a>[function <span class="apidocSignatureSpan">wechat.</span>checkSignature (query, token)](#apidoc.element.wechat.checkSignature)
- description and source-code
```javascript
checkSignature = function (query, token) {
  var signature = query.signature;
  var timestamp = query.timestamp;
  var nonce = query.nonce;

  var shasum = crypto.createHash('sha1');
  var arr = [token, timestamp, nonce].sort();
  shasum.update(arr.join(''));

  return shasum.digest('hex') === signature;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.wechat.event"></a>[function <span class="apidocSignatureSpan">wechat.</span>event (fn)](#apidoc.element.wechat.event)
- description and source-code
```javascript
event = function (fn) {
  return (new Handler())[method](fn);
}
```
- example usage
```shell
...
// FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
// CreateTime: '1359125022',
// MsgType: 'link',
// Title: '公众平台官网链接',
// Description: '公众平台官网链接',
// Url: 'http://1024.com/',
// MsgId: '5837397520665436492' }
}).event(function (message, req, res, next) {
// message为事件内容
// { ToUserName: 'gh_d3e07d51b513',
// FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
// CreateTime: '1359125022',
// MsgType: 'event',
// Event: 'LOCATION',
// Latitude: '23.137466',
...
```

#### <a name="apidoc.element.wechat.image"></a>[function <span class="apidocSignatureSpan">wechat.</span>image (fn)](#apidoc.element.wechat.image)
- description and source-code
```javascript
image = function (fn) {
  return (new Handler())[method](fn);
}
```
- example usage
```shell
...
// message为文本内容
// { ToUserName: 'gh_d3e07d51b513',
// FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
// CreateTime: '1359125035',
// MsgType: 'text',
// Content: 'http',
// MsgId: '5837397576500011341' }
}).image(function (message, req, res, next) {
// message为图片内容
// { ToUserName: 'gh_d3e07d51b513',
// FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
// CreateTime: '1359124971',
// MsgType: 'image',
// PicUrl: 'http://mmsns.qpic.cn/mmsns/bfc815ygvIWcaaZlEXJV7NzhmA3Y2fc4eBOxLjpPI60Q1Q6ibYicwg/0',
// MediaId: 'media_id',
...
```

#### <a name="apidoc.element.wechat.link"></a>[function <span class="apidocSignatureSpan">wechat.</span>link (fn)](#apidoc.element.wechat.link)
- description and source-code
```javascript
link = function (fn) {
  return (new Handler())[method](fn);
}
```
- example usage
```shell
...
// CreateTime: '1359125311',
// MsgType: 'location',
// Location_X: '30.283950',
// Location_Y: '120.063139',
// Scale: '15',
// Label: {},
// MsgId: '5837398761910985062' }
}).link(function (message, req, res, next) {
// message为链接内容
// { ToUserName: 'gh_d3e07d51b513',
// FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
// CreateTime: '1359125022',
// MsgType: 'link',
// Title: '公众平台官网链接',
// Description: '公众平台官网链接',
...
```

#### <a name="apidoc.element.wechat.location"></a>[function <span class="apidocSignatureSpan">wechat.</span>location (fn)](#apidoc.element.wechat.location)
- description and source-code
```javascript
location = function (fn) {
  return (new Handler())[method](fn);
}
```
- example usage
```shell
...
// { ToUserName: 'gh_d3e07d51b513',
// FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
// CreateTime: '1359125022',
// MsgType: 'shortvideo',
// MediaId: 'OMYnpghh8fRfzHL8obuboDN9rmLig4s0xdpoNT6a5BoFZWufbE6srbCKc_bxduzS',
// ThumbMediaId: 'media_id',
// MsgId: '5837397520665436492' }
}).location(function (message, req, res, next) {
// message为位置内容
// { ToUserName: 'gh_d3e07d51b513',
// FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
// CreateTime: '1359125311',
// MsgType: 'location',
// Location_X: '30.283950',
// Location_Y: '120.063139',
...
```

#### <a name="apidoc.element.wechat.reply"></a>[function <span class="apidocSignatureSpan">wechat.</span>reply (content, fromUsername, toUsername, message)](#apidoc.element.wechat.reply)
- description and source-code
```javascript
reply = function (content, fromUsername, toUsername, message) {
  var info = {};
  var type = 'text';
  info.content = content || '';
  info.createTime = new Date().getTime();
  if (message && (message.MsgType === 'device_text' || message.MsgType === 'device_event')) {
    info.DeviceType = message.DeviceType;
    info.DeviceID = message.DeviceID;
    info.SessionID = isNaN(message.SessionID) ? 0 : message.SessionID;
    info.createTime = Math.floor(info.createTime / 1000);
    if (message['Event'] === 'subscribe_status' || message['Event'] === 'unsubscribe_status') {
      delete info.content;
      info.DeviceStatus = isNaN(content) ? 0 : content;
    } else {
      if (!(content instanceof Buffer)) {
        content = String(content);
      }
      info.content = new Buffer(content).toString('base64');
    }
    type = message.MsgType;
    if (message.MsgType === 'device_event') {
      info['Event'] = message['Event'];
    }
  } else if (Array.isArray(content)) {
    type = 'news';
  } else if (typeof content === 'object') {
    if (content.hasOwnProperty('type')) {
      type = content.type;
      if (content.content) {
        info.content = content.content;
      }
      if (content.HardWare) {
        info.HardWare = content.HardWare;
      }
    } else {
      type = 'music';
    }
  }
  info.msgType = type;
  info.toUsername = toUsername;
  info.fromUsername = fromUsername;
  return compiled(info);
}
```
- example usage
```shell
...

app.use(express.query());
app.use('/wechat', wechat(config, function (req, res, next) {
// 微信输入信息都在req.weixin上
var message = req.weixin;
if (message.FromUserName === 'diaosi') {
  // 回复屌丝(普通回复)
  res.reply('hehe');
} else if (message.FromUserName === 'text') {
  //你也可以这样回复text类型的信息
  res.reply({
    content: 'text object',
    type: 'text'
  });
} else if (message.FromUserName === 'hehe') {
...
```

#### <a name="apidoc.element.wechat.reply2CustomerService"></a>[function <span class="apidocSignatureSpan">wechat.</span>reply2CustomerService (fromUsername, toUsername, kfAccount)](#apidoc.element.wechat.reply2CustomerService)
- description and source-code
```javascript
reply2CustomerService = function (fromUsername, toUsername, kfAccount) {
  var info = {};
  info.msgType = 'transfer_customer_service';
  info.createTime = new Date().getTime();
  info.toUsername = toUsername;
  info.fromUsername = fromUsername;
  info.content = {};
  if (typeof kfAccount === 'string') {
    info.content.kfAccount = kfAccount;
  }
  return compiled(info);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.wechat.session"></a>[function <span class="apidocSignatureSpan">wechat.</span>session (id, req, data)](#apidoc.element.wechat.session)
- description and source-code
```javascript
session = function (id, req, data) {
  Object.defineProperty(this, 'id', { value: id });
  Object.defineProperty(this, 'req', { value: req });
  if (data) {
    for (var key in data) {
      this[key] = data[key];
    }
  }
}
```
- example usage
```shell
...
OAuth功能请前往：<https://github.com/node-webot/wechat-oauth>

### WXSession支持
由于公共平台应用的客户端实际上是微信，所以采用传统的Cookie来实现会话并不现实，为此中间件模块在openid的基础上添加了Session支持。一旦服务端启用了'connect.session'中间件，在业务中就可以访问'req.wxsession'属性。这个属性与'
req.session'行为类似。

'''js
app.use(connect.cookieParser());
app.use(connect.session({secret: 'keyboard cat', cookie: {maxAge: 60000}}));
app.use('/wechat', wechat('some token', wechat.text(function (info, req, res, next) {
if (info.Content === '=') {
  var exp = req.wxsession.text.join('');
  req.wxsession.text = '';
  res.reply(exp);
} else {
  req.wxsession.text = req.wxsession.text || [];
...
```

#### <a name="apidoc.element.wechat.shortvideo"></a>[function <span class="apidocSignatureSpan">wechat.</span>shortvideo (fn)](#apidoc.element.wechat.shortvideo)
- description and source-code
```javascript
shortvideo = function (fn) {
  return (new Handler())[method](fn);
}
```
- example usage
```shell
...
// { ToUserName: 'gh_d3e07d51b513',
// FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
// CreateTime: '1359125022',
// MsgType: 'video',
// MediaId: 'OMYnpghh8fRfzHL8obuboDN9rmLig4s0xdpoNT6a5BoFZWufbE6srbCKc_bxduzS',
// ThumbMediaId: 'media_id',
// MsgId: '5837397520665436492' }
}).shortvideo(function (message, req, res, next) {
// message为短视频内容
// { ToUserName: 'gh_d3e07d51b513',
// FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
// CreateTime: '1359125022',
// MsgType: 'shortvideo',
// MediaId: 'OMYnpghh8fRfzHL8obuboDN9rmLig4s0xdpoNT6a5BoFZWufbE6srbCKc_bxduzS',
// ThumbMediaId: 'media_id',
...
```

#### <a name="apidoc.element.wechat.text"></a>[function <span class="apidocSignatureSpan">wechat.</span>text (fn)](#apidoc.element.wechat.text)
- description and source-code
```javascript
text = function (fn) {
  return (new Handler())[method](fn);
}
```
- example usage
```shell
...

### WXSession支持
由于公共平台应用的客户端实际上是微信，所以采用传统的Cookie来实现会话并不现实，为此中间件模块在openid的基础上添加了Session支持。一旦服务端启用了'connect.session'中间件，在业务中就可以访问'req.wxsession'属性。这个属性与'
req.session'行为类似。

'''js
app.use(connect.cookieParser());
app.use(connect.session({secret: 'keyboard cat', cookie: {maxAge: 60000}}));
app.use('/wechat', wechat('some token', wechat.text(function (info, req, res, next) {
if (info.Content === '=') {
  var exp = req.wxsession.text.join('');
  req.wxsession.text = '';
  res.reply(exp);
} else {
  req.wxsession.text = req.wxsession.text || [];
  req.wxsession.text.push(info.Content);
...
```

#### <a name="apidoc.element.wechat.toString"></a>[function <span class="apidocSignatureSpan">wechat.</span>toString ()](#apidoc.element.wechat.toString)
- description and source-code
```javascript
toString = function () {
    return toString;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.wechat.toXML"></a>[function <span class="apidocSignatureSpan">wechat.</span>toXML (data)](#apidoc.element.wechat.toXML)
- description and source-code
```javascript
toXML = function (data) {
  var include = function (path, includeData) {
    var d = utils.shallowCopy({}, data);
    if (includeData) {
      d = utils.shallowCopy(d, includeData);
    }
    return includeFile(path, opts)(d);
  };
  return fn.apply(opts.context, [data || {}, escapeFn, include, rethrow]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.wechat.video"></a>[function <span class="apidocSignatureSpan">wechat.</span>video (fn)](#apidoc.element.wechat.video)
- description and source-code
```javascript
video = function (fn) {
  return (new Handler())[method](fn);
}
```
- example usage
```shell
...
// { ToUserName: 'gh_d3e07d51b513',
// FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
// CreateTime: '1359125022',
// MsgType: 'voice',
// MediaId: 'OMYnpghh8fRfzHL8obuboDN9rmLig4s0xdpoNT6a5BoFZWufbE6srbCKc_bxduzS',
// Format: 'amr',
// MsgId: '5837397520665436492' }
}).video(function (message, req, res, next) {
// message为视频内容
// { ToUserName: 'gh_d3e07d51b513',
// FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
// CreateTime: '1359125022',
// MsgType: 'video',
// MediaId: 'OMYnpghh8fRfzHL8obuboDN9rmLig4s0xdpoNT6a5BoFZWufbE6srbCKc_bxduzS',
// ThumbMediaId: 'media_id',
...
```

#### <a name="apidoc.element.wechat.voice"></a>[function <span class="apidocSignatureSpan">wechat.</span>voice (fn)](#apidoc.element.wechat.voice)
- description and source-code
```javascript
voice = function (fn) {
  return (new Handler())[method](fn);
}
```
- example usage
```shell
...
// { ToUserName: 'gh_d3e07d51b513',
// FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
// CreateTime: '1359124971',
// MsgType: 'image',
// PicUrl: 'http://mmsns.qpic.cn/mmsns/bfc815ygvIWcaaZlEXJV7NzhmA3Y2fc4eBOxLjpPI60Q1Q6ibYicwg/0',
// MediaId: 'media_id',
// MsgId: '5837397301622104395' }
}).voice(function (message, req, res, next) {
// message为音频内容
// { ToUserName: 'gh_d3e07d51b513',
// FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
// CreateTime: '1359125022',
// MsgType: 'voice',
// MediaId: 'OMYnpghh8fRfzHL8obuboDN9rmLig4s0xdpoNT6a5BoFZWufbE6srbCKc_bxduzS',
// Format: 'amr',
...
```



# <a name="apidoc.module.wechat.Event"></a>[module wechat.Event](#apidoc.module.wechat.Event)

#### <a name="apidoc.element.wechat.Event.Event"></a>[function <span class="apidocSignatureSpan">wechat.</span>Event ()](#apidoc.element.wechat.Event.Event)
- description and source-code
```javascript
Event = function () {
  this.events = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.wechat.Event.dispatch"></a>[function <span class="apidocSignatureSpan">wechat.Event.</span>dispatch (event)](#apidoc.element.wechat.Event.dispatch)
- description and source-code
```javascript
dispatch = function (event) {
  return function (message, req, res, next) {
    // message为事件内容
    // { ToUserName: 'gh_d3e07d51b513',
    // FromUserName: 'oPKu7jgOibOA-De4u8J2RuNKpZRw',
    // CreateTime: '1359125022',
    // MsgType: 'event',
    // Event: 'LOCATION',
    // Latitude: '23.137466',
    // Longitude: '113.352425',
    // Precision: '119.385040',
    // MsgId: '5837397520665436492' }
    event._dispatch(message, req, res, next);
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.wechat.Event.prototype"></a>[module wechat.Event.prototype](#apidoc.module.wechat.Event.prototype)

#### <a name="apidoc.element.wechat.Event.prototype._dispatch"></a>[function <span class="apidocSignatureSpan">wechat.Event.prototype.</span>_dispatch (message, req, res, next)](#apidoc.element.wechat.Event.prototype._dispatch)
- description and source-code
```javascript
_dispatch = function (message, req, res, next) {
  if (this.events[message.Event]) {
    this.events[message.Event](message, req, res, next);
  } else {
    next();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.wechat.Event.prototype.add"></a>[function <span class="apidocSignatureSpan">wechat.Event.prototype.</span>add (event, callback)](#apidoc.element.wechat.Event.prototype.add)
- description and source-code
```javascript
add = function (event, callback) {
  this.events[event] = callback;
  return this;
}
```
- example usage
```shell
...
'req.wxsession'与'req.session'采用相同的存储引擎，这意味着如果采用redis作为存储，这样'wxsession'可以实现跨进程共享。

### 等待回复
等待回复，类似于电话拨号业务。该功能在WXSession的基础上提供。需要为等待回复预置操作，中间件将其抽象为'List'对象，在提供服务前需要添加服务。

'''js
var List = require('wechat').List;
List.add('view', [
['回复{a}查看我的性别', function (info, req, res) {
  res.reply('我是个妹纸哟');
}],
['回复{b}查看我的年龄', function (info, req, res) {
  res.reply('我今年18岁');
}],
['回复{c}查看我的性取向', '这样的事情怎么好意思告诉你啦- -']
...
```



# <a name="apidoc.module.wechat.List"></a>[module wechat.List](#apidoc.module.wechat.List)

#### <a name="apidoc.element.wechat.List.List"></a>[function <span class="apidocSignatureSpan">wechat.</span>List ()](#apidoc.element.wechat.List.List)
- description and source-code
```javascript
List = function () {
  this.map = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.wechat.List.add"></a>[function <span class="apidocSignatureSpan">wechat.List.</span>add (name, items, head, delimiter, foot)](#apidoc.element.wechat.List.add)
- description and source-code
```javascript
add = function (name, items, head, delimiter, foot) {
  var description = [];
  var list = new List();
  list.name = name;
  items.forEach(function (item) {
    var text = item[0];
    // 抽取出key，并关联上对应的handle
    var replaced = text.replace(/\{(.*)\}/, function (match, key) {
      list.map[key] = item[1];
      return key;
    });
    description.push(replaced);
  });

  if (delimiter) {
    var lists = description.join('\n' + delimiter + '\n');
    list.description = util.format('%s\n%s\n%s', head || '', lists, (foot || ''));
  } else {
    list.description = description.join('\n');
  }
  listCache[name] = list;
}
```
- example usage
```shell
...
'req.wxsession'与'req.session'采用相同的存储引擎，这意味着如果采用redis作为存储，这样'wxsession'可以实现跨进程共享。

### 等待回复
等待回复，类似于电话拨号业务。该功能在WXSession的基础上提供。需要为等待回复预置操作，中间件将其抽象为'List'对象，在提供服务前需要添加服务。

'''js
var List = require('wechat').List;
List.add('view', [
['回复{a}查看我的性别', function (info, req, res) {
  res.reply('我是个妹纸哟');
}],
['回复{b}查看我的年龄', function (info, req, res) {
  res.reply('我今年18岁');
}],
['回复{c}查看我的性取向', '这样的事情怎么好意思告诉你啦- -']
...
```

#### <a name="apidoc.element.wechat.List.clear"></a>[function <span class="apidocSignatureSpan">wechat.List.</span>clear ()](#apidoc.element.wechat.List.clear)
- description and source-code
```javascript
clear = function () {
  listCache = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.wechat.List.get"></a>[function <span class="apidocSignatureSpan">wechat.List.</span>get (name)](#apidoc.element.wechat.List.get)
- description and source-code
```javascript
get = function (name) {
  return listCache[name];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.wechat.List.prototype"></a>[module wechat.List.prototype](#apidoc.module.wechat.List.prototype)

#### <a name="apidoc.element.wechat.List.prototype.get"></a>[function <span class="apidocSignatureSpan">wechat.List.prototype.</span>get (key)](#apidoc.element.wechat.List.prototype.get)
- description and source-code
```javascript
get = function (key) {
  return this.map[key];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.wechat.session"></a>[module wechat.session](#apidoc.module.wechat.session)

#### <a name="apidoc.element.wechat.session.session"></a>[function <span class="apidocSignatureSpan">wechat.</span>session (id, req, data)](#apidoc.element.wechat.session.session)
- description and source-code
```javascript
session = function (id, req, data) {
  Object.defineProperty(this, 'id', { value: id });
  Object.defineProperty(this, 'req', { value: req });
  if (data) {
    for (var key in data) {
      this[key] = data[key];
    }
  }
}
```
- example usage
```shell
...
OAuth功能请前往：<https://github.com/node-webot/wechat-oauth>

### WXSession支持
由于公共平台应用的客户端实际上是微信，所以采用传统的Cookie来实现会话并不现实，为此中间件模块在openid的基础上添加了Session支持。一旦服务端启用了'connect.session'中间件，在业务中就可以访问'req.wxsession'属性。这个属性与'
req.session'行为类似。

'''js
app.use(connect.cookieParser());
app.use(connect.session({secret: 'keyboard cat', cookie: {maxAge: 60000}}));
app.use('/wechat', wechat('some token', wechat.text(function (info, req, res, next) {
if (info.Content === '=') {
  var exp = req.wxsession.text.join('');
  req.wxsession.text = '';
  res.reply(exp);
} else {
  req.wxsession.text = req.wxsession.text || [];
...
```



# <a name="apidoc.module.wechat.session.prototype"></a>[module wechat.session.prototype](#apidoc.module.wechat.session.prototype)

#### <a name="apidoc.element.wechat.session.prototype.destroy"></a>[function <span class="apidocSignatureSpan">wechat.session.prototype.</span>destroy (callback)](#apidoc.element.wechat.session.prototype.destroy)
- description and source-code
```javascript
destroy = function (callback) {
  delete this.req.wxsession;
  this.req.sessionStore.destroy(this.id, callback);
  return this;
}
```
- example usage
```shell
...
 * Callback:
 *
 * - 'err', 错误对象，删除发生错误时传入
 * @param {Function} callback 从存储中删除Session数据后的回调函数
 */
Session.prototype.destroy = function (callback) {
  delete this.req.wxsession;
  this.req.sessionStore.destroy(this.id, callback);
  return this;
};

module.exports = Session;
...
```

#### <a name="apidoc.element.wechat.session.prototype.save"></a>[function <span class="apidocSignatureSpan">wechat.session.prototype.</span>save (callback)](#apidoc.element.wechat.session.prototype.save)
- description and source-code
```javascript
save = function (callback) {
  this.req.sessionStore.set(this.id, this, callback || function(){});
  return this;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
