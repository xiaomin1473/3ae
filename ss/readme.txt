目前完成情况：
    1.APP首页照着IOS端重写了。
    2.分类下的商品详情页已经完成了。
    3.个人中心的我的订单静态页面，已经完成了1.0的二级页。现在IOS端上线2.0了得重写。
    4.个人中心的左上角设置二级页，完成。
    5.页面逻辑、公共样式、静态资源整理的有点乱了。
    6.那边写的几个页面用的插件有点儿多，移除了一部分。



issue：
    原因：两个人的代码比较难以维护，新写的代码也有很多的bug，以前写过的一些代码块儿复用率低改了很长时间
        （未解决） 1.首页轮播bug未修复
        （未解决） 2.首页图片和三个一级页的静态资源冲突
        （未解决） 3.商品页顶部轮播未写
        （未解决） 4.订单模块页面全面升级，得进行迭代
        （未解决） 5.局部css样式难以维护了，公共样式，进行UI框架解耦
        （未解决） 6.二级页和三级页还有好多没有写



资源：

    后台接口： https://www.aiyuemall.com/uploads/apiword/




工作日程安排：

    9月12日
            (*) 1. 熟悉整个ios端APP的整个产品逻辑。
            (*) 2. 图片管理分类。（从小郭那儿拿的图片文件）
                3. 熟悉了后台的接口条目，并进行了整理。
            (*) 4. 重写webAPP端的首页。
       （可选择）5. 构思整个APP的页面路由规则和页面切换方式（数据传输方式，过渡动画，文档目录结构）。

    9月13日
            (*) 1. 制定日程安排readme.txt。
                2. 进行APP目录架构。
            (*) 3. 列表页，购物车，个人中心，进行分支整理。
       （可选择）4. 实现一些页面内部的简单功能。
            (*) 5. 构思明天近60个静态页面的组件实现方式。
                6. 选择一些内容繁杂的页面提前做。

    9月14日
            (*) 1. 3.0详情页之前外包出去了，中午之前必出。
            (*) 2. 整理60个静态页面，并分类打包，写公共组件。
            (*) 3. 尽量把内容庞杂和组件状态繁杂的公共区块写出来。



    （原计划）9月14日
                     1. 实现近60个页面的静态实现。
            （可选择）2. 选择每个组件的状态规则和实现方式。
                     3. 


    9月15日
            (*) 1. 对整个App目录进行了整理，分类打包（上午）
            (*) 2. 下午把整理出来的子模块进行静态页面实现，不写功能。
            (*) 3. 进行页面路由逻辑链接。
       （可选择）4. 制定前端路由规则。



    （原计划）9月15日
                    (*) 1. 把剩下的页面在下午15点之前出来。误差尽量控制在半小时之内。
                    (*) 2. 对已完成的条目进行简单的代码审查。
                    (*) 3. 进行简单的模拟环境测试。


    （原计划）9月15日
                (*)  1. 任务整理，并对已完成的条目进行复盘，查漏补缺。
            （可选择）2. 页面兼容性测试。
            （可选择）3. 整理未完成条目。
                     4. 对这周APP任务进行总结归纳。



架构日程安排：

    9月13日 APP目录结构如下：

            applications            页面目录
                index                   首页目录
                list                    分类列表
                    css                         局部css样式     (未整理)
                    js                          局部脚本        (未整理)
                    images                      (三方文件名)    (未整理)
                    index.html                  模块首页        (未整理)
                shopcart                购物车
                    css                         局部css样式     (未整理)
                    js                          局部脚本        (未整理)
                    images                      (三方文件名)    (未整理)
                    index.html                  模块首页        (未整理)
                user                    用户中心
                    css                         局部css样式     (未整理)
                    js                          局部脚本        (未整理)
                    images                      (三方文件名)    (未整理)
                    index.html                  模块首页        (未整理)
            css                     文件夹（空）公共样式
            detail                  微信发来的图
            img                     公共商城图片
            js                      脚本
            static                  静态资源
            index.html              首页加载

        issue:
            原因：首页和其他三个一级页是两个人写的
                （未解决） 1.首页轮播bug未修复
                （未解决） 2.首页图片和三个一级页的静态资源冲突



    9月14日 APP目录结构如下：

            applications           应用
                index                   首页
                list                    分类列表
                shopcart                购物车
                user                    用户中心
                    compenents                  局部组件目录
                        alert                       弹出框
                            confire                         确认
                            cancel                          取消
                    function                    局部功能模块
                        user                        用户功能模块
                        order                       订单功能模块
                        security                    安全功能模块
                    css                         局部css样式     (未整理)
                    js                          局部脚本        (未整理)
                    images                      (三方文件名)    (未整理)
                    index.html                  模块首页        (未整理)
            css                     全局静态样式
            detail                  微信发来的图
            img                     公共商城图片
            js                      脚本
            static                  静态资源
            index.html              首页加载
            readme.txt              文档

        issue：
            原因：首页和其他三个一级页是两个人写的
                （未解决） 1.首页轮播bug未修复
                （未解决） 2.首页图片和三个一级页的静态资源冲突
                （未解决） 3.商品页顶部轮播未写



    9月15日 APP目录结构如下：

            applications            应用
                index                   首页
                list                    分类列表
                shopcart                购物车
                user                    用户中心
                    settings                    设置
                    order                       订单
                    security                    安全验证
                    account                     账户
                    index
                        css                         局部css样式     (未整理)
                        js                          局部脚本        (未整理)
                        images                      (三方文件名)    (未整理)
                        index.html                  模块首页        (未整理)
            compenents              组件目录
                alert                       弹出框
                    confire                         确认
                    cancel                          取消
            detail                  微信发来的图
            lib                     三方类库
            common                  公共样式
            static                  静态资源
                themes                  全局主题资源包
                css                     全局静态样式
                img                     公共商城图片
                js                      脚本
            index.html              移动端首页
            readme.txt              文档



        issue：
            原因：首页和其他三个一级页是两个人写的
                （未解决） 1.首页轮播bug未修复
                （未解决） 2.首页图片和三个一级页的静态资源冲突
                （未解决） 3.商品页顶部轮播未写
                （未解决） 4.订单模块页面全面升级，得进行迭代
                （未解决） 5.局部css样式难以维护了，公共样式，进行UI框架解耦
                （未解决） 6.二级页和三级页还有好多没有写




路由规则:(待定，先用TP5的模板引擎规则吧，可能后期比较好耦合)


    /m/index.html                            m.aiyuemall.com/index.html
    /m/applications/index/                   m.aiyuemall.com/index.html
    /m/applications/user/index/              m.aiyuemall.com/user.html
    /m/applications/user/order/index/        m.aiyuemall.com/order.html




注:
    1.只是静态页面跳转，暂时不考虑添加逻辑js,页面暂时使用相对路径，绝对路径和全局资源变量待定。

    2.可以很方便地做成单页APP。

    3.vuejs在PC端和部分移动场景不是很友好，刚起步的框架迭代速度很快，不是太适合用在频繁更新的场景，这边打算模仿vue和TP5写原生es5的前端框架。



小技巧:（可能对性能有影响，没测试）
    /m/index.html 使用embed标签去隐藏地址栏的路由显示(F12开发者工具粘网址还是会显示路由)

    //移动端有问题    <embed src="applactions\index\index\index.html"  width="100wh" height="100vh"> wh,vh 窗口显示单位————100vh:1当前视图窗口高度
    
    <embed src="applactions\index\index\index.html"  width="100%" height="100%">

