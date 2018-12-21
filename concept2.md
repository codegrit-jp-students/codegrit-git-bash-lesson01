## 最初に知っておいて欲しいコマンド

自分のユーザー名を表示するだけだとあまり有用性がないので、有用性の高いコマンドを学んでいきましょう。全部で11個なので、頑張って使っているとすぐに慣れて自然にコマンドが頭に浮かぶようになるはずです。

### pwd

pwd(**P**rint **W**orking **D**irectory)を使うと現在自分がどのディレクトリにいるかを知ることが出来ます。最初にターミナルを開いた時はホームディレクトリに居ますので、Macの場合でしたら以下のように表示されるでしょう。

```
$ pwd
/c/Users/user_name
```

### cd

cd(**C**hange **D**irectory)を使うとホームディレクトリに戻ることが出来ます。例えば、現在のディレクトリがDesktopだとしましょう。すると次のようになりあす。

```
$ pwd
/c/Users/user_name/Desktop
$ cd
$ pwd
/c/Users/user_name
```

### cd + ディレクトリ

`cd`のみであれば、ホームディレクトリに戻りますが`cd ディレクトリ`で他のディレクトリへ移動することが出来ます。例えばDesktopに移動したい場合は以下のようにします。

```
$ pwd
/c/Users/username
$ cd Desktop
$ pwd
/c/Users/username/Desktop
```

また試しに、`De`まで入力した後に`tab`をクリックして見て下さい。すると自分で全部を入力しなくても`Desktop`と入るはずです。

### ls

`ls`(lists)は、指定したディレクトリ内のファイルやフォルダを見るために利用します。lsの後に何も入力しなければ現在いるディレクトリのファイルやフォルダを見ることが出来ます。例えばホームディレクトリであれば以下のように表示されるはずです。

```
$ cd Desktop
$ pwd
/c/Users/username/Desktop
$ ls
desktop.ini  test/  testDir/
$ ls testDir
test.txt
```

### mkdir

`mkdir`(**M**ake **D**irectory)を利用すると、新しいディレクトリ(フォルダ)を作成することが出来ます。

```
$ pwd
/c/Users/username
$ mkdir test
$ cd test
$ pwd
/Users/username/test
$ ls
$ 

空なので何も表示されません。
```

### touch

`touch`を利用すると、新しいファイルを作成することが出来ます。

```
$ pwd
/Users/user_name/test
$ ls
$ touch test.md
$ ls
test.md
```

### nano

ターミナル内でnanoというエディタを立ち上げることが出来ます。ちょっとファイルを編集したいという場合に便利です。

```
$ nano test.md
```

すると以下のような画面に変わります。

![nano-1](./images/nano.png)

何かを入力してみましょう。

![nano-2](./images/nano-2.png)

`control + X`を押すと以下のような文章が出ます。

![nano-3](./images/nano-3.png)

ここで、"Shift + Y"(大文字のY)で保存ができます。

### cat

cat(Con**cat**enate)はファイルの中身を見たい時に利用します。例えば、先ほど作成した"test.md"を見てみましょう

```
$ ls
test.md
$ cat test.md
これはテストです。
```

このようにファイルをエディタなどで開くのが面倒だと言う時にcatはとても便利です。

### mv

mv(**M**o**v**e)はファイルを別の場所に移したい時に利用します。例えば、現在"test.md"のファイルがホームディレクトリにありますが、これをDesktopに移したいとします。

```
$ pwd
/c/Users/user_name/test
$ ls
test.md
$ mv test.md ../Desktop
$ ls
$
$ ls ../Desktop
test.md
```

このように、ファイルがtestフォルダから消えて、Desktopに移動したことが分かります。

### cp

cp(**C**o**p**yはファイルをコピーしたい時に利用します。例えば先ほどDesktopに移したtest.mdファイルをコピーしてtest2.mdというファイルを作ってみましょう。

```
$ cd ../Desktop
$ ls
test.md
$ cp test.md test2.md
$ ls
test.md test2.md
```

### rm

さて、テストファイルを勉強目的に作ってみましたが、今後使わないので消してしまいましょう。このときにはrm(**R**e**m**ove)コマンドを使います。

```
$ ls
test.md test2.md
$ rm test.md test2.md
$ ls
$
ファイルが削除されたため何も表示されません。
```

### rm -r

さて、ファイルを削除しましたが、ホームディレクトリ直下に作成した"test"フォルダがまだ残っています。これを消したいときは`rm`に`-r`というオプションを付けます。

```
$ cd
$ ls
... test
$ rm -r test
$ ls
... 
testフォルダが消えます。
```

## CodeGritでコマンドラインをどう使っていくのか

プログラミングスクールの中には、初心者にとっつきにくいコマンドラインの利用や、バージョン管理のシステム、を避けているところも少なくありません。CodeGritでは、学習者が将来的にプロの開発者となることを想定してコースを作成しているため、あえて避けずにコマンドラインを事前コースに含んでいます。

今回習ったコマンドラインについては、例えばGitというプログラマほぼ全員の使っているバージョン管理システムを使う場合や、Javascriptのようなプログラミング言語を学習する際にも頻繁に使っていきます。このレッスンだけで全て使いこなせるようになっていなくても学習の中でどんどん身に付いていきますので安心してください。

## まとめ

ここまでで、コマンドラインの基礎を抑えることが出来ました。今後コマンドラインに慣れていったら、他のコマンドやオプションを使う機会が増えていくかと思います。その都度新しい知識を身に着けてコマンドラインのエキスパートとなっていきましょう。

## 更に学ぼう

### 動画で学ぶ

[UNIXコマンド入門 [一般ユーザー編] - ドットインストール](https://dotinstall.com/lessons/basic_unix_v2)

### 記事で学ぶ

[UNIXコマンドの使い方](http://www.gi.ce.t.kyoto-u.ac.jp/user/susaki/command/)