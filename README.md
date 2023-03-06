# vscode 代码片段插件


## 使用步骤

### 1. 安装依赖
```
npm install
```

### 2. 维护插件信息
package.json
``` json 
{
  // displayName 插件名称，建议自己起名修改
  "displayName": "code-snippets 名称",
  // description 插件描述
  "description": "code-snippets 插件描述",
}
```

### 3. 维护代码片段
snippets/snippets.json    
添加自己常用的一些代码片段

``` json
{
  "xxx-button 按钮": {
    "prefix": "xxx-button",
    "body": [
      "<xxx-button type=\"${1|primary,text,info,success,warning,danger|}\"",
      "            auth=\"$2\"",
      "            @click=\"$3\">${4}</xxx-button>"
    ],
    "description": "xxx UI <xxx-button>"
  }
}
```


### 4. 打包插件
```
npm run build
```
打包成功后根目录就多了个 .vsix文件，就是vscode的插件安装包