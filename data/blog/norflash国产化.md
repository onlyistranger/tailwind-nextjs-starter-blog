大家好，我是痞子衡，是正经搞技术的痞子。今天痞子衡给大家讲的是**国内外串行NOR Flash厂商官网Cross Reference功能**。

串行 NOR Flash 是一个相对发展稳定的市场，目前全球市场约 90% 的份额被中国的三家厂商（Winbond华邦/MXIC旺宏/GigaDevice兆易创新）占据，另外 10% 份额由众多厂商瓜分（这些厂商里也不乏国际一线大厂）。

我们在做嵌入式产品设计很多时候都需要外挂串行 NOR Flash，比如用于扩大代码 XIP 执行空间，比如存储图片资源或者运行参数等。如果嵌入式产品的出货量大，项目经理可能会选择不止一家 Flash 厂商来供货，这时候我们就需要用到交叉引用（Cross Reference）功能，利用交叉引用功能来找到性能参数相近的两颗 Flash 互相替代。

大部分 Flash 厂商的官网上都做了交叉引用功能，少部分厂商官网暂时还不支持交叉引用，痞子衡今天体验了 15 家 Flash 厂商的官网，对于它们的 Cross Reference 功能做了比较详细的体验：

`国外厂商：     --标准产线：Micron镁光、Infineon英飞凌（收购Spansion）、Renesas瑞萨（收购Adesto）、Microchip微芯（收购SST）   国内厂商：     --大陆地区：GigaDevice兆易创新、ISSI芯成、Boya博雅、Puya普冉、XTX芯天下、XMC武汉新芯、Dosilicon东芯、FudanMicro复旦微     --台湾地区：Winbond华邦、MXIC旺宏、ESMT晶豪   `

### 一、各厂商官网Cross Reference入口

#### 1.1 Winbond华邦

专业做存储器的老牌厂商华邦的 Cross Reference 入口还是比较明显的，直接官网首页固定栏里就能点进去：

> -   入口：https://www.winbond.com/hq/support/documentation/?__locale=en&category=/.categories/resources/cross-reference/
>     

