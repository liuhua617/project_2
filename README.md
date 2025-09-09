# project_2
​​蒲公英自动化
项目介绍：该项目是一个UI自动化框架的封装平台,主要基于Python+PlayWright搭建了接口自动化框架,实现注册,登录,新增项目,新增环境等功能用例转自动化的实现,并且合理使用断言,生成可视化的测试报告；
技术栈：Python+pytest+playwright+Ajax+allure+Jenkins+docker+Linux
项目亮点：
采用pytest测试框架的规则来维护用例,采用@pytest.mark.parametrize钩子函数维护参数的传递与提取;
采用playwright支持的定位方法,如Selector选择器,get_by_text等,并很好的处理了iframe定位的问题;
基于playwright框架自身特性,灵活使用断言操作如判断Ajax异步请求与响应结果,注册,登录成功等用例;
避免每次执行用例都要反复登录,借助pytest的fixtures实现用例前置的cookies登录,提高了批量执行的效率;
通过自定义mock数据,伪造请求头,包括url,handler,body等,实现自定义状态码如404,500的报错方便调试;
基于docker搭建jenkins流水线脚本,集成Git+allure实现自动推送测试报告到钉钉群聊的pipline模式;
