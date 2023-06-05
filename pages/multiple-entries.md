# 多个入口点

你可以将 slides.md 分割成多个文件，并可以通过src 按照需求组织它们。

#### `slides.md`

```markdown
# Page 1

这是page1 第二页引入了subpage2.md

---
src: subpage2.md
---
```

<br>

#### `subpage.md`

```markdown
# Page 2

这是page2的内容
```

[Learn more](https://sli.dev/guide/syntax.html#multiple-entries)
