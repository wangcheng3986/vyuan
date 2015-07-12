# vyuan
服务端协议

域名："http://api.yuanchuangtech.com/webapi/"
通用header：
channelId：“” 渠道
versionName：““ 版本
versionCode：“” 版本
deviceId；“” 设备id
model：“” 手机型号
app：“” 应用程序包名

{app=com.prone.vyuan, model=HM 1SC, channelId=1101, versionCode=121, versionName=2.0.1201, deviceId=99000550830036}

[Accept-Encoding: gzip, deflate, Accept-Charset: UTF-8,*;q=0.5, Cache-Control: no-cache, Cookie: _c=de5MR4oV06PMKCYxF6Pm+eSc0uFT0mNa0Ol396hpD8fCdmcc0CPa0wayR9wpfOwCECSLKmaV0yoVFiDYf93pXZFaKZoJ0mPBd4laR93xfbqpfsgpXCNaECasFDayR9yPfOgMo9DMBOfMfOfmXv==;]


1.登陆 queryLogin					
  
    	url:”api/cgi1.cgi"
	
上行协议：[account, 18659032, password, cccccc]	
下行协议：{"data":{"avatarCount":0,"workCity":10131001,"isVipUser":0,"nickname":"会员18659032","cookieMap":{"remember":"6081d0d06bf28018998042728e87bd3f","s":"QyQCLzxtfLT3YTfkfWIr","userId":"18659032"},"userId":"18659032","photoCount":0,"gender":1,"isReplyUser":0,"goldAmount":"0"},"msg":"成功","status":1}	

	{"status":-1,"msg":"密码错误"}
	{“data":null,"msg":"参数错误","status":-1}
2.qq登陆：queryloginQQ	

 	url：”api/cgi2.cgi“
	[openId, 1B86E42E203C8F4F7B6CA166B6A2CBB6, accessToken, 630D6DC81DA8DE19F3A7C94C84FE0A15]
	{"data":{"isFirstLogin":true},"msg":"成功","status":1}	
3 修改qq登陆时的个人信息：editloginQQSaveProfile		
   	url：”api/cgi3.cgi"
	[openId, 1B86E42E203C8F4F7B6CA166B6A2CBB6, accessToken, 630D6DC81DA8DE19F3A7C94C84FE0A15, nickname, 骕骦凌空, gender, 1, year, 1988, month, 1, day, 1, workCity, 10104000, height, 170]
	{"data":{"avatarCount":0,"workCity":10104000,"isVipUser":0,"nickname":"会员18659037","cookieMap":{"remember":"10328e15210694299fd5c7b01a0baac7","s":"kDErjI35QYLv7gmWFSW5","userId":"18659037"},"userId":"18659037","photoCount":0,"gender":1,"isReplyUser":0,"goldAmount":"0"},"msg":"成功","status":1}

4. queryloginAuto		
	url："api/cgi4.cgi"
	[]		
	{"data":{"avatarCount":0,"workCity":10104000,"isVipUser":0,"nickname":"会员18659031","cookieMap":{"remember":"ba9d22121d05718bb2d6f649a9fd100a","s":"rMyB9ToKQKMCezGEsNcZ","userId":"18659031"},"userId":"18659031","photoCount":0,"gender":1,"isReplyUser":0,"goldAmount":"0"},"msg":"成功","status":1}

5 editRegister				
	"api/cgi7.cgi"),
	[regType, simple, gender, 1, year, 1994, month, 1, day, 1, workCity, 10104000, nickname, cc, password, 123456, height, 170]

6 editSayHi					(8, 			"api/cgi8.cgi"),
7	queryMmsUnReadCount			(9,				"api/cgi9.cgi"),
8	editMmsSend					(10,			"api/cgi10.cgi"),
	
