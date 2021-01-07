### 代码数量的统计

## 依赖环境

```
python2.7+
```

## 使用说明

```shell
# clone本项目到本地
git clone https://github.com/wangfpp/code_statistics
# cd到项目目录
cd work/project_name
# 拷贝统计代码到项目目录
cp ../code_clone_path/gitlog_prety.py ./
# 执行代码
python ./gitlog_prety.py 2020-12-20 
# 或者
python ./gitlog_prety.py


# 或者直接用相对或绝对目录执行
python ../github/code_clone_path/gitlog_prety.py

```

## 已经完成的功能和特性

1. 不指定日期统计当前年的1月1号到当前时间的记录
2. 指定日期则从指定日起开始查询记录
3. 兼容py2和py3
```python
# 主要是str和bytes的转换处理问题
   def py2py3(self, str):
        py_verison = sys.version_info.major
        if py_verison > 2:
            str = self.str2bytes(str)
        return str

    def str2bytes(self, str):
        return str.encode(encoding='utf-8')
```
4. Terminal彩色输出　信息标识
5. 无任何第三方依赖
