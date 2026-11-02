# Yingbei 英文法律页面

公司旗下多个 App 共用，当前点名包含 Arrow Melody；正文适用于由本公司发布、并链接至本协议的 App。

## 文件及部署

- `privacy-policy.html`：英文隐私政策。
- `user-agreement.html`：英文用户协议 / Terms of Use。
- `data-deletion.html`：英文账号与数据删除申请说明，包含预填邮件模板。
- `styles.css`：三个页面共用样式，支持手机与打印。

将上述四个文件按原有相对路径部署到公开 HTTPS 静态网站即可，无需构建。商店分别填写对应文件的公开 URL；Google Play 外部数据删除资源建议直接使用 `data-deletion.html`。

本次只创建本地网页，未部署公网，也未改动游戏项目或商店后台。页面没有 JavaScript、外部字体、图片、广告、统计脚本、Cookie 或本地存储；托管服务的访问日志属于单独的数据处理活动，需要按实际配置披露。

## 公司资料及来源

- 英文名称：Shenzhen Yingbei Network Technology Co., LTD（按用户提供的名称保留）。
- 中文登记名称：深圳市影贝网络科技有限公司。
- 统一社会信用代码：91440300MA5FLJAQ2U。
- 联系邮箱：yingbeiwangluo@163.com。
- 注册地址：深圳市宝安区西乡街道流塘社区榕树路68号流塘置地大厦1707B。
- 注册地址英文译文：Room 1707B, Liutang Zhidi Building, No. 68 Rongshu Road, Liutang Community, Xixiang Subdistrict, Bao'an District, Shenzhen, Guangdong 518100, China.

