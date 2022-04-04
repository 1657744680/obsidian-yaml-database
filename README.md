版本升级注意事项！！
- [升级注意事项！！](https://github.com/1657744680/obsidian-yaml-bulk-edit/issues/12)

> **此插件涉及到批量修改文档内容，所以使用前请进行数据备份！！使用此插件导致的任何数据丢失本人概不负责。**
>
> 请在使用前备份数据！！
>
> 请在使用前备份数据！！
>
> 请在使用前备份数据！！
>
> 当您误操作数据后，请使用命令`YAML属性批量管理: 还原上一步操作`来还原操作。

# 目录

* [obsidian\-yaml\-bulk\-edit 批量编辑yaml](#obsidian-yaml-bulk-edit-批量编辑yaml)
* [安装](#安装)
* [使用方法](#使用方法)
  * [面板批量更改YAML](#面板批量更改yaml)
  * [yaml 表格操作](#yaml-表格操作)
    * [创建表格](#创建表格)
    * [操作区域](#操作区域)
    * [表格区域](#表格区域)
    * [相关设置项](#相关设置项)
  * [筛选条件说明](#筛选条件说明)
* [未来规划](#未来规划)
  * [表格编辑](#表格编辑)
  * [批量编辑](#批量编辑)
* [版本更新日志](#版本更新日志)

# obsidian-yaml-bulk-edit 批量编辑yaml

> **此插件涉及到批量修改文档内容，所以使用前请进行数据备份！！使用此插件导致的任何数据丢失本人概不负责。**
>
> 请在使用前备份数据！！
>
> 请在使用前备份数据！！
>
> 请在使用前备份数据！！
>
> 当您误操作数据后，请使用命令`YAML属性批量管理: 还原上一步操作`来还原操作。

> 此插件适用的人群：
>
> - 使用obsidian并懂得yaml的用户
> - 想体验类似于notion的database的用户（当然差很远的了😄）
>
> 若您想要使用本插件，强烈推荐您阅读本插件的[筛选条件说明](#筛选条件说明)，阅读这个有利于您采取合理的措施以使得该插件和文件配合。

> 我不太会CSS，表格样式的代码是QQ群的`Cuman`老哥按我的要求帮忙提供的，感谢！！

插件的Github链接：https://github.com/1657744680/obsidian-yaml-bulk-edit

插件视频演示：https://www.bilibili.com/video/BV1wr4y1p7qz/

这个插件是即可以批量编辑obsidian中文档的yaml，也可以像notion那样表格编辑的形式来编辑某个文档的某个yaml。

- 批量编辑YAML： 
<img src="https://user-images.githubusercontent.com/39726621/161392925-2de339c6-3c65-4faf-a196-832774f80e61.png" alt="image" width="500px" />

- 表格编辑YAML：
<img src="https://user-images.githubusercontent.com/39726621/161393772-d50e0043-299a-45da-9cbd-15455827f30c.png" alt="image" width="500px" />


# 安装

手动从release页面下载安装，或使用Brat进行安装

# 使用方法

您有两种方式操作yaml

1. 命令：面板**批量**更改YAML
   （包括增删改属性名、改属性值、删除YAML、清理空值一系列批量操作）
   1. 输入条件筛选文档
   2. 确认筛选的文档和自己想要修改的目标文档一致
   3. 选择操作
   4. 输入参数
   5. 修改完成
2. 命令：还原上一步操作
   （可以还原上一步对yaml进行的操作，可以还原批量操作和表格操作，但是操作只会被记录50条）
   1. `还原上一步操作`只对以下两种操作生效：
      - yaml表格修改属性值
      - 面板批量更改YAML
   2. 对于“yaml表格修改文件名称”、“yaml表格新建文档”这2种操作，`还原上一步操作`不能生效。
   
3. 代码块：表格编辑YAML
   （编辑**某个文档的某个属性值**）
   1. 点击`刷新`重新读取缓存刷新表格
   2. 点击`搜索`对当前表格内容进行搜索
   3. 点击`属性`指定显示的属性及顺序，还可以指定属性的名称和数据类型
   4. 点击`↑↓`设置排序条件，支持多条件排序，排序优先级即为条件的顺序
   5. 点击`筛选`筛选文档
   6. 点击`＋`来在当前表格新建文档（右键点击`＋`进入添加文档设置）
   7. 点击表格单元格来改变某个文档的某个属性值
   8. 点击文件名称修改文件名

## 面板批量更改YAML

面板①②③长度过长时均可以上下滑动

1. Ctrl+P调出命令面板，选择命令`YAML属性批量管理: 打开操作面板`
2. 点击命令后进入**面板①**，在这里输入条件以筛选文档，可以添加新的条件（注意：各个条件之间为与关系），输入完成后确定。目前支持以下几种条件：
   1. `yaml`——`包含/不包含`——`属性名`
   2. `yaml属性`——`属性名`——`属性值`
   3. `标签`——`包含/不包含`——`标签名`
   4. `文件名称`——`符合/不符合`——`正则表达式`
   5. `文件路径`——`符合/不符合`——`正则表达式`
   <img src="https://user-images.githubusercontent.com/39726621/161392999-2c20f1bc-04a6-4265-b1fb-416ecf73a9a7.png" alt="image" width="500px" />

3. 点击确定后进入到**面板②**，这里会展示筛选的文档，当您确认文档符合要求后可选择具体操作进行下一步（如果发现显示的文档并不符合您的预期要求，那么您可以进一步选择或者关闭当前面板回到面板①重新设置条件）。可选择的操作有：
   1. `添加新属性`
   2. `修改属性名`
   3. `修改属性值`
   4. `删除属性`
   5. `删除整个YAML`
   6. `清理控制属性`（可能需要多点几下）
   <img src="https://user-images.githubusercontent.com/39726621/161393141-459d1bb8-e466-4cb5-a650-9075a2daf96b.png" alt="image" width="500px" />

4. 点击具体操作后进入到**面板③**，在这里输入值来进行最后一步的操作。请谨慎操作！！确认输入无误后点击确定即可提交。当您误操作数据后，请使用命令YAML属性批量管理: 还原上一步操作来还原操作。
<img src="https://user-images.githubusercontent.com/39726621/160273284-614702eb-bc59-4dfc-937a-3f55a799c1e0.png" alt="image" width="500px" />

5. 到这里就完成批量修改操作了。
6. 您可以使用命令`还原上一步操作`来还原批量操作
7. 批量编辑设置项
   1. `禁止删除和修改的名称属性`：对于十分重要的yaml属性值，为了避免对这些重要的属性值造成误删、误改，可以将他们添加到此。（一行一个属性，多个属性请换行）<img src="https://user-images.githubusercontent.com/39726621/160730853-8372818b-8bcc-4f66-afa7-af71987895fb.png" alt="image" width="500px" />
   2. `忽略的文件或文件夹路径`：输入基于库的路径，路径开头不要加`/`，（一行一个路径，多个路径请换行）<img src="https://user-images.githubusercontent.com/39726621/160730894-f701ee0a-775a-47ad-8ac9-292885251f32.png" alt="image" width="500px" />

## yaml 表格操作

### 创建表格

> 您必须在代码块中以下面的形式填写id！！！
> 若您未填写，那么表格将不会被渲染。

````text
```yamledit
id:在这里填写一个在当前页面所有的yamledit代码块中独一无二id值
```
````

### 操作区域

<img src="https://user-images.githubusercontent.com/39726621/161559118-dacfb970-1a59-4716-971e-58d4c4f18dfc.png" alt="image" width="500px" />

操作区域是指表格的按钮、搜索部分，包括以下内容：

- `刷新`（点击重新读取缓存渲染表格）

- `搜索`（只会对当前表格显示的内容进行搜索，对于checkbox类型的属性需要输入true或false来搜索）

- `属性`（属性批量操作面板、属性显示控制、属性名称控制）

  - 点击`属性`后出现的操作区域中的`批量操作属性`会对当前表格内的文档进行批量操作。
  - 目前支持的类型如下：
    - text（默认类型，可显示所有类型的值）
    - checkbox（选框）
    - date（日期）
    - time（时间）
    - number（数字）
    - img（仅支持在线图片）
    - url

- `排序` `↑↓`（按照指定的排序条件进行排序，支持多条件排序，支持对文件和各属性按asc或desc排序）

  - `排序` `↑↓`的优先级是您输入参数的顺序

- `筛选`（和批量操作筛选文档的条件相同）

  - 详见[筛选条件说明](#筛选条件说明)

- `＋`（添加文档）（`还原上一步操作`不会还原该操作）

  - 右键点击：进行添加的文件位置和文件模板的设置
    （请确保该设置和`筛选`条件配合以生效）
    - 新建文档的位置：若您未对文件位置进行设定，那么新增的文件位置将会位于系统的默认位置
    - 新建文档的内容：
      - 若您指定模板，那么**插件会对模板进行校验并根据筛选条件更改模板YAML**，请注意这一点。
      - 若您未指定文件模板，那么**插件会根据筛选条件对新增的文件进行更改YAML**以使新建的文档能够被当前表格索引。
      - <img src="https://user-images.githubusercontent.com/39726621/161558590-a0f197f3-570e-4337-8e1c-6cb857cc0b8d.png" alt="image" width="500px" />
  - 左键点击：输入文档标题添加文档
    - 输入文档名称，成功新建之后表格会刷新。（若未刷新请手动刷新）
    - <img src="https://user-images.githubusercontent.com/39726621/161559398-32748bac-27b9-4a30-8888-00aa819dbeb7.png" alt="image" width="500px" />


---

其它的注意事项：

- 部分按钮输入参数后需要点击确定才会发生更改，点击取消编辑即可取消更改。若表格未刷新，可自行点击按钮刷新。
- 部分按钮支持多个参数的输入和删除。

### 表格区域

在此处您可以编辑文件名称和文件的yaml属性：

- 文件名称：直接编辑即可（`还原上一步`命令**不对**该操作生效）
- 文件的yaml属性：直接编辑即可（`还原上一步`命令对该操作生效）

> **部分类型**的输入框可能需要您点击一下除该输入框的其它位置，使输入框**失焦**才能够触发更改。

---

其它的注意事项：

2. 当您操作表格的某个单元格且输入改变值时，若该单元格所对应的文档没有该单元格所对应的属性，那么插件会自动为该文档**新建该属性**。
2. 对于多行的yaml属性，当您对它编辑并赋值时，插件会将文档中的它从多行变成单行，但这并不会有什么其它的影响。

### 相关设置项

`隐藏的属性名称`，在这里输入您想要默认隐藏的属性。（一行一个属性，多个属性请换行）
（一般情况下，这个只会在您初次创建表格时会用到。）<img src="https://user-images.githubusercontent.com/39726621/160731246-a43163f1-a0fe-4d6c-aa13-f48dc2295168.png" alt="image" width="500px" />

## 筛选条件说明

每个条件之间是与关系。

| 参数1    | 参数2            | 参数3               | 说明                                         |
| -------- | ---------------- | ------------------- | -------------------------------------------- |
| yaml     | 包含<br />不包含 | 属性名              | `yaml`中`包含/不包含` `属性名`的文档         |
| yaml属性 | 属性名           | 属性值              | `yaml属性`中`属性名`值为`属性值`的文档       |
| 标签     | 包含<br />不包含 | 标签名（不带`#`号） | `包含/不包含` `标签名`的文档                 |
| 文件名称 | 符合<br />不符合 | 正则表达式          | `文件名称` `符合/不符合` `正则表达式` 的文档 |
| 文件路径 | 符合<br />不符合 | 正则表达式          | `文件路径` `符合/不符合` `正则表达式` 的文档 |



# 版本更新日志

## 0.6.0

### 增强

- [x] 文件设置为可编辑，可为文档重命名
- [x] 为yamledit添加按钮`＋`，可用于在指定位置以指定模板创建新文档

## 0.5.3

### 修复

- [x] 修复yamledit点击筛选按钮后，已存在的筛选条件中的参数②被覆盖的bug
- [x] 修复yamledit点击属性按钮后添加属性时只出现一个输入框的bug

### 增强

- [x] yamledit无筛选条件不显示任何文件，设置筛选条件后才显示文件
- [x] 优化了yamledit表格某属性宽度过窄时输入框过大的问题
- [x] 优化了对于checkbox类型属性的排序

## 0.5.2

### 增强

- [x] yamledit代码块prop:部分代码格式重构，如果您使用过yamledit，请删除原本的表格以使插件正常工作！！
- [x] yamledit表格支持设置属性栏宽度

## 0.5.1

### 修复

- [x] 修复一点表格编辑yaml时属性命名的小错误

## 0.5.0

### 修复

- [x] 修复了表格操作筛选文档时属性值中含英文冒号解析条件出错的bug
- [x] 修复了yaml中含有一些特殊符号时的错误，解决措施：插件会自动为对yaml赋值的属性添加英文半角单引号，同时会将您输入的值中的英文半角单引号强制转为英文半角双引号

### 增强

- [x] 还原上一步操作（最多纪录50条操作数据，包括批量操作、表格编辑）
- [x] 增加了对多行属性的编辑方法，目前的方法是删除多行属性值写到单行属性中去
- [x] 为表格增加按键操作
  - [x] 刷新（点击重新读取缓存渲染表格）
  - [x] 搜索（只会对当前表格显示的内容进行搜索，对于checkbox类型的属性需要输入true或false来搜索）
  - [x] 属性（属性批量操作面板、属性显示控制、属性名称控制）
  - [x] 排序`↑↓`（按照指定的排序条件进行排序，支持多条件排序，支持对文件和各属性按asc或desc排序）
  - [x] 筛选（和批量操作筛选文档的条件相同）
- [x] 像notion那样，表格的属性是有类型的（注意，若您的属性值不符合您指定的属性类型，那么该值可能不会被显示！text类型可显示所有属性值）目前支持以下类型：
  - [x] text（默认）
  - [x] checkbox
  - [x] date
  - [x] time
  - [x] number
  - [x] img（仅支持在线图片）
  - [x] url
- [x] table中的td显示和input分开以更好的支持多类型数据

## 0.2.0

### 修复

- [x] 表格CSS与第三方主题冲突的问题 #2

### 增强

- [x] 去除表格编辑YAML时的文件名称的`.md`后缀
- [x] 支持多条件排序！

## 0.1.1

### 修复

- [x] 修复不识别yaml中tags、tag的bug

### 增强

- [x] 将设置项中的禁止删除和修改选项分为2项：①禁止批量操作的属性、②禁止表格操作的属性
- [x] 设置中的操作项均由text改为textarea以方便编写

## 0.1.0

### 增强

- [x] 支持代码块渲染为列表来编辑YAML
  新版本（包括表格编辑YAML功能）功能演示视频：[obsidian批量修改文档yaml属性插件新版本演示（表格编辑YAML！！）](https://www.bilibili.com/video/BV1yu411v7Ej/)
- [x] 设置项中添加选项：表格中隐藏的属性名称
- [x] 面板②增加操作：清理空值属性

## 0.0.3

### 增强

- [x] 支持筛选文档后进一步选择目标文档
- [x] 设置项中添加选项：忽略文件夹

## 0.0.2

### 修复
- [x] 修复`yaml属性`选择属性后搜索选框不显示全部已存在的属性值的问题
- [x] 修复未选择添加功能时自动添加`---`的问题
### 增强
- [x] 为面板③修改删除、修改属性操作的第一个输入框增加候选项
- [x] 面板②增加操作：删除整个yaml

## 0.0.1

视频演示：[obsidian批量修改文档yaml属性插件演示](https://www.bilibili.com/video/BV1pq4y1Y7as/)
