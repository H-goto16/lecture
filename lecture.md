# 2. パスの表記編
## 2.1. 絶対パスと相対パス
+ 絶対パス: ルートディレクトリ（/）から始まるパス

```bash
/home/user/Documents/file.txt
```
+ 相対パス: 現在のディレクトリからの相対的なパス

```bash
./file.txt  # 現在のディレクトリ内のファイル
../file.txt  # 一つ上の階層のファイル
```

## 2.2. パスの重要な記号
+ `.` (ドット): 現在のディレクトリ

+ `..` (二重ドット): 一つ上のディレクトリ

+ `~` (チルダ): ホームディレクトリ（例: /home/user）

1. Linuxコマンド編
1.1. 基本的なコマンド
```
pwd: 現在の作業ディレクトリ（カレントディレクトリ）を表示
```
```bash
pwd
```
+ ls: ディレクトリの内容をリスト表示

```bash
ls
```
+ cd: ディレクトリを移動

```bash
cd /path/to/directory
cd ..  # 一つ上の階層に移動
```
+ cp: ファイルやディレクトリをコピー

```bash
cp source.txt destination.txt
```
+ mv: ファイルやディレクトリを移動または名前変更

```bash
mv oldname.txt newname.txt
```
+ rm: ファイルやディレクトリを削除

```bash
rm filename.txt
rm -r directory_name  # ディレクトリを再帰的に削除
```
+ touch: 新しい空のファイルを作成

```bash
touch newfile.txt
```
+ mkdir: 新しいディレクトリを作成

```bash
mkdir new_directory
```

+ VSCodeを起動する

```bash
code file_path
```

## Git
https://qiita.com/H-goto16/items/9d852e6a7aa787fceab2

## 実践

+ ホームディレクトリに移動

<details><summary>解答</summary>

```bash
cd
```

or

```bash
cd ~
```

</details>

+ `workspace`というディレクトリを作成

<details><summary>解答</summary>

```bash
mkdir workspace
```

</details>

+ `workspace`というディレクトリがあるか確認

<details><summary>解答</summary>

```bash
ls
```

+ 必要性 : エクスプローラでファイルを確認するのと同じ作業。ファイルの存在確認は重要なので何かあれば手癖でlsを打ち込んで確認するようにすると良い。

</details>

+ `workspace`というディレクトリに移動

<details><summary>解答</summary>

```bash
cd workspace
```

+ 必要性 : エクスプローラのダブルクリックと同じ容量であり、移動することが必須

</details>

+ `my`というディレクトリを`~workspace/`下に作成し、移動

<details><summary>解答</summary>

```bash
mkdir my
cd my
```

</details>

+ Pythonファイルを`~workspace/my/`下作成する。ファイル名は`index.py`

<details><summary>解答</summary>

```bash
touch index.py
```



</details>

+ `index.py`を`main.py`に名前を変更する

<details><summary>解答</summary>

```bash
mv index.py main.py
```

</details>

+ `src`というディレクトリを`~workspace/my/`下に作成し、`main.py`をその中に移動させる

<details><summary>解答</summary>

```bash
mkdir src
mv main.py src
```

</details>

+ `VSCode`でディレクトリを開く

<details><summary>解答</summary>

```bash
code .
```

適宜コマンドが存在しない場合は相談

</details>

+ (VSCode) `~workspace/src/main.py`に`Hello World`とターミナルに出力するプログラムを記入する

<details><summary>解答</summary>

```python
print("Hello World")
```

</details>

+ `src/main.py`を実行する


<details><summary>解答</summary>

```bash
python3 src/main.py
```

or

```bash
cd src
python3 main.py
```

</details>



+ `workspace/my`ディレクトリをgit管理する初期設定を行う

<details><summary>解答</summary>

`ls`や`pwd`などを用いて**workspace/myにいることをよく確認する！**


```bash
git init
```

+ 必要性 : gitでプログラムを管理することで、いつだれがどこをどう変更してメッセージを残したかが賢明になり、チームで開発するときにコードの安全性を保ちながら開発を行うことができる。

</details>

+ 全てのファイルをステージングに上げる

<details><summary>解答</summary>

```bash
git add .
```

+ ステージングされたファイルのみコミットされるのでステージングをわけてコミットするとコミットメッセージを分けることができる。
+ ステージングとはコミット待ちファイルの認識で良い。

</details>

+ コミットメッセージを残す。今回は`initial commit`をコミットメッセージにする

<details><summary>解答</summary>

```bash
git commit -m "initial commit"
```

+ 必要性 : コミットすることでそのファイルがどのような理由で変更されたかがわかる。したがって適当なコミットメッセージはチームメンバーにとっても迷惑である。

</details>

+ ブラウザでリモートリポジトリを作成(リポジトリ名は`lecture`)
また、プライベートにする

<details><summary>解答</summary>

`Create New...` -> `New repository`

`Repository name* ` -> lecture

`Public` -> `Private`

今回はテストなのでPrivateだが、Publicにすることで全世界に公開することができる。


</details>

+ SSHでURLをコピーし、リモートリポジトリとローカルリポジトリを紐付け

<details><summary>解答</summary>

```bash
git remote add origin [COPIED_URL]
```

+ 必要性 : リモートとローカルを紐付けることでバックアップをとったりすることが可能である。

</details>

+ 標準ブランチをmaster -> mainに変更

<details><summary>解答</summary>

```bash
git branch -M main
```

+ 必要性 : slave的な宗教観念からmainに変更することが多い

</details>

+ リモートリポジトリにpushする

<details><summary>解答</summary>

```bash
git push -u origin main
```

+ 必要性 : ローカルがごちゃごちゃしても最悪リモートから復旧が可能になったりする

</details>

+ `~workspace/my/src/`下に`module.py`を作成

<details><summary>解答</summary>

```bash
touch module.py
```

</details>

+ (VSCode) `Hello World`と出力する関数を作成。関数名は`output_hello_world`

<details><summary>解答</summary>

```python
def output_hello_world():
  print("Hello World")
```

</details>

+ 新しく作成した`module.py`をステージングに上げる

<details><summary>解答</summary>

```bash
git add .
```

or

```bash
git add src/module.py
```

</details>

+ コミットメッセージをつける。メッセージは`feat: add function that output Hello World`

<details><summary>解答</summary>

```bash
git commit -m "feat: add function that output Hello World"
```

</details>

+ コミットをpushする

<details><summary>解答</summary>

```bash
git push -u origin main
```

</details>

+ リモートリポジトリに変更がないか確認する

<details><summary>解答</summary>

```bash
git fetch
```

+ 必要性 : チームや自分がGitHubを更新をしたことをローカルにも認知させる。これがないと最新の状態にならず競合(conflict)が発生する原因になる。

</details>

+ リモートのmainをローカルのmainに取り込み、ローカルを最新の状態に更新する。

<details><summary>解答</summary>

```bash
git pull origin main
```

</details>
