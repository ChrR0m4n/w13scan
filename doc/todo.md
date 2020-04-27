
- [x] 指纹识别结构框架
- [x] 设立插件等级概念，等级越高检测一个目标就会发送越多payload，例如等级1 发送0~3,等级2发送4～10，等级3发送10～30，在插件中根据环境情况使用这些等级来使用更多的payload检测。
- [x] 命令行加入参数 插件等级
- [x] 输出模块重构
- [x] 增加反连平台
- [x] 基于语义的xss漏洞扫描
- [x] 基于语义的jsonp敏感信息
- [x] net xss 语义识别
- [ ] sql注入
- [x] loader模块完善
- [x] 对uri头进行探测
- [x] 对post json的处理
- [x] log 颜色
- [x] json导出 
- [x] html导出
    - html报告模仿参考
        - https://phtracker.herokuapp.com/productsList
    - html tag问题 编译与调试不一致问题
    - 搭建测试靶机
- [ ] 识别更多参数
    - [x] js html语义识别更多参数
    - [ ] -u
    - [ ] -f
    - [ ] -r
- [ ] 整理完善命令行参数
- [ ] ini配置文件
- [ ] 完善readme


## Useage

- w13scan主动扫描(单个url或多个url)
- w13scan只用指纹识别(单个url或多个url)
- w13scan被动扫描
- w13scan反连平台
- w13scan专用burpsuite模块
- w13scan漏洞扫描api接口
- crawlergo调用w13scan

- w13scan保存json,html例子
- w13scan webui

## Test Params
```
/?q=1
/?q=1'
/?q=1"
/?q=[1]
/?q[]=1
/?q=1`
/?q=1\
/?q=1/*'*/
/?q=1/*!1111'*/
/?q=1'||'asd'||'   <== concat string
/?q=1' or '1'='1
/?q=1 or 1=1
/?q='or''='
```