9	queryMmsConv				(12,			"api/cgi12.cgi"),
	[] /[startIndex, 0]	
	{"data":{"adminCount":0,"receiveCount":3},"msg":"成功","status":1}
{"data":[{"workCity":"西藏阿里","isVipUser":0,"nickname":"小妙","_sendTime":"1436669315000","sendTime":"上午 10:48","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqcDLz/TuEqpN/AgAgwK/iOoDRgXB.jpg","marriage":"未婚，寻觅中","education":"大专以下","isReplyUser":0,"emailSummary":"想知道你长什么样子啊","emailType":4,"dataType":2,"notReadCount":1,"height":160,"userId":"17961033","age":27,"gender":2,"salary":"2000到3000","locked":15,"LocationInfo":{}},{"workCity":"四川德阳","isVipUser":0,"nickname":"sunny","_sendTime":"1436669130000","sendTime":"上午 10:45","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbEq/RbAgEq/AgRbwK/nEPVhbSd.jpg","marriage":"未婚，寻觅中","education":"大专","isReplyUser":0,"emailSummary":"你的资料好少哦，发张照片吧","emailType":4,"dataType":2,"notReadCount":1,"height":144,"userId":"18183138","age":30,"gender":2,"salary":"5000到8000","locked":15,"LocationInfo":{}},{"workCity":"辽宁丹东","isVipUser":0,"nickname":"谜族珍贵","_sendTime":"1436668620000","sendTime":"上午 10:37","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbpN/EqEqTu/pNmSwK/plJsWiBR.jpg","marriage":"未婚，寻觅中","education":"大专","isReplyUser":0,"emailSummary":"有空多了解一下","emailType":4,"dataType":2,"notReadCount":1,"height":166,"userId":"18011605","age":30,"gender":2,"salary":"5000到8000","locked":15,"LocationInfo":{}},{"workCity":"北京","isVipUser":0,"nickname":"管理员小薇","_sendTime":"1436668558000","sendTime":"上午 10:35","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqpNpN/pNpNwK/wKwKwK/rBQXRwqJ.jpg","marriage":"未婚，寻觅中","education":"本科","isReplyUser":0,"emailSummary":"感谢您注册情缘网,你的账号ID为:18659031,请牢记你","emailType":3,"dataType":2,"notReadCount":1,"height":167,"userId":"10000","age":26,"gender":2,"salary":"4-6千元","locked":0,"LocationInfo":{"longitude":113.955294,"latitude":22.561022}}],"msg":"最后一页","status":11}

10	deleteMmsConv				(13,			"api/cgi13.cgi"),
11	queryMmsConvDetail			(14,			"api/cgi14.cgi"),
	{"data":{"userInfo":{"sendFlag":0,"isVipUser":0,"nickname":"会员18659031","userId":"18659031","gender":1,"locked":0,"avatar":"http://img1.static.yuanchuangtech.com/user-album/default/1-0.jpg","isReplyUser":0},"objUserInfo":{"isVipUser":0,"nickname":"小妙","userId":"17961033","gender":2,"locked":15,"avatar":"http://img1.static.yuanchuangtech.com/user-album/EqcDLz/TuEqpN/AgAgwK/iOoDRgXB.jpg","isReplyUser":0},"emailList":[{"content":"想知道你长什么样子啊","emailType":2,"emailId":"249","_sendTime":"1436669315000","sendTime":"2015-07-12 10:48:35","sendBy":4,"contentId":"7943253680755278233"}]},"msg":"最后一页","status":11}


12  editAddLbs					(16,			"api/cgi16.cgi"),
13	editBuyProductByMobileCard	(22,			"api/cgi22.cgi"),
14	queryAlipayOrder			(23,			"api/cgi23.cgi"),
15	queryAlipayMiniOrder		(24,			"api/cgi24.cgi"),
16	queryAlipayWapOrder			(25,			"api/cgi25.cgi")
[productId, 1003, money, 100.00]	
	{"data":{"redirectURL":"http://wappaygw.alipay.com/service/rest.htm?sign=9d2445e71dfeaecf7e176a4a56b79f4e&sec_id=MD5&v=2.0&req_data=%3Cauth_and_execute_req%3E%3Crequest_token%3E201507123b2bd7cafe3a8e7c546fd06a3049335b%3C%2Frequest_token%3E%3C%2Fauth_and_execute_req%3E&service=alipay.wap.auth.authAndExecute&partner=2088611286435550&format=xml"},"msg":"成功","status":1}

17	queryProductVipList			(26,			"api/cgi26.cgi"),
18	queryProductMmsList			(27,			"api/cgi27.cgi")
{"data":[{"money":30,"month":1,"hot":1,"prodcutId":1001,"oldmoney":50,"presentLogo":"","parentName":"发信会员"},{"money":50,"month":3,"hot":1,"prodcutId":1002,"oldmoney":80,"presentLogo":"","parentName":"发信会员"},{"money":100,"month":12,"hot":1,"prodcutId":1003,"oldmoney":100,"presentLogo":"","parentName":"发信会员"}],"msg":"成功","status":1}
	
19	queryMemberBalance			(28,			"api/cgi28.cgi")
[]	
{"data":{"isVipUser":0,"serviceTime":{},"account":0,"isReplyUser":0},"msg":"成功","status":1}	
20	editPhotoUpload				(29,			"api/cgi29.cgi"),
21	editPhotoSetAvatar			(30,			"api/cgi30.cgi"),
22	queryPhotoList				(31,			"api/cgi31.cgi"),
23	deletePhoto					(32,			"api/cgi32.cgi"),
24	querySearchListById			(33,			"api/cgi33.cgi"),
25	querySearchGetSetting		(34,			"api/cgi34.cgi"),

