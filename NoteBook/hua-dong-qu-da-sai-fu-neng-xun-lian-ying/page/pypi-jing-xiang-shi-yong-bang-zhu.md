# PyPI 镜像使用帮助

PyPI 镜像在每次同步成功后间隔 5 分钟同步一次。

## pip

### 临时使用

```
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple some-package
```

注意，`simple` 不能少, 是 `https` 而不是 `http`

### 设为默认

升级 pip 到最新的版本 (>=10.0.0) 后进行配置：

```
python -m pip install --upgrade pip
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```

如果您到 pip 默认源的网络连接较差，临时使用本镜像站来升级 pip：

```
python -m pip install -i https://pypi.tuna.tsinghua.edu.cn/simple --upgrade pip
```

### 配置多个镜像源

如果您想配置多个镜像源平衡负载，可在已经替换 `index-url` 的情况下通过以下方式继续增加源站：

```
pip config set global.extra-index-url "<url1> <url2>..."
```

请自行替换引号内的内容，源地址之间需要有空格

可用的 `pypi` 源列表（校园网联合镜像站）：[https://mirrors.cernet.edu.cn/list/pypi](https://mirrors.cernet.edu.cn/list/pypi)

## PDM

通过如下命令设置默认镜像：

```
pdm config pypi.url https://pypi.tuna.tsinghua.edu.cn/simple
```

## Poetry

通过以下命令设置默认镜像：

```
poetry source add --priority=default mirrors https://pypi.tuna.tsinghua.edu.cn/simple/
```

通过以下命令设置次级镜像：

```
poetry source add --priority=secondary mirrors https://pypi.tuna.tsinghua.edu.cn/simple/
```
