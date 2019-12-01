<center>
# 標準化の例

解析ソフトでも様々な方法でデータを0-255で標準化してから可視化しているため,どの標準化手法が最も良いか考察する.

<br>

__結論のみ見るならば一番下までスワイプしてください.全部載ってます.__

<br>

[標準化とは](https://bellcurve.jp/statistics/course/19647.html)

なお,全ての手法について,fitsデータに含まれる値を0-255の範囲に標準化して,その値の大きさを画像の明るさで表現している.

用いたデータは[NGC4852.fits](https://www.dropbox.com/s/8uy7pnvo2o4s44l/datas.zip?dl=0s)の400or401フレーム目である.

<br><br><br>

## 1.単純な標準化
以下の式を用いて標準化する.

<br><br>
![](images/png/v=valueofeachpixel.png)<br>

![](images/png/img.png)
<br><br><br>
__結果__

![](images/normal.jpg)

<br><br><br>

## 2.自然対数を用いた標準化
以下の式を用いて標準化する.

<br><br>
![](images/png/v=valueofeachpixel.png)<br>

![](images/png/loge.png)<br>

![](images/png/img.png)
<br><br><br>
__結果__

![](images/loge.jpg)

<br><br><br>

## 3.正の範囲で自然対数を用いた標準化
なぜか負数も対数表現できてしまい気味が悪かったので,
以下の式を用いて標準化する.

<br><br>
![](images/png/v=valueofeachpixel.png)<br>

![](images/png/v=abs.png)<br>

![](images/png/loge.png)<br>

![](images/png/img.png)
<br><br><br>
__結果__

![](images/loge2.jpg)

<br><br><br>

## 4.2を底とした自然対数を用いた標準化
真数=0であると計算できないため,以下の式を用いて標準化する.

<br><br>
![](images/png/v=valueofeachpixel.png)<br>

![](images/png/v=abs.png)<br>

![](images/png/v=v+1.png)<br>

![](images/png/log2.png)<br>

![](images/png/img.png)
<br><br><br>
__結果__

![](images/log2.jpg)

<br><br><br>

## 5.10を底とした自然対数を用いた標準化
真数=0であると計算できないため,以下の式を用いて標準化する.

<br><br>
![](images/png/v=valueofeachpixel.png)<br>

![](images/png/v=abs.png)<br>

![](images/png/v=v+1.png)<br>

![](images/png/log10.png)<br>

![](images/png/img.png)
<br><br><br>
__結果__

![](images/log10.jpg)

<br><br><br>

## 6.総覧


単純な標準化 → log e n → log e n(1>n,1>n>0) → log 2 n (n>1) → log 10 n(n>1)

![](images/normal.jpg) ![](images/loge.jpg) ![](images/loge2.jpg) ![](images/log2.jpg) ![](images/log10.jpg)

</center>