26	querySearchListBySetting	(35,			"api/cgi35.cgi"),
	[gender, 2, workCity, 10104000, avatar, 0, pageIndex, 2]

	{"data":[{"workCity":"天津","height":162,"isVipUser":0,"nickname":"WeChat：cherr","age":23,"userId":"18346302","photoCount":1,"gender":2,"LocationInfo":{},"education":"大专","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbAg/iHTuAg/pNoJwK/FznFvmqh.jpg","isReplyUser":0},{"workCity":"天津","height":165,"isVipUser":0,"nickname":"欣语忆夣","age":27,"userId":"18080807","photoCount":1,"gender":2,"LocationInfo":{},"education":"本科","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbpN/RbpNRb/pNcDwK/CJCznpjb.jpg","isReplyUser":0},{"workCity":"天津","height":162,"isVipUser":0,"nickname":"歇斯底里的微笑","age":26,"userId":"18065918","photoCount":1,"gender":2,"LocationInfo":{},"education":"本科","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbpN/TumSLz/EqRbwK/HyjQFHNa.jpg","isReplyUser":0},{"workCity":"天津","height":160,"isVipUser":0,"nickname":"小月","age":25,"userId":"18345226","photoCount":1,"gender":2,"LocationInfo":{},"education":"本科","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbAg/iHmSoJ/oJTuwK/HhNgUIBW.jpg","isReplyUser":0},{"workCity":"天津","height":160,"isVipUser":0,"nickname":"喵丫头","age":29,"userId":"18212108","photoCount":1,"gender":2,"LocationInfo":{},"education":"大专以下","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRboJ/EqoJEq/pNRbwK/cLPYUgwj.jpg","isReplyUser":0},{"workCity":"天津","height":163,"isVipUser":0,"nickname":"EchoZ","age":29,"userId":"18016526","photoCount":1,"gender":2,"LocationInfo":{},"education":"大专","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbpN/EqTumS/oJTuwK/ITnaIQGm.jpg","isReplyUser":0},{"workCity":"天津","height":160,"isVipUser":0,"nickname":"晓晓","age":31,"userId":"18335664","photoCount":1,"gender":2,"LocationInfo":{},"education":"大专以下","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbAg/AgmSTu/TuiHwK/AvDEuxpT.jpg","isReplyUser":0},{"workCity":"天津","height":152,"isVipUser":0,"nickname":"婷婷","age":25,"userId":"18058149","photoCount":1,"gender":2,"LocationInfo":{},"education":"本科","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbpN/mSRbEq/iHLzwK/ItyYpgiw.jpg","isReplyUser":0},{"workCity":"天津","height":164,"isVipUser":0,"nickname":"妮妮","age":29,"userId":"18024511","photoCount":1,"gender":2,"LocationInfo":{},"education":"大专以下","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbpN/oJiHmS/EqEqwK/PbdcntGw.jpg","isReplyUser":0},{"workCity":"天津","height":168,"isVipUser":0,"nickname":"李颖","age":29,"userId":"17896346","photoCount":1,"gender":2,"LocationInfo":{},"education":"大专以下","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqcDRb/LzTuAg/iHTuwK/WMhekwWL.jpg","isReplyUser":0}],"msg":"成功","status":1}


27	querySysConfig				(36,			"api/cgi36.cgi"),
28	queryVersion				(37,			"api/cgi37.cgi"),
		[]
		{"data":{"content":"1.修改消息有时接收不到的bug。 \\n2优化UI。","payWay":"1","forceUpdate":"0","url":"http://dl.yuanchuangtech.com/qingyuan/2.0.1111/qingyuan_2.0.1111_1101.apk","version":"2.0.1111"},"msg":"成功","status":1}

29	editLike					(38,			"api/cgi38.cgi"),
30	deleteLike					(39,			"api/cgi39.cgi"),
31	queryLikeList				(40,			"api/cgi40.cgi"),
32	queryLikeMeList				(41,			"api/cgi41.cgi")
[pageIndex, 1]
{"data":{"list":[],"rowCount":0},"msg":"最后一页","status":11}
	
33	editMateProfile				(42,			"api/cgi42.cgi"),
34	editProfile					(43,			"api/cgi43.cgi")

	[workCity, 10104000, height, 170, marriage, 1, education, 4, nation, 1, occupation, 0, salary, 4, bloodType, 1, house, 0, car, 0, introduce, tttttt

, nickname, 骕骦凌空]
	{"data":{},"msg":"成功","status":1}

