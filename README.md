# AupLauncher
Copyright (C) 2020 Takym.
Copyright (C) 2020 kokkiemouse. (仮)

[日本語](https://github.com/Takym/AupLauncher#ja)
[English](https://github.com/Takym/AupLauncher#en)

## 概要
AviUtl と Audacity のプロジェクトファイルを認識し適切なアプリケーションを起動します。
Windows 10 (2004) で動作確認しています。

## 注意
このアプリケーションはレジストリを変更します。
実行前にバックアップを取る事をおすすめします。

## 利用規約
このソフトウェアはMITライセンスの下で配布されます。
詳しくは[LICENSE.txt](LICENSE.txt)をご覧ください。

## インストール方法
0. AviUtl と Audacity がインストールされている事を前提に動作します。まず最初にインストールしておいてください。
	* [AviUtl](http://spring-fragrance.mints.ne.jp/aviutl/)
	* [Audacity](https://www.audacityteam.org/)
1. 適当な場所に下記のフォルダとファイルをコピーします。
	* en
		* AupLauncher.resources.dll
	* ja
		* AupLauncher.resources.dll
	* AupLauncher.exe
	* AupLauncher.exe.config
2. AupLauncher.exe を右クリックし管理者として実行します。すると、拡張子情報が自動的に関連付けられます。
3. 設定項目を環境に合わせて修正します。
4. 変更を保存します。
5. インストール完了です。

## アンインストール方法
1. 設定画面を開きます。
2. [アンインストール] ボタンを押します。
3. メッセージが表示されたら [はい] を選択します。
4. 関連フォルダとファイルを手動で削除します。

## 使い方
* 上記の指示に従って正しくインストールした場合、「.aup」ファイルを開くと自動的に AviUtl または Audacity が起動します。
* また、ファイル名の先頭に「aupfile:」と付けてブラウザ・エクスプローラ等のアドレスバーに入力する事でも起動できます。
* AupLauncher.exe に何も引数を与えずに起動した場合、設定画面が開かれます。
* 設定画面の右上の[?]ボタンを押すとバージョン情報が表示されます。

## 使用しているライブラリについて
自家ビルドなWindows API Codec Packを使用しています。

## バージョン履歴
|バージョン|開発コード名|更新日    |内容                                                                                                                           |
|:--------:|:----------:|:---------|:------------------------------------------------------------------------------------------------------------------------------|
|v0.0.0.6  |Derived From aupl00a6 base exe|2020/04/10|EXEファイルをメインにし、DLLはCOM登録時だけ呼び出されるようにした(EXEだけだと正常に登録ができないので、RUNDLL32で別プロセス化した。) |
|v0.0.0.6  |Derived From aupl00a6         |2020/04/06|動的アイコンのインストール、アンインストールを個別にできるようにした。さらに、特定の操作だけ管理者権限を要求するよう改善した。 |
|v0.0.0.5  |Derived From aupl00a5         |2020/04/04|サムネで区別できる機能を追加。                                                                 
