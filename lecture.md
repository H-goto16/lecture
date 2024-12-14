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
+

<details><summary>解答</summary>

```bash

```

</details>
+

<details><summary>解答</summary>

```bash

```

</details>+

<details><summary>解答</summary>

```bash

```

</details>
+

<details><summary>解答</summary>

```bash

```

</details>



