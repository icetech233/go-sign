# 说明文档

### api 的地址 

https://api-takumi.mihoyo.com/

### 接口

```

获取账号信息
/binding/api/getUserGameRolesByCookie?game_biz=hk4e_cn

获取签到信息,是否已经签到
/event/bbs_sign_reward/info?

签到
/event/bbs_sign_reward/sign

```


```

请求报文

POST https://api-takumi.mihoyo.com/event/bbs_sign_reward/sign HTTP/1.1
Host: api-takumi.mihoyo.com
Accept-Encoding: gzip, deflate
User-Agent: Mozilla/5.0 (Linux; Android 12; SM-G955U Build/R16NW; wv) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/104.0.0.0 Safari/537.36 miHoYoBBS/2.35.2
Referer: https://webstatic.mihoyo.com/bbs/event/signin-ys/index.html?bbs_auth_required=true&act_id=e202009291139501&utm_source=bbs&utm_medium=mys&utm_campaign=icon
Cookie: UM_distinctid=xxxx;....
x-rpc-device_id: b0b40000-0000-0000-0000-000000000000
x-rpc-client_type: 5
x-rpc-app_version: 2.35.2
DS: 1665485038,000000,xxxx08ed3be56482d0f377ef4afexxxx
Content-Type: application/json
Content-Length: 66

{"act_id":"e202009291139501","region":"cn_gf01","uid":"10xxxxxxxx"}

HTTP/1.1 200 OK
Date: Tue, 11 Oct 2022 10:43:58 GMT
Content-Type: application/json
Content-Length: 73
Connection: keep-alive
Set-Cookie: aliyungf_tc=xxxx; Path=/; HttpOnly
Set-Cookie: account_id=xxxxx; Path=/; Domain=mihoyo.com; Max-Age=2592000
Set-Cookie: cookie_token=xxxx; Path=/; Domain=mihoyo.com; Max-Age=2592000
Vary: Accept-Encoding
X-Powered-By: takumi
X-Trace-Id: xxxxx:xxxxx:0:0


{"retcode":0,"message":"OK","data":{"code":"","risk_code":0,"gt":"","challenge":"","success":0}}

{"data":null,"message":"旅行者,你已经签到过了","retcode":-5003}

```