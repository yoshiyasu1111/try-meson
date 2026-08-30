# Try Meson

Mesonを使ってC++プログラムをビルドするためのサンプルです。

`meson.build`にビルド方法を記述し、MesonからNinjaの`build.ninja`を生成してビルドします。

## ファイル構成

```text
.
├── hello.cpp
└── meson.build
```

* `hello.cpp` — サンプルのC++プログラム
* `meson.build` — Mesonのビルド定義

## 必要なもの

* C++コンパイラ（GCCなど）
* [Meson](https://mesonbuild.com/)
* [Ninja](https://ninja-build.org/)

Ubuntuでは、以下のコマンドでインストールできます。

```sh
sudo apt update
sudo apt install meson ninja-build
```

## ビルド

まず、`meson setup`でビルドディレクトリを作成します。

```sh
meson setup build
```

その後、`meson compile`でビルドします。

```sh
meson compile -C build
```

`build`ディレクトリに`hello`という実行ファイルが生成されます。

```sh
./build/hello
```

実行すると、以下のように表示されます。

```text
Hello, World!
```

## クリーン

ビルドディレクトリを削除する場合は、Mesonの`compile`コマンドではなく、ディレクトリごと削除できます。

```sh
rm -rf build
```

その後、再び`meson setup build`を実行すればビルドできます。

## 関連記事

このリポジトリは、以下の記事で使用しているサンプルコードです。
