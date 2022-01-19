‼️由于个人原因，不接受任何SteamBot订单，包括但不限于Buff扫货机器人、自动化爬虫、商城定制化等(谢谢大家的热心支持了，但烦请不要再用邮件问我是否接单了，统一回复就是不接不能不做)‼️
⚠️项目停止维护，QQ群已转移，终止技术支持，大家有缘再见⚠️
<!--markdown--><span style="font-family: 微软雅黑;"><span style="font-size: x-large;"><strong>简介:</strong></span></span>
<span style="font-family: 微软雅黑;">目前已提供完整的函数库,各位dalao可直接通过二次开发成Bot便可投入使用,本项目严格遵守<span style="color: red;"><strong>Apache License V2</strong></span></span>
<span style="font-family: 微软雅黑;">以下为目前已实现的API
</span>
<ul>
 	<li><span style="font-family: 微软雅黑;"><strong>接受/拒绝/取消/发起交易</strong></span></li>
 	<li><span style="font-family: 微软雅黑;"><strong>支持二步验证的登录</strong></span></li>
 	<li><span style="font-family: 微软雅黑;"><strong>获取单笔交易状态</strong></span></li>
	 <li><span style="font-family: 微软雅黑;"><strong>获取steamID SessionID</strong></span></li>
 	<li><span style="font-family: 微软雅黑;"><strong>获取玩家游戏列表</strong></span></li>
 	<li><span style="font-family: 微软雅黑;"><strong>获取API秘钥</strong></span></li>
 	<li><span style="font-family: 微软雅黑;"><strong>获取玩家库存</strong></span></li>
 	<li><span style="font-family: 微软雅黑;"><strong>支持自动过二步验证[需要提供shared_sersect,方法详参我的博客]</strong></span></li>
 	<li><span style="font-family: 微软雅黑;"><strong>支持面对象</strong>
    <li><span style="font-family: 微软雅黑;"><strong>支持代理服务器</strong></span></li>
</span></li>
 	<li><span style="font-family: 微软雅黑;"><strong>支持遍历未确认的交易请求</strong></span></li>
 	<li><span style="font-family: 微软雅黑;"><strong>确认/取消发回饰品的交易</strong></span></li>
</ul>

<span style="font-family: 微软雅黑;">
</span>