地址和信用代码依据用户于 2026-11-02 提供的[企查查公司详情链接](https://www.qcc.com/firm/914965866f4c527576e406c767da6860.html)及该详情页工商信息截图填写。直接网页抓取返回访问拦截，完整登记字段来自用户提供的截图，并非本次独立取得的工商官网证明。英文地址是上述中文地址的译写，保留中文原址便于核对及投递。

截图另列一处标注“2025年报”的通信地址。本版采用登记表中的注册地址，并明确标为 Registered address；未将较早年报通信地址擅自认定为当前注册地址。网页不公开截图中的法定代表人、资本等无关信息。

## 已完成的内容

- 一般受众休闲游戏定位，不专门面向 13 岁以下儿童，同时保留当地儿童隐私保护要求。
- 已列明用户确认的 Firebase Analytics、HUAWEI Analytics Kit、GameAnalytics、HUAWEI Ads / Petal Ads、TopOn / AnyThink、Unity Ads、AdMob，以及 HUAWEI ID、Google PGS、Apple Game Center 和商店内购。
- 按用途说明数据类别、来源、SDK 直接收集、共享、广告与统计选择、权限、保存标准、删除、地区权利和跨境处理。
- SDK 表为公司共用清单，以具体 App、渠道及启用配置为适用范围；未把聚合平台的整个合作伙伴目录写成本公司的已启用清单。
- 隐私政策与用户协议独立；增加独立删除申请页，三个页面互链。
- 已填入真实邮箱、注册地址和公司代码，清除正文占位符、审阅稿提示及 `noindex`。
- 没有编造欧盟/英国代表、DPO 姓名、专线、服务器端点或游戏内菜单路径。隐私事务由现有公司邮箱统一承接。

## 删除申请如何工作

`data-deletion.html` 的按钮使用 `mailto:`，打开预填公司邮箱、主题和资料模板的邮件草稿。用户需要自行检查并发送；没有邮件客户端时，可以手动使用自己的邮箱发送。页面不会在打开邮件草稿时声称“申请已提交”，也没有伪造后台处理接口。

申请范围包括本公司控制的 App 账号（如存在）及关联个人数据，也支持只删除特定数据。应通过必要且适度的验证定位记录，处理公司及受托处理方持有的数据，并告知合法保留例外和完成结果。

正文采用的处理目标为：**核验后的删除申请争取 30 天内完成**；法定答复期限、较短期限及依法允许的延期优先适用。这是公司需要兑现的处理承诺，不是已经测试过的自动化后台能力。应安排人员持续处理 `yingbeiwangluo@163.com` 的申请。

只存在于设备上的进度需要使用 App 重置或设备数据删除功能清除；平台账号、平台持有的独立副本和订阅续费单独管理。页面没有将退出登录、解绑、冻结或卸载等同于删除账号。

## 正式发行时仍需落实的产品行为

这些事项无法仅靠修改网页实现，也未在本次任务中修改游戏或控制台：

1. **App 内账号删除**：如果某发行版提供账号创建（包括符合规则定义的自动/访客账号），需要实际可用的 App 内删除入口。普通 iOS 游戏不能仅要求用户发邮件来替代该入口。当前文案没有宣称某个未经验证的菜单路径已经存在；外部邮件页也不能作为“已完成 Apple App 内删除”的证据。[Apple 账号删除要求](https://developer.apple.com/help/app-review/guideline-reference/5-1-1-account-deletion/)。
2. **先行同意及撤回**：确保广告、统计、ATT 及相关权限按适用规则在正确时机触发，SDK 初始化顺序与文案相符。GameAnalytics 另有玩家同意要求。[GameAnalytics Developer Policy](https://www.gameanalytics.com/trust/privacy-faq)。
3. **最终 SDK 清单与后台**：逐个发行包核对 TopOn 实际启用的其他广告源、SDK 版本、事件、权限、保存配置和跨境安排。用户确认的“Unity、AdMob 等”并未给出其他广告源名称，因此网页未擅自将未知网络写成已集成服务。近似命名的本地旧项目不能自动视为 Arrow Melody 的当前发行包。
4. **地区法定安排**：如果实际发行及处理触发欧盟/英国代表、DPO 或其他专项义务，需要真实任命和披露；不能靠编造联系人补齐。现有公司隐私邮箱不被描述为已经任命的境外代表。

数据保存采用用途、请求和法律义务等明确判断标准，没有虚构当前 SDK 后台已配置某个固定期限。中国法条款保留用户所在地不可排除的消费者保护；购买、订阅和广告移除条款仅对实际提供的功能适用。

## 商店与服务官方参考

- [Google Play User Data](https://support.google.com/googleplay/android-developer/answer/10144311?hl=en)：公开可访问的隐私页面、数据披露和安全要求。[Google 账号删除资源说明](https://support.google.com/googleplay/android-developer/answer/13327111?hl=en)：外部删除请求渠道及相关要求。
- [Apple App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)、[Apple 标准/自定义 EULA 说明](https://developer.apple.com/help/app-store-connect/manage-app-information/provide-a-custom-license-agreement/)。当前用户协议引用保留 Apple 标准 EULA；未配置自定义 EULA 时不要把此网页当作已经满足全部 Apple 自定义 EULA 最低条款的文本提交。
- [HUAWEI AppGallery Review Guidelines](https://developer.huawei.com/consumer/en/doc/distribution/app/30202)、[Policy Center](https://developer.huawei.com/consumer/en/policy-center/)、[HMS Core Privacy Statement](https://developer.huawei.com/consumer/en/doc/hmscore-common-Guides/privacy-0000001261262707)。部分华为动态文档无法完整抓取，应以实际海外发行版本和后台当前规则为准。
- [Firebase 隐私](https://firebase.google.com/support/privacy)、[GameAnalytics Developer Policy](https://www.gameanalytics.com/trust/privacy-faq)、[TopOn 广告隐私](https://www.toponad.net/en/privacy-policy)、[Unity 玩家隐私](https://unity.com/legal/game-player-and-app-user-privacy-policy)、[Google 合作方数据说明](https://policies.google.com/technologies/partner-sites?hl=en)。
- [Google PGS 数据披露](https://developer.android.com/games/pgs/data-collection)、[Game Center 隐私](https://www.apple.com/legal/privacy/data/en/game-center/)、[HUAWEI ID 隐私](https://consumer.huawei.com/minisite/cloudservice/id/common/b0/latest/privacy-statement.htm)。

各商店的开发者名称、App 内实际行为及隐私标签/Data safety 填报应与页面一致。网页文案完整不等于已审计游戏全部合规性，也不构成商店审核保证。

## 验证结果

- 三页 HTML 嵌套、主标题、所有本地文件链接和页内锚点通过检查。
- 三页均无未填写标记、审阅稿提示、旧邮箱或 `noindex`。
- 两份协议的注册地址、信用代码及邮箱一致；删除按钮的收件地址、主题和预填模板已校验。
- 已用浏览器实际检查三页互链、390px 手机页面及 1280px 电脑布局，无整页横向溢出。
- 尚未验证公网部署、邮箱投递及后台删除执行；静态页不会发送或自动处理删除请求。
