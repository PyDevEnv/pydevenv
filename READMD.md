# Python 开发指南

## 多版本
* Pyenv
  * 安装
    ```shell
    $ curl -L https://raw.githubusercontent.com/pyenv/pyenv-installer/master/bin/pyenv-installer | bash
    ```
  * 参考
    * [Pyenv -- Simple Python version management](https://github.com/pyenv/pyenv)
    * [Pyenv-installer -- This tool is used to install `pyenv` and friends.](https://github.com/pyenv/pyenv-installer)

* Python
  * 安裝
    ```shell
    pyenv install 2.6.x
    pyenv install 2.7.x
    pyenv install 3.3.x
    pyenv install 3.4.x
    pyenv install 3.5.x
    pyenv install 3.6.x
    pyenv install 3.7.x

    pyenv global system 2.6.x 2.7.x 3.3.x 3.4.x 3.5.x 3.6.x 3.7.x
    ```
  * 安装
    * [Using tox with pyenv #92](https://github.com/pyenv/pyenv/issues/92#issuecomment-31157539)
    * [Choosing the Python Version](https://github.com/pyenv/pyenv#choosing-the-python-version)

## 虚拟环境
* Virtualenv
  * 安装
    ```shell
    pip install virtualenv
    ```
  * 使用
    ```bash
    cd ~/env
    virtualenv xxx
    source ~/env/xxx/bin/activate
    ```
  * 参考
    * [Virtualenv -- Virtual Python Environment builder](https://github.com/pypa/virtualenv)

* Autoenv
  * 参考
    * [Autoenv -- Directory-based Environments](https://github.com/kennethreitz/autoenv)

## 常用库
```
ipdb
ipython
```

## 代码规范
* PEP8
  * 参考
    * [PEP 8 -- Style Guide for Python Code](https://python.org/dev/peps/pep-0008/)

* Pycodestyle
  * 安装
    ```shell
    pip install pycodestyle
    ```
  * 参考
    * [Pycodestyle -- Simple Python style checker in one Python file](https://github.com/PyCQA/pycodestyle)

* Flake8
  * 安装
    ```shell
    pip install flake8
    ```
  * 参考
    * [Flake8 -- a python tool that glues together pep8, pyflakes, mccabe, and third-party plugins to check the style and quality of some python code.](https://github.com/PyCQA/flake8)

## 代码调试
```python
import ipdb;ipdb.set_trace()
```

## 自动化测试
* 多版本
  * 使用 ``Pyenv`` 完成多版本安裝

* Tox
  * 安装
    ```shell
    pip install tox
    ```
  * 配置文件
    ```shell
    tox.ini
    ```
  * 依赖文件
    ```shell
    dev-requirements.txt
    requirements.txt
    ```
  * 执行
    ```shell
    tox
    ```
  * 参考
    * [Tox -- Virtualenv management and test command line tool](https://github.com/tox-dev/tox)

* Pytest
  * 安装
    * Tox 自动安装 ``pytest``、``pytest-cov`` 等
  * 配置文件
    ```shell
    pytest.ini
    ```
  * 执行
    ```shell
    pytest
    ```
  * 参考
    * [Pytest -- The pytest framework makes it easy to write small tests, yet scales to support complex functional testing](https://github.com/pytest-dev/pytest)
    
  * 提示
    ```doc
    您可以使用 ``pytest -s --pdb`` 在测试失败的时候自动进入 pdb 调试
    ```

## 参考链接