<span style="font-size: x-large;"><strong>可用方法:</strong></span>
<table class="t_table" cellspacing="0">
<tbody>
<tr>
<td>setSteamID</td>
<td>设定SteamID</td>
</tr>
<tr>
<td>setDeviceID</td>
<td>设定DeviceID</td>
</tr>
<tr>
<td>setSharedSecret</td>
<td>设定SharedSecert</td>
</tr>
<tr>
<td>setIdentitySecret</td>
<td>设定IdentitySecret</td>
</tr>
<tr>
<td>setProxyServer</td>
<td>设定代理服务器信息</td>
</tr>
<tr>
<td>getApiKey</td>
<td>获取API-KEY</td>
</tr>
<tr>
<td>getgamelist</td>
<td>获取用户游戏列表</td>
</tr>
<tr>
<td>getinventory</td>
<td>获取用户库存</td>
</tr>
<tr>
<td>send</td>
<td>发起一笔饰品交易</td>
</tr>
<tr>
<td>login</td>
<td>登录Steam账户</td>
</tr>
<tr>
<td>acceptoffer</td>
<td>接受交易报价</td>
</tr>
<tr>
<td>canceloffer</td>
<td>取消交易报价</td>
</tr>
<tr>
<td>declineoffer</td>
<td>拒绝交易报价</td>
</tr>
<tr>
<td>GenerateSteamGuardCode</td>
<td>生成2FA验证码</td>
</tr>
<tr>
<td>fetchConfirmations</td>
<td>遍历确认列表</td>
</tr>
<tr>
<td>getConfirmationTradeOfferId</td>
<td>获取交易确认页的TradeOfferId</td>
</tr>
<tr>
<td>acceptConfirmation</td>
<td>接受确认请求</td>
</tr>
<tr>
<td>cancelConfirmation</td>
<td>取消确认请求</td>
</tr>
</tbody>
</table>
<span style="font-size: x-large;"><strong><span style="font-family: 微软雅黑;">
</span></strong></span>
<strong><span style="font-family: 微软雅黑;"><span style="font-size: x-large;">交易字符串样例:</span></span></strong>
<br>
<code>
{
"newversion":true,
"version":1,
"me":{"assets":[{"appid":"游戏AppID","contextid":"2","amount":1,"assetid":"游戏饰品的ID"}],"currency":[],"ready":true},
"them":{"assets":[],"currency":[],"ready":false}
}
</code>
assets里面必须是数组,而不是对象
<br>
<span style="font-size: x-large;"><strong><span style="font-family: 微软雅黑;">开发文档:</span></strong></span>
<br>
<a href="https://www.yuque.com/books/share/8f76ee1e-917e-4656-82d2-cebec314829c?#">https://www.yuque.com/books/share/8f76ee1e-917e-4656-82d2-cebec314829c?#</a>
<br>
<span style="font-size: x-large;"><strong><span style="font-family: 微软雅黑;">注意事项:</span></strong></span>
这些是使用Umarket试运营后得出的一些注意事项,请注意!
<ul class="litype_1" type="1">
 	<li>机器人账户一定要有超过5USD的交易记录,不然作为受限账户是无法发起发回交易的</li>
 	<li>机器人一定要有消费记录,不然可能会受限,暂挂住商品</li>
 	<li>Steamcommunity极其不稳定,有时候login返回Null或者Empty Response都是因为无法正常访问Steam的服务造成的</li>
 	<li>Steam的交易确认页面有时候会抽搐,需要多加载几次,才能刷新出来</li>
 	<li>解决无法访问Steam服务的方法有两个一是使用各家的加速器,二是使用科学手段来修复网络不可用,三是把机器人放到国外去</li>
</ul>
<span style="font-size: x-large;"><strong><span style="font-family: 微软雅黑;">
</span></strong></span>

<strong><span style="font-family: 微软雅黑;"><span style="font-size: x-large;">更新日志:</span></span></strong><br>
<span style="font-family: 微软雅黑;">2021/09/25:</span>
<span style="font-family: 微软雅黑;">各位江湖有缘再见，项目终止维护，谢谢大家这么多年来的支持🙏。</span>
<br>
<span style="font-family: 微软雅黑;">2021/05/01:</span>
<span style="font-family: 微软雅黑;">各位劳动节快乐呀！希望大家玩的开心😄，最近作者开始准备考研了，因此维护工作也只能暂时放下了。预计明年上岸后才能继续维护，希望得到大家的理解，谢谢🙏。</span>
<br>
<span style="font-family: 微软雅黑;">2020/11/26:</span>
<span style="font-family: 微软雅黑;">又快要过完一年了，在这一年里面，项目的状态从开发中转入维护状态，我也没有太多精力在Steam交易上面了，所以从今日起，我暂停接手Steam交易机器人的二次开发和定制，如果有需要的话，请另寻别家吧！希望各位同仁多多见谅。日志就先写到这了，有缘再见Peace！</span>
<br>
<span style="font-family: 微软雅黑;">2019/06/15:</span>
<span style="font-family: 微软雅黑;">时隔一年时间,加入了遍历确认的功能。</span>
<span style="font-family: 微软雅黑;">Umarket也弃坑了[项目太大了,一个人无法carry,以后再考虑用框架重写]</span>
<span style="font-family: 微软雅黑;">不过这个SteamBot终于可以用于实际的项目中了,已形成一个交易闭环了,接下去就交由各位dalao做下去吧OWO</span>
<span style="font-family: 微软雅黑;">还有就是,欢迎大家常到我的Blog看看呀,就写到这了,Peace</span>