# 贡献指南

欢迎贡献!本 Wiki 由 ECUST Origin 全队共同维护。

## 贡献流程

1. **Fork** 本仓库到自己的 GitHub 账号。
2. 在自己的 Fork 上创建新分支:
   ```bash
   git checkout -b docs/<组别>/<简述>
   # 例如: docs/mechanical/chassis-overview
   ```
3. 在 `docs/<组别>/` 下新增或修改 Markdown 文件。
4. 本地预览:
   ```bash
   pip install mkdocs-material
   mkdocs serve
   # 浏览器打开 http://localhost:8000
   ```
5. 提交 Pull Request,标题格式:
   ```
   [docs/<组别>] 简述改动
   # 例如: [docs/mechanical] 新增底盘设计总览
   ```
6. 等对应组别负责人 Review 后合并。

## 文件命名

- 全部小写,单词用 `-` 连接:`motion-control.md`
- 索引页固定为 `index.md`
- 避免空格、中文、特殊字符

## Markdown 写作规范

### 标题

- 每个文档顶部从 `H1` 开始(MkDocs 会自动用文件名作为 H1)
- 标题之间至少空一行
- 标题层级不要跳级

### 链接

- 站内链接用相对路径:
  ```markdown
  详见 [底盘设计](chassis.md)
  ```
- 站外链接可加 `{target="_blank"}` 让浏览器新标签页打开

### 图片

- 放在 `docs/assets/<组别>/` 下
- 用相对路径引用:
  ```markdown
  ![底盘爆炸图](assets/mechanical/chassis-explode.png)
  ```
- 提交 PR 时图片与文档同 PR,保持同步

### 代码

使用三个反引号并标注语言:

\`\`\`python
def hello():
    print("hello")
\`\`\`

### 警告框

Material 主题支持:

\`\`\`
!!! note "提示"
    正文内容
!!! warning "注意"
    正文内容
\`\`\`

### 折叠块

\`\`\`
??? question "常见问题?"
    答案写在这里
\`\`\`

## 目录约定

```
docs/
├── index.md             # 全站首页
├── getting-started.md   # 新人入门
├── glossary.md          # 术语表
├── resources.md         # 资源链接
├── <组别>/
│   ├── index.md         # 组别概览
│   └── *.md             # 具体主题
└── assets/<组别>/       # 图片资源
```

## 引用与转载

- 引用第三方资料必须注明出处,放在段末或参考资料小节。
- 大段转载需获得原作者许可。
- 本 Wiki 内容默认以 [CC BY-SA 4.0](LICENSE) 协议发布,贡献即视为同意该协议。

## 负责人

每个组别需指定一名 **文档负责人**(在 `docs/<组别>/index.md` 顶部填入 GitHub ID 与联系方式占位),负责:
- 审核本组别 PR
- 季度内容审计与过期内容清理
- 维护本组别术语表条目

## 提问与反馈

- 文档问题: 在 GitHub 上提 Issue,标签选 `documentation`
- 流程问题: 联系战队文档负责人
