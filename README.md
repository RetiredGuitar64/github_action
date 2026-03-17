## github actions分为很多个小步骤

当在项目里写有 .github/workflows/*.yml 的时候, 这些就会被解析为workflow

### workflow
- 每一个.yml就是一个workflow, workflow包含了他触发所需要的event, 还有这个workflow会运行什么jobs, 等等所有内容

### Event
- 每个workflow可以有单个或多个workflow去trigger, 也可以手动触发

### Jobs
- workflow中包含很多个jobs, 相当于是要做的工作, 目标, 可以是 init环境,跑test, 或者deploy, 都是个job
- 每一个job都可以跑在一个单独的runner, 就是一个真机环境, 或者容器

### Steps
- 每个job又由很多step构成,比如执行shell命令, 安装软件环境
- 也可以直接use其他人已经打包好的action

### Action
- 这个action和github actions 还不是一个概念
- 这个action, 是别人已经打包好的操作, 可以直接在step里面使用,相当于别人直接打包好的小步骤,直接使用

### Runners
- 这个就是运行job时候的环境, github提供ubunutu, windows和mac
- 也可以用自己的runner