35	queryProfile				(44,			"api/cgi44.cgi"),
[userId, 18024511]
{"data":{"userDetail":{"car":"","birthday":"1985-11-07","workCity":"天津","isVipUser":0,"visitedTipCount":1,"introduce":"大家好，我是一个独立的女孩，现在我理想中的约会方式是牵手漫步在公园，彼此相依相偎，希望将来过安定、温馨，下雨有人接的生活。对于我的另一半，我希望他是一个有责任心的男士……希望在情缘网能找到牵手一辈子的他。","children":"","house":"","education":"大专以下","photoList":[{"photoId":"8227243867429807588","verified":1,"avatar":1,"photo":"http://img1.static.yuanchuangtech.com/user-album/EqRbpN/oJiHmS/EqEqwK/PbdcntGw.jpg"}],"height":164,"userId":"18024511","age":29,"gender":2,"attentionedTipCount":0,"salary":"2000到3000","occupation":"","attentionCount":0,"nickname":"妮妮","photoCount":1,"marriage":"未婚，寻觅中","avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbpN/oJiHmS/EqEqwK/PbdcntGw.jpg","isReplyUser":0,"nation":"","bloodType":"","LocationInfo":{}},"mateDetail":{"userId":"18024511","workCity2":"","workCity3":"","gender":"男士","workCity1":"天津","age2":38,"education1":"","age1":26,"height2":0,"education2":"","marriages":"未填","height1":0},"userCode":{"car":0,"birthday":"1985-11-07 00:00:00","occupation":0,"workCity":10104000,"children":0,"house":0,"avatar":"PbdcntGw.jpg","education":2,"marriage":1,"nation":0,"bloodType":0,"height":164,"userId":"18024511","gender":2,"salary":3},"mateCode":{"createTime":null,"updateTime":null,"workCity2":0,"workCity3":0,"workCity1":10104000,"photo":0,"userId":"18024511","gender":1,"serialVersionUID":null,"age2":38,"age1":26,"education1":0,"height2":0,"education2":0,"marriages":"0","height1":0}},"msg":"成功","status":1}
36	queryVisitMeList			(45,			"api/cgi45.cgi")
[pageIndex, 1]		
{"data":{"list":[{"visiterId":"18004200","height":162,"workCity":"重庆","isVipUser":0,"_lastVisitTime":"1436671450000","nickname":"陌的的","age":23,"userId":"18004200","gender":2,"LocationInfo":{},"avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbpN/pNiHoJ/pNpNwK/mEEUYAnN.jpg","isReplyUser":0},{"visiterId":"18267705","height":161,"workCity":"广东惠州","isVipUser":0,"_lastVisitTime":"1436670940000","nickname":"丽丽","age":28,"userId":"18267705","gender":2,"LocationInfo":{},"avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRboJ/TucDcD/pNmSwK/gaHjkdkl.jpg","isReplyUser":0},{"visiterId":"17961033","height":160,"workCity":"西藏阿里","isVipUser":0,"_lastVisitTime":"1436669315000","nickname":"小妙","age":27,"userId":"17961033","gender":2,"LocationInfo":{},"avatar":"http://img1.static.yuanchuangtech.com/user-album/EqcDLz/TuEqpN/AgAgwK/iOoDRgXB.jpg","isReplyUser":0},{"visiterId":"18183138","height":144,"workCity":"四川德阳","isVipUser":0,"_lastVisitTime":"1436669130000","nickname":"sunny","age":30,"userId":"18183138","gender":2,"LocationInfo":{},"avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbEq/RbAgEq/AgRbwK/nEPVhbSd.jpg","isReplyUser":0},{"visiterId":"18011605","height":166,"workCity":"辽宁丹东","isVipUser":0,"_lastVisitTime":"1436668620000","nickname":"谜族珍贵","age":30,"userId":"18011605","gender":2,"LocationInfo":{},"avatar":"http://img1.static.yuanchuangtech.com/user-album/EqRbpN/EqEqTu/pNmSwK/plJsWiBR.jpg","isReplyUser":0}],"rowCount":5},"msg":"最后一页","status":11}


37	editPasswrod				(46, 			"api/cgi46.cgi"),
38	editBuyProductByGoldCoin 	(500, 			"api/cgi47.cgi"),
39	//未完成接口
	editFeedback			 	(500, 			"api/cgi500.cgi"),
	
40 queryProductGoldCoin		(500,			"api/cgi500.cgi"),
