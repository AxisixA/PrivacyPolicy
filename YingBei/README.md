# Yingbei 英文协议网页

适用于 Shenzhen Yingbei Network Technology Co., LTD 旗下链接至这些协议的多个 App；正文点名包含 Arrow Melody，后续同类产品可复用。

## 文件

- `privacy-policy.html`：英文隐私政策，包含 SDK 披露、广告/统计同意、平台账号、内购、保存及删除、地区权利和儿童条款。
- `user-agreement.html`：英文用户协议 / Terms of Use。
- `styles.css`：两页共用样式，适配手机和打印。

无需构建或依赖安装。正文直接写在 HTML 中，没有 JavaScript、外部字体、图片、广告或统计脚本。页面本身不设置 Cookie 或浏览器本地存储；上线后的服务器访问日志需要按实际托管配置处理。

## 已依据用户确认的信息编写

- 公司旗下多个 App 通用，当前游戏包括 Arrow Melody。
- 一般受众休闲游戏，不专门面向 13 岁以下儿童。
- 统计：Google Analytics for Firebase、HUAWEI Analytics Kit、GameAnalytics。
- 广告：HUAWEI Ads / Petal Ads、TopOn / AnyThink 聚合，广告源包括 Unity Ads、AdMob。
- 平台服务：HUAWEI ID、Google Play Games Services、Apple Game Center。
- 包含内购；订阅条款仅在某 App 实际提供订阅时适用。
- 隐私及客服邮箱：yingbeiwangluo@163.com（两页均已添加可点击的邮件链接）。

## 发布前必须完成

1. 两页已使用用户提供的 `yingbeiwangluo@163.com`，并设置 `mailto:` 链接。上线时确保此邮箱可以正常接收和处理隐私、客服及删除请求。
2. 替换 `[COMPANY_POSTAL_ADDRESS]` 为公司真实对外联系地址。不要将第三方 SDK 公司的联系信息填成自己的信息。
3. 确认各 App 使用平台登录后是否还创建/保存 Yingbei 游戏账号。将隐私页中的 `[ACCOUNT_DELETION_DETAILS]` 替换为真实的 App 内删除路径，或明确说明没有独立 Yingbei 账号及删除游戏数据的方法。不能将“解绑”“退出登录”或“冻结”写成删除账号。
4. `[REGIONAL_REPRESENTATIVE_OR_DPO_DETAILS_IF_REQUIRED]`：按目标市场和业务情况确认是否需要欧盟/英国代表或 DPO；适用则填写，不适用则删除该句。不要凭空指定代表。
5. 在每个发行包核对实际 SDK、版本、权限、事件、广告聚合配置和数据传输。特别核对 TopOn 中“等”所指的其他广告源：目前正文只列出了已提供的 Unity Ads、AdMob 和华为广告；实际启用其他网络必须补齐其名称、用途、数据类别和官方隐私链接。公司通用表不等于所有 App 都集成全部服务。
6. 核对实际保存期限/判断标准、服务器地区和跨境传输安排。正文没有擅自假定 Firebase/华为后台选择了某个固定期限；如有固定期限，可进一步写入。跨境保护、加密、数据删除等承诺必须在实际流程中兑现。
7. 确认 App 中已有独立可撤回的广告和统计选择、所需的先行告知、ATT 和必要权限控制。仅有网页不等于完成 SDK 同意管理；GameAnalytics 也有自己的初始化前同意要求。
8. 核对用户协议中的产品示例、购买恢复能力、广告移除范围和订阅流程。当前默认中国法并保留用户所在地不可排除的消费者权利；正式发布前确认公司接受这一争议解决安排。
9. 完成后去除两页顶部的 `.review-note` 审阅提示。`noindex` 只用于避免审阅稿被索引，正式发布可删除该 meta；它不代替访问控制，也不会阻止拥有链接的人访问页面。

查找所有待填标记：

```sh
rg -n '\[[A-Z_ ,]+\]' privacy-policy.html user-agreement.html
```

## 商店接入

将两个 HTML 和 `styles.css` 一起放到自己的公开 HTTPS 静态网站，保持相对路径不变。建议提交直接地址：

- 隐私政策：`https://你的域名/你的路径/privacy-policy.html`
- 用户协议：`https://你的域名/你的路径/user-agreement.html`
- 删除说明：`https://你的域名/你的路径/privacy-policy.html#delete-data`

以上域名是部署示意，尚未创建公开网站。目录中不会自动生成可提交商店的公网网址。托管应允许不登录、无地域限制地访问正文，不应通过阅读协议触发强制同意广告或统计。

