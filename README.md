# C 语言训练营 Unit 0 — C Primer

> 零基础入门热身——通过 5 个最小可运行程序，掌握"编辑 - 编译 - 运行"全流程，建立变量、表达式、控制流的基本心智模型。

## 📚 练习题列表

1. [**01_simplest_c_program** - 最简单的 C 程序](./exercises/01_simplest_c_program/)
2. [**02_hello_world_printf** - 打印输出](./exercises/02_hello_world_printf/)
3. [**03_loop_counting** - 循环打印](./exercises/03_loop_counting/)
4. [**04_odd_or_even** - 判断奇偶](./exercises/04_odd_or_even/)
5. [**05_sum_1_to_100** - 从 1 加到 100 求和](./exercises/05_sum_1_to_100/)

## 前置条件

- 您必须报名 [C 语言训练营](https://opencamp.ai/C/camp/2026?lang=zh_CN)

  ![](resource/c.jpg)

- 您必须在训练营个人中心完成 CNB 账号绑定

  ![](resource/bangding.jpg)

## 操作流程

1. Fork 本仓库，解锁作业副本。
2. 在您 Fork 的仓库中点击 **云原生开发** 按钮进入开发环境。
3. 根据文档完成 5 个 lesson 中的练习题（共 9 道小题）。
4. 完成后提交代码到 main 分支，并创建合并请求。

   ![](resource/pr.png)

5. 在 PR 页面查看评分结果（可多次提交，每次提交都会触发评分，以最高分为准）。

   ![](resource/pingce.png)

6. 如果通过，则可以在 OpenCamp 的晋级榜单上看到自己的成绩。

   ![](resource/bangdan.jpg)

## 云原生开发 / 本地开发

### 🛠️ 系统要求

- GCC 编译器
- Python 3.11+
- （推荐）安装 [uv](https://docs.astral.sh/uv/) 用于运行 clings

```bash
# Ubuntu/Debian
sudo apt-get update && sudo apt-get install -y gcc python3
# 安装 uv (推荐)
curl -LsSf https://astral.sh/uv/install.sh | sh

# macOS (Homebrew)
brew install gcc uv
```

### 安装 clings

```bash
# 方式 1: uvx (推荐，无需安装，隔离运行)
uvx clings init unit0
uvx clings

# 方式 2: pipx (隔离安装到独立环境)
pipx install clings

# 方式 3: pip + 虚拟环境
python3 -m venv .venv && source .venv/bin/activate
pip install clings
```

> **注意**: Ubuntu 23.04+ / Python 3.11+ 禁止直接 `pip install` 到系统环境。
> 请使用上述 uvx / pipx / venv 方式，避免 `--break-system-packages`。

### 🚀 快速开始

```bash
# 1. 初始化练习 (如果还没有 exercises/ 目录)
clings init unit0

# 2. 进入交互式 watch 模式 (保存即验证)
clings

# 3. 或者查看练习列表
clings list

# 4. 查看当前题目提示
clings hint

# 5. 查看当前得分
clings score unit0
```

### 完成练习的步骤

1. **查看列表**: `clings list` 查看所有练习和进度
2. **阅读题目**: 进入 `exercises/01_simplest_c_program/` 查看 README.md 和 `.c` 文件
3. **编辑代码**: 根据注释提示补全 `.c` 文件中的代码
4. **自动验证**: `clings` watch 模式会在保存时自动编译和验证
5. **查看提示**: 卡住时运行 `clings hint` 获取帮助
6. **下一题**: 通过后按 `n` 自动跳到下一题

### 命令参考

```bash
clings                    # 交互式 watch 模式 (默认)
clings list               # 列出练习 + ✔/• 进度状态
clings hint [exercise]    # 查看提示
clings run [exercise]     # 运行单个练习
clings check unit0        # 批量验证所有题目
clings score unit0        # 打分 (输出 JSON 报告)
clings reset <exercise>   # 重置练习文件
clings doctor             # 检查环境
clings -v                 # 显示版本号
```

## 📁 项目结构

```
Unit-0-C-Primer/
├── exercises/                  # 练习题源码
│   ├── 01_simplest_c_program/  # Lesson 1: main 函数与 return
│   │   ├── README.md           # 课程讲义
│   │   ├── exercises.toml      # 练习元数据 + 测试用例
│   │   ├── 01a_return_zero.c   # 练习题 (补全代码)
│   │   └── 01b_return_expression.c
│   ├── 02_hello_world_printf/  # Lesson 2: printf 与格式化
│   ├── 03_loop_counting/       # Lesson 3: while/for 循环
│   ├── 04_odd_or_even/         # Lesson 4: if-else 条件分支
│   └── 05_sum_1_to_100/        # Lesson 5: 循环累加与 continue
├── clings.toml                 # Unit 配置
├── .cnb.yml                    # CI 打分 + 云开发环境配置
├── Dockerfile.ci               # CI 打分环境
├── .ide/Dockerfile             # 云开发环境 (code-server)
└── README.md                   # 本文件
```

## 🔧 故障排除

1. **编译错误** — 仔细阅读编译器报错信息，检查语法 (分号、花括号、返回类型)
2. **输出不匹配** — 注意换行符 `\n`、空格、大小写是否与期望输出完全一致
3. **环境问题** — 运行 `clings doctor` 检查 gcc 和 Python 是否就绪

## 📄 许可证

MIT

---

**Happy Coding! 🚀**
