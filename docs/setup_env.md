# set environment

## install pip

* download pip script && install pip

```bash
curl -O https://bootstrap.pypa.io/get-pip.py
python3 get-pip.py --user
```

* export path

```bash
# python ver: 3.7, shell: zshell
echo 'export PATH="$HOME/Library/Python/3.7/bin:$PATH"' >> ~/.zprofile
source ~/.zprofile
```

* refrence

```bash
# 出力は、実際のプログラムではなくシンボリックリンクへのパスになる場合があります。ls -al を実行して、その参照先を確認します
ls -al /usr/local/bin/python3

# ex) >> /usr/local/bin/python3 -> ../Cellar/python/3.7.5/bin/python3
```

## install aws-cli version 1

* install aws-cli

```bash
pip3 install awscli --upgrade --user
```

* check aws-cli installed

```bash
aws --version
```

* export path(Set path `.zshrc` or `.zprofile`)

```bash
echo 'export PATH="~/.local/bin:$PATH"' >> ~/.zprofile
source ~/.zprofile
```