- **Google Play**：在 Play Console 和 App 中提供隐私政策链接，按每个 App 的真实 SDK 行为填写 Data safety。若该 App 提供账号创建，需提供 App 内删除入口及外部可操作的账号/数据删除渠道。页面删除锚点可作为外部说明入口；联系邮箱已填入，仍需落实接收、验证和删除处理流程。不能仅因为用了 PGS 就武断认定有或没有独立 App 账号。[Google User Data](https://support.google.com/googleplay/android-developer/answer/10144311?hl=en)、[账号删除说明](https://support.google.com/googleplay/android-developer/answer/13327111?hl=en)。
- **Apple**：App Store Connect 隐私资料、隐私标签与 App 内披露要反映真实行为。提供账号创建时要有符合规则的 App 内删除流程；普通游戏不能仅靠要求用户发邮件代替。当前用户协议通过引用保留 Apple 标准 EULA，适合未在 App Store Connect 配置自定义 EULA 的情形；不要直接将此网页当作已满足 Apple 全部最低条款的自定义 EULA 上传。如果要改成自定义 EULA，需另行补齐完整最低条款及开发者地址、电话、邮箱。[App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)、[账号删除](https://developer.apple.com/help/app-review/guideline-reference/5-1-1-account-deletion/)、[标准及自定义 EULA](https://developer.apple.com/help/app-store-connect/manage-app-information/provide-a-custom-license-agreement/)、[自定义 EULA 最低条款](https://www.apple.com/legal/internet-services/itunes/dev/minterms/)。
- **华为海外 AppGallery**：使用英文独立隐私页和用户协议页，开发者身份与商店资料一致，核对当前海外发行规则、实际 HMS Kit 和广告 SDK 披露。华为部分文档为动态页面，本次未能完整抓取海外审核指南正文；上线时仍需在开发者后台检查当前版本，不能据此声称已获得商店合规认证。[AppGallery Review Guidelines](https://developer.huawei.com/consumer/en/doc/distribution/app/30202)、[Policy Center](https://developer.huawei.com/consumer/en/policy-center/)。

政策文字已覆盖已知场景，无法单凭通用网页保证所有市场的法律合规或商店审核通过；最终应与实际发行包、后台设置和目标市场一致。

## SDK 与平台官方资料

网页 SDK 表内有对应的官方链接。额外核对入口：

- [Firebase 隐私与安全](https://firebase.google.com/support/privacy)：仅声明已确认的 Analytics，不因为出现 Firebase 就假设使用了 Authentication、Crashlytics 等其他服务。
- [GameAnalytics Developer Policy](https://www.gameanalytics.com/trust/privacy-faq)：涵盖玩家同意及开发者责任；面向开发者账户的 Privacy Notice 不等同于游戏玩家数据披露。
- [TopOn Advertising Services Privacy Policy](https://www.toponad.net/en/privacy-policy)：其支持的整个广告源目录不等于本公司的启用清单。
- [Unity 玩家隐私政策](https://unity.com/legal/game-player-and-app-user-privacy-policy)、[Google 广告及合作方数据说明](https://policies.google.com/technologies/partner-sites?hl=en)。
- [HMS Core Privacy Statement](https://developer.huawei.com/consumer/en/doc/hmscore-common-Guides/privacy-0000001261262707)：包含具体 Kit 的隐私声明入口。华为 SDK 的数据范围随版本、地区和权限而变；应核对海外所用版本，不能直接套用中国大陆 Ads SDK 的全部字段。
- [Google PGS 数据披露](https://developer.android.com/games/pgs/data-collection)、[Game Center 隐私](https://www.apple.com/legal/privacy/data/en/game-center/)、[HUAWEI ID 隐私](https://consumer.huawei.com/minisite/cloudservice/id/common/b0/latest/privacy-statement.htm)。

本次参考资料核对日期：2026-11-02。

## 本次验证

- 两页 HTML 标签嵌套、唯一主标题、所有本地文件链接及页内锚点检查通过。
- 已用浏览器检查 390px 手机与 1280px 电脑布局：页面无整体横向溢出，SDK 宽表限制在独立滚动容器中。
- 已实际点击协议互链及 SDK 目录跳转；两页不含脚本或外部加载资源。
- 尚未部署公网；未审计游戏安装包、SDK 控制台配置或实际数据删除接口。外部官方链接已按查到的地址列入，部分华为动态文档无法完整抓取，仍需在目标地区环境复核。
