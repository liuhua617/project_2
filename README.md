# project_2
​​蒲公英自动化
项目介绍：该项目是一套基于Python+Playwright的UI自动化测试框架封装平台，实现注册,登录,新增项目,新增环境等功能用例转自动化的实现,并且合理使用断言,生成可视化的测试报告；
技术栈：Python+pytest+playwright+Ajax+allure+Jenkins+docker+Linux
项目架构：采用pytest测试框架的规则来维护用例,采用@pytest.mark.parametrize钩子函数维护参数的传递与提取;
采用playwright支持的定位方法,如Selector选择器,get_by_text等，并很好的处理了iframe定位的问题；
基于playwright框架自身特性，灵活使用断言操作，如判断Ajax异步请求与响应结果,注册,登录成功等用例；
通过pytest的fixtures机制实现前置Cookies登录，避免单条用例重复执行登录流程，提高了批量执行的效率；
通过自定义mock数据,伪造请求头,包括url,handler,body等,实现自定义状态码如404,500的报错，方便调试;
基于docker搭建jenkins流水线脚本,集成Git+allure实现自动推送测试报告到钉钉群聊的pipeline模式；
