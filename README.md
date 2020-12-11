# lifegame

###  環境構築

- python3,numpy,scipy,OpenCVをインストール

- numpyは、数値計算を効率的に行う。
- scipyは、numpyで行える配列や行列の演算を行うことができ、加えてさらに信号処理や統計といった計算ができるようになっています。
- OpenCVは、コンピューターで画像や動画を処理する。

### 初期設定

- 配列をnumpyのarrayメソッドで作成。
- random.randで 0・1 の乱数を生成。
- dtype=intで整数に変換
- reshapeで配列を2次元配列に形状変換する。

### 周囲の個数カウント

- 0または1を要素にもつint型のnumpy配列Fについて、
自身を含む周囲９マスの１の個数をカウントする。

- 要素が1の配列をnumpy.onesで生成。
- signal.correlate2dで2つの2次元配列をふたつの配列の類似性を確認する。
- sameで、同じ部分を合計し中心に出力。
- boundary="wrap"で配列の上下左右を繋げる。

### 次の世代

- 
- 
- 

### ループ

- 
- 
- 

### 画像化

- 
- 
- 

### 操作

- python3 life.py　を実行すると、OpenCVの画像表示ウィンドウが立ち上がり、リアルタイムで世代が進む様子を見られます。

- r ：リセット
- q または Esc： 終了
- s ：遅く
- f：早く

### GIF
![](https://gyazo.com/36b94a5341ee9e08b7caee9f497bf63c.gif)