![图片](https://mmbiz.qpic.cn/mmbiz_png/icSsJyL95utZJmLg3qn58SjicMo7VDOPmr6VrPm66eKN9ib6tVicv53XdrgglGYriahibdOx5rZGdFRrwmapbULZCIEg/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

#### 1.2 MXIC旺宏

另一个专业做存储器的老牌厂商旺宏的 Cross Reference 入口风格跟华邦几乎一致：

> -   入口：https://www.macronix.com/en-us/products/Pages/cross-reference-search.aspx
>     

![图片](https://mmbiz.qpic.cn/mmbiz_png/icSsJyL95utZJmLg3qn58SjicMo7VDOPmr6EReGHGqHVw6qMNGFjM4mnAlYXlCzAvMaVFZvw7PCzYRCuNgIsDtKA/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

#### 1.3 GigaDevice兆易创新

兆易创新的 Cross Reference 入口就稍微有点隐蔽了，藏在菜单栏 **Products** 下面，需要仔细找一下。不过也能理解，毕竟存储器不是兆易创新的全部，他们家还有 MCU：

> -   入口：https://www.gigadevice.com/products/cross-reference-search-tool/
>     

![图片](https://mmbiz.qpic.cn/mmbiz_png/icSsJyL95utZJmLg3qn58SjicMo7VDOPmr3oxZic0wWlY5qnXd2hdYJ6HC0R69pV21lOicd919zgibSK7zxTdGSD95Q/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

#### 1.4 Infineon英飞凌

英飞凌的 Cross Reference 入口也比较隐蔽，藏在菜单栏 **Design Support** 下面，英飞凌家的产品类目就更多了，存储器估计只占业务的很小份额：

> -   入口：https://www.infineon.com/cms/en/product/search/cross-reference/
>     

![图片](https://mmbiz.qpic.cn/mmbiz_png/icSsJyL95utZJmLg3qn58SjicMo7VDOPmr1U1ylibmHc42skIFibuxtpWZpeGr0HVkHQgzQDp49nRsFX5YwcIGSEibw/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

#### 1.5 Micron镁光

国际存储器大厂镁光 Cross Reference 入口是最隐蔽的，一级菜单栏 **Support** 里都不能直接找到，还要再点进二级 **Tools and Utilities** 页面里，然后仔细找一番，才能发现专用的 **NOR Cross-Reference Tool** 工具。不熟悉他们家官网的人应该很难找到这个入口：

> -   入口：https://www.micron.com/support/tools-and-utilities/nor-cross-reference-tool
>     

![图片](https://mmbiz.qpic.cn/mmbiz_png/icSsJyL95utZJmLg3qn58SjicMo7VDOPmrSuAUqT8ux9fzE5TxOAtUx78056QTyibkN6tdBe6J1z2fpz8ORia2frbQ/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

#### 1.6 ISSI芯成

芯成的 Cross Reference 入口风格跟华邦和旺宏比较像，但是更进了一步，直接搜索框给你，可以省去一次点击就能得到结果：

> -   入口：https://www.issi.com/WW/PSearch/USPSearch/CrossReference_Search.aspx
>     

![图片](https://mmbiz.qpic.cn/mmbiz_png/icSsJyL95utZJmLg3qn58SjicMo7VDOPmrnl1mJibdSpCY5avh8FNS8r8F4cOgBMYs2EZKrOt9fjpXSqcTwAIpwvg/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

#### 1.7 Renesas瑞萨

瑞萨的 Cross Reference 入口跟英飞凌很像，藏在菜单栏 **Design Resources** 下面，产品类目多了，看来都这样的风格：

> -   入口：https://www.renesas.cn/cn/en/support/cross-reference
>     

![图片](https://mmbiz.qpic.cn/mmbiz_png/icSsJyL95utZJmLg3qn58SjicMo7VDOPmriaJVQg2jDblDprIu9wWiaHx0AzGpIFxSLY799Is1b4e64YIWQ0wWvtsQ/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

#### 1.8 Puya普冉

大陆新锐厂商里只有普冉官网做了 Cross Reference 入口，风格像芯成：

> -   入口：https://www.puyasemi.com/ssckcp/index_28.html
>     

![图片](https://wximg.cccyun.cc/mmbiz_png/icSsJyL95utZJmLg3qn58SjicMo7VDOPmr1ff8e71ic7e7V7PvahCVjso8anicfQlyF1c8jPkh8TmGoPuUYg9h8psQ/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

### 二、各厂商Cross Reference互相支持情况

下面是各厂商交叉引用相互支持情况，痞子衡特意试了列出的全部厂商，选用了各自代表性的 128Mb 产品（比如 W25Q128、MX25L128、GD25Q128、S25FL128、MT25QL128、IS25LP128、AT25SF128）。最终结果其实还挺有趣的（瞄准什么竞争对手，也侧面反映了公司的发展策略，需要你细品）：

`1. 作为NOR市场份额前三的 Winbond华邦 和 GigaDevice兆易创新 把交叉引用功能覆盖得最全面。   2. 同样是NOR市场份额前三的 MXIC旺宏 交叉引用里不支持大陆厂商。   3. 全球存储器界的霸主 Micron镁光 交叉引用里不支持除台湾地区之外的亚洲厂商。   4. 欧洲汽车芯片元老 Infineon英飞凌 交叉引用里不支持所有的亚洲厂商。   5. 日本汽车芯片霸主 Renesas瑞萨 交叉引用里不支持 Infineon英飞凌（来自汽车领域的恩怨？）。`

![图片](https://mmbiz.qpic.cn/mmbiz_png/icSsJyL95utZJmLg3qn58SjicMo7VDOPmrC8ZcjrAgn3ZVDm7e4rD5NUMl2u7A2hdgYAGsRYerxlpphKVoCurBnA/640?wx_fmt=png&tp=wxpic&wxfrom=5&wx_lazy=1&wx_co=1)

至此，国内外串行NOR Flash厂商官网Cross Reference功能痞子衡便介绍完毕了，掌声在哪里~~~