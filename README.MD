px68k-libretro のフォーク版

このリポジトリは、[px68k-libretro](https://github.com/libretro/px68k-libretro) のフォーク版です。
自分が利用するために都合の良い改造しています。

変更点

- コアオプションのInputのJoy/MouseでJoystickを選んだら、ジョイパッドの入力をマウスの操作に変換するようにした  
十字キーがカーソル移動、Bボタンが左クリック、Aボタンが右クリックになる
- M3Uを使った起動時のクラッシュを回避するために毎回SRAMを初期化するようにした  
参考: https://retropie.org.uk/forum/topic/31953/lr-px68k-multidisk-games-problem/13

ダウンロード

GitHub Actions のワークフローで自動的にコアファイルをビルドしています。  
[ワークフローの一覧](https://github.com/osobaudonmen/px68k-libretro/actions/workflows/release-build.yml) から最新の結果ページにアーティファクトとして添付されています。    
ただし、ワークフローの結果を90日間しか保存しないように設定しているため、しばらくコミットがなかったら消えると思います。

以下、オリジナルのREADME.mdを掲載しています。

---

px68k-libretro 

forked from https://github.com/hissorii/px68k
backported c68k core from https://github.com/kenyahiro/px68k/ 
(fork of https://github.com/hissorii/px68k using recent c68k yabause core to support X64 build)

All credit goes to hissorii ( and kenyahiro for updating c68k core) .

How to use :

First create a 'keropi' folder in retroarch system directory.
put the x68000 bios files in.

Then launch emulator with some content (dim|zip|img|d88|88d|hdm|dup|2hd|xdf|hdf)
12 or joypad L2 to enter menu.
Touroku key via ScrollLock key or Joypad R2 to enable MIDI music when preseed in Wolfteam games.


You can launch content with:

- retroarch -L px68k_libretro.so ./content.hdf

- retroarch -L px68k_libretro.so ./content.xdf

- retroarch -L px68k_libretro.so ./content.cmd
 (cmdfile is a text file contening cmd like "px68k /somewhere/software/x68000/content1.dim /somewhere/software/x68000/content2.dim")

- retroarch -L sdlpx68k_libretro.so "px68k /somewhere/software/x68000/content1.dim /somewhere/software/x68000/content2.dim"

- load retroarch , then load core and content from RA menu.

ひっそりぃ(hissorii)/sakahi
http://hissorii.blog45.fc2.com (ひっそりぃドットコム)
http://emuhani.seesaa.net      (えみゅはに - Emulator Hacking 日記)
GitHub: https://github.com/hissorii/px68k
iOS 版リポジトリ http://hissorii-com.appspot.com
Twitter: @hissorii_com
