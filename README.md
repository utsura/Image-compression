# Image-compression
画像圧縮を実行するためのリポジトリです。

わからなければ、杉山に聞いて下さい！！！！！！！！！！！！！！！！！！！！！

## 環境構築
前提として、`node` をインストールして`npm`を使えるようにして下さい.

以下のバージョンでは動作確認ができています.
```
Node : v10.15.0
Npm  : no6.4.1
```

#### 手順
#### 1. Clone する
任意の場所にCloneしてください.
```
git clone https://github.com/utsura/Image-compression.git
```


#### 2. 該当ディレクトリに移動する

```
cd Image-compression/
```

#### 3. グローバルでgulpを入れる

```
npm install gulp -g
```

#### 4. 念の為入ったか確認する
```
gulp -v
```

#### 5. pakage.json 作成

```
npm init -y
```

#### 6. ローカルに gulpを入れる

```
npm install gulp
```

#### 7. gulp-imageminを導入する
```
npm install --save-dev gulp-imagemin
```

#### 8. imagemin-mozjpegを導入する

```
npm install --save-dev imagemin-mozjpeg
```

#### 9. imagemin-pngquantを導入する

```
npm install --save-dev imagemin-pngquant
```

#### 10. gulp-changedを導入する
```
npm install --save-dev gulp-changed
```

#### 11. 以下のファイルを Image-compression 以下に作成する

```
mkdir ./save_image
mkdir ./compressed
```

## 使い方
### 画像を準備する
1. さくらレンタルサーバ コントロールパネル > ファイルマネージャー > utsura > html > save_image をダウンロードする

1. slackの開発チャンネルのピン留めされている画像圧縮スレの最終圧縮日を確認する
例: 8月１４日まで完了

1. 圧縮済みのファイルを削除する
    1. ダウンロードした `save_image` を展開し、最終圧縮日までの画像を削除する（例: 8/14以下）

1. `save_image`（非圧縮な画像しかないはず）を該当ファイル(gulpfile.jsがおいてあるところ)にコピーする
ファインダーで行ってもOKです。

```
# ダウンロードディレクトリにsave_image があることを想定しています

cp /~Downloads/save_image ./path/to/Image-compression/save_image
```

1. gulp を実行する
```
gulp
```

1. 圧縮されたファイルを確認する
同一ディレクトリにある `compressed` を確認して、画像があるか確認して下さい

1. 元のファイルと圧縮後のファイルサイズを見て、圧縮されているか確認する
ダウンロードフォルダにある `save_image` と Image-compressionにある `compressed` の同じ画像サイズをみて、圧縮されているか確認する

1. 確認して、圧縮が確認していれば、OK!!!

## 圧縮した画像を再アップロードする

2. さくらレンタルサーバ コントロールパネル > ファイルマネージャー > utsura > html > save_imageを開く

2. アップロードを選択し、compressedにある全てのファイルをアップロードする

そのとき、必ず　上書きをする　にチェックを入れて下さい。

