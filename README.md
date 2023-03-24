# png2ttf  
builds ttf font from png image  
png画像を二値化してttfフォントを作るwindows向けプログラム。nymwaさんのtwahiに触発されて作った https://github.com/nymwa/ttf-twahi  
  
※このプログラムはfontforgeモジュールを使うため  
fontforge-console.batを開くと出るCUIから使う(後述)  
  
###使い方  

##準備  
magick https://imagemagick.org/index.php  
png -> bmp 変換用  
ダウンロードしてインストールすればpathが通って使える  

potrace https://potrace.sourceforge.net/  
bmp -> svg 変換用  
ダウンロードしてpotrace.exeがあるフォルダに手動で環境変数を設定しpathを通せば使える  
windows10の場合の手順:  
設定>システム>詳細情報>システムの詳細設定>環境変数(N)>ユーザーの環境変数>編集(E)>新規  
から「C:\p\potrace」などとpotrace.exeのあるフォルダを入力しOKを押す  
  
fontforge https://fontforge.org/en-US/  
svg -> ttf 変換用  
ダウンロードしてインストールする  
  
  
##実行  
#1  
uni0041.png のような形式でunicodeコードがファイル名のpng画像ファイルを用意してpng2ttf.pyと同じフォルダに置く  
#2  
このコードのname = "font1" の所を作りたいフォント名に書き換える  
#3  
fontforgeをインストールしたフォルダにあるfontforge-console.batを開けてfontforge python bindingが使えるCUIを開く  
#4  
「cd C:/Users/Tarou/Downloads」(png2ttfがあるディレクトリへの移動コマンド)「ffpython png2ttf.py」(実行コマンド)などのように打つって実行 
#5  
png画像と同じフォルダにttfフォントファイルが書き出される  
  
macやlinuxユーザーならCUIを開かなくてもaptコマンドとかで普通にfontforgeモジュールをインストールしてもっと楽にプログラムを実行できると思う  
  
#png2COLRttf  
[png2COLRttf](https://github.com/Mikanixonable/png2COLRttf)  
姉妹プログラム。カラーフォントを画像から自動生成する
