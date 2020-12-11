# ライフゲーム

###  環境構築

python3,numpy,scipy,OpenCVをインストール

- numpyは、数値計算を効率的に行う。
- scipyは、numpyで行える配列や行列の演算を行うことができ、加えてさらに信号処理や統計といった計算ができるようになっています。
- OpenCVは、コンピューターで画像や動画を処理する。

### 初期設定

- 配列をnumpyのarrayメソッドで作成。
- random.randで 0・1 の乱数を生成。
- dtype=intで整数に変換
- reshapeで配列を2次元配列に形状変換する。

### 周囲の個数カウント

0または1を要素にもつint型のnumpy配列Fについて、
自身を含む周囲９マスの１の個数をカウントする。

- 要素が1の配列をnumpy.onesで生成。
- signal.correlate2dで2つの2次元配列をふたつの配列の類似性を確認する。
- sameで、同じ部分を合計し中心に出力。
- boundary="wrap"で配列の上下左右を繋げる。

### 次の世代

ある世代での状態FについてNを周囲の個数カウントした配列とすると、次の世代では

- Nが３の場合は必ず1
- Nが４の場合はF値をそのまま継続
- それ以外は必ず0

### ループ

- 配列初期設定 init_state
- 次の世代を計算する　next_generation
- 状態を出力する print_state

### 画像化

OpenCVを使って画像をリアルタイムで表示

- 状態Fをscale倍にした画像表示
- cv2.INTER_NEARESTを指定することでモザイク状に出力。

### 操作

python3 life.py　を実行すると、OpenCVの画像表示ウィンドウが立ち上がり、リアルタイムで世代が進む様子を見られます。

- r ：リセット
- q または Esc： 終了
- s ：遅く
- f：早く

### GIF
![](https://gyazo.com/36b94a5341ee9e08b7caee9f497bf63c.gif)