### make的工作流
1. 读入所有Makefile
2. 读入被include其他Makefile
3. 初始化文件中的变量
4. 推导隐晦规则，并分析所有规则
5. 为所有的目标文件创建依赖关系链
6. 根据依赖关系，决定哪些目标要重新生成
7. 执行生成命令

### make使用
#### 默认搜索路径
- /usr/local/bin
- /usr/include

#### 添加搜索路径
- -I
- --include-dir

#### 环境变量MAKEFILES
在这个环境变量中的值会被include
但从这个环境变量中引入的Makefile的目标不会起作用，且出错时不理会
*不建议使用*

### makefile语法
#### 导入其他makefile
include <flename>
#### 忽略出错继续执行
在命令前添加-
