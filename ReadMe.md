# このソフトウェアについて

音名、変化記号、音高から周波数を算出して11オクターブ分の12音を鳴らした。

オクターブを考慮した音高を算出する。

# 対象ファイル名

ファイル名|説明
----------|----
playToneFrequency.py|音声再生を実行する
makeToneFrequency.py|音声ファイル出力を実行する
ToneFrequency.py|幹音と変化記号(`D+`等)と音高から周波数を算出する
ToneAccidentaler.py|幹音と変化記号(`D+`等)から音律における音IDと音高(pitch(-1〜9))を算出する
Accidental.py|変化記号の定義
NaturalTone.py|幹音の定義

# 実行

```sh
$ cd src/MusicTheory
$ python playToneFrequency.py
```
```sh
$ cd src/MusicTheory
$ python makeToneFrequency.py
```

```sh
$ python testToneFrequency.py 
...
-------pitch: -1
noteNumber: 0
C   0  -1 8.175799
noteNumber: 1
C#  1  -1 8.661957
noteNumber: 2
D   2  -1 9.177024
noteNumber: 3
D#  3  -1 9.722718
noteNumber: 4
E   4  -1 10.300861
noteNumber: 5
F   5  -1 10.913382
noteNumber: 7
G   7  -1 12.249857
noteNumber: 8
G#  8  -1 12.978272
noteNumber: 9
A   9  -1 13.750000
noteNumber: 10
A# 10  -1 14.567618
noteNumber: 11
B  11  -1 15.433853
...
-------pitch: 4
noteNumber: 60
C   0   4 261.625565
noteNumber: 61
C#  1   4 277.182631
noteNumber: 62
D   2   4 293.664768
noteNumber: 63
D#  3   4 311.126984
noteNumber: 64
E   4   4 329.627557
noteNumber: 65
F   5   4 349.228231
noteNumber: 67
G   7   4 391.995436
noteNumber: 68
G#  8   4 415.304698
noteNumber: 69
A   9   4 440.000000
noteNumber: 70
A# 10   4 466.163762
noteNumber: 71
B  11   4 493.883301
...
-------pitch: 9
noteNumber: 120
C   0   9 8372.018090
noteNumber: 121
C#  1   9 8869.844191
noteNumber: 122
D   2   9 9397.272573
noteNumber: 123
D#  3   9 9956.063479
noteNumber: 124
E   4   9 10548.081821
noteNumber: 125
F   5   9 11175.303406
noteNumber: 127
G   7   9 12543.853951
noteNumber: 128
G#  8   9 13289.750323
noteNumber: 129
A   9   9 14080.000000
noteNumber: 130
A# 10   9 14917.240369
noteNumber: 131
B  11   9 15804.265640
```

音が低すぎる気がする。

# 開発環境

* Linux Mint 17.3 MATE 32bit
* [libav](http://ytyaru.hatenablog.com/entry/2018/08/24/000000)
    * [各コーデック](http://ytyaru.hatenablog.com/entry/2018/08/23/000000)
* [pyenv](https://github.com/pylangstudy/201705/blob/master/27/Python%E5%AD%A6%E7%BF%92%E7%92%B0%E5%A2%83%E3%82%92%E7%94%A8%E6%84%8F%E3%81%99%E3%82%8B.md) 1.0.10
    * Python 3.6.1
        * [pydub](http://ytyaru.hatenablog.com/entry/2018/08/25/000000)
        * [PyAudio](http://ytyaru.hatenablog.com/entry/2018/07/27/000000) 0.2.11
            * [ALSA lib pcm_dmix.c:1022:(snd_pcm_dmix_open) unable to open slave](http://ytyaru.hatenablog.com/entry/2018/07/29/000000)
        * [matplotlib](http://ytyaru.hatenablog.com/entry/2018/07/22/000000)
            * [matplotlibでのグラフ表示を諦めた](http://ytyaru.hatenablog.com/entry/2018/08/05/000000)

# 参考

感謝。

## 音名

* https://ja.wikipedia.org/wiki/%E9%9F%B3%E5%90%8D%E3%83%BB%E9%9A%8E%E5%90%8D%E8%A1%A8%E8%A8%98

## 音高の算出

http://www.asahi-net.or.jp/~HB9T-KTD/music/Japan/Research/DTM/freq_map.html
http://www.nihongo.com/aaa/chigaku/suugaku/pythagoras.htm

## サイン波のスピーカ再生

* http://www.non-fiction.jp/2015/08/17/sin_wave/
* http://aidiary.hatenablog.com/entry/20110607/1307449007
* http://ism1000ch.hatenablog.com/entry/2013/11/15/182442

# ライセンス

このソフトウェアはCC0ライセンスである。

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed.ja)

Library|License|Copyright
-------|-------|---------
[pydub](https://github.com/jiaaro/pydub)|[MIT](https://github.com/jiaaro/pydub/blob/master/LICENSE)|[Copyright (c) 2011 James Robert, http://jiaaro.com](https://github.com/jiaaro/pydub/blob/master/LICENSE)
[pygame](http://www.pygame.org/)|[LGPL](https://www.pygame.org/docs/)|[pygame](http://www.pygame.org/)

