# 黎明导航

**基于 Hugo-Webstack 网址导航网站**

项目基于 https://github.com/oulh/nav/

可以自己 fork 部署以及 pull request

这里介绍 Github Pages 的方法：

1. 导入或 Fork 本项目

2. Github Pages 设置

   ![](https://raw.githubusercontent.com/oulh/nav/main/static/images/gh-pages.jpg)

3. Github Action 设置
   
   如果是导入的：Settings - Actions - General - Allow all actions and reusable workflows
   
   如果是Fork的：Actions - "I understand my workflows, go ahead and enable them"

4. 可自定义编辑的内容：
   
   - 主页面：/data/webstack.yml
   - 子页面：/content/xxx.md
   
   查看构建状态：Actions - All workflows
   
   如何希望提交后不触发构建，只需在 commit 信息中包含关键词：`[skip ci]`或`[no ci]`，包括[]符号。
   
5. 访问页面

   你的站点链接是：https://用户名.github.io/仓库名
   
6. pull request

## 附：webstack.yml

可以复制以下配置，编辑 [webstack.yml](https://github.com/oulh/nav/blob/main/data/webstack.yml) 原有的内容，修改完可以问 gpt 你改的对不对。

title和url是必要属性，其他非必须。

```yaml
---
- taxonomy: 分类名称
  icon: fa-star
  links: 
    - title: 
      url: https://
      logo: 
      description: 
    - title: 
      url: 
      description: 
    - title: 
      url: 

          
- taxonomy: 
  icon: 
  list: 
    - term: 
      links:
        - title: 
          url: 
          description: 
    - term: 
      links:
        - title: 
          url: 
        - title: 
          url: 

- taxonomy: 其他链接
  icon: fa-link
  friend:
    - title: 
      url: 
      description: 
    - title: 
      url: 
      
---
```
