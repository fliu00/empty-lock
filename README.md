# 功能介绍
本库的作用是为了防止yarn.lock或者package.lock文件被删除，在yarn的时候通过postinstall脚本报错提醒开发者不能删除lock文件，需要使用GitLab的lock文件。

此库需要添加到devDependencies下。

# 版本1.0.0 
此版本无任何功能。

# 版本1.0.X
> 1.0.0版本只添加了postinstall脚本，只要安装此版本则报错提醒。

# 步骤
1. 安装版本empty-lock@1.0.0到项目内
2. 把package.json中"empty-lock": "1.0.0", 改为"empty-lock": "^1.0.0"
3. 把yarn.lock或者package.lock中empty-lock@1.0.0改为empty-lock@^1.0.0

现在只要删除yarn.lock或者package.lock，通过yarn会拉去1.0.X版本，通过报错提醒安装失败警示开发者不能删除lock文件。
