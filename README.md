# ownership

**追踪一次输出里每个结论的责任人。**

`ownership` —— 沿决策链标出每个结论由谁产出、依据什么，标出无人负责的环节

- 零依赖，Python 3.10+ 标准库即可运行
- 单文件，`ownership.py` 拷走就能用
- 不联网、不写文件

<!-- ipos:install -->
## 安装

零依赖，Python 3.10+ 即可：

```bash
pip install karuna632-ownership
```

装完直接用命令名调用：

```bash
ownership --help
```

也可以不用安装，直接把 `ownership.py` 拷走用——它只依赖标准库。

## 为什么需要它

重点是标出「没人认领」的结论，而不是给已有结论补标签

它遵守下面几条自己定的规矩：

1. **只报告能定位到具体位置的结论**，不做语义猜测。
2. **规则表公开**，每条命中都能对应到 智能体责任归属 领域的一条明示规则。
3. **输入为空或格式不对时明确报错**，不静默返回空结果。

## 用法

```bash
python ownership.py --file input.txt
python ownership.py --text "示例内容"
python ownership.py --file input.txt --json
```

加 `--json` 可以拿到机器可读的结果，便于接到流水线里。

## 已知局限

- 计数按字面 token 统计，不做词形还原。
- 只报告分布，不判断该保留哪些。

## 跑测试

```bash
python test_ownership.py
```

测试用独立的断言与临时数据，不污染工作目录。

## 来源与参考

- Python 标准库文档：<https://docs.python.org/3/>
- GitHub 仓库：<https://github.com/karuna632/ownership>

---

## 关于作者

karuna632 做智能体责任归属相关的问题。这个工具先替你回答一个具体问题，再谈别的。

- 个人主页：<https://karuna632.github.io>
- 仓库：<https://github.com/karuna632/ownership>

## 许可

MIT，见 [LICENSE](LICENSE)。
