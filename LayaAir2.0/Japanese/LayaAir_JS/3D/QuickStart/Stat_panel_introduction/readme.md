# Stat统计面板的介绍

###### *version :2.2.0beta4   Update:2019-9-2*

開発者の性能最適化を容易にするために、LayaAir 3 Dは性能統計パネル「Stt統計パネル」を提供しています。開発者はリアルタイムで関連の性能パラメータを確認できます。

​![图](img/1.png)（図1）

統計に参加した性能パラメータは以下の通りです。（すべてのパラメータは約1秒ごとに更新されます。）

​**FPS（WebGL）／FPS（3 D）：**Laya 2 DモードまたはLaya 3 Dモードのフレームレート、すなわち、毎秒表示されるフレーム数は、高い値ほど安定しており、すっきりした感じがする。

​**Sprite:**すべてのレンダリングノード（容器を含む）の数を統計して、その大きさはエンジンのノード巡回、データ組織、レンダリングの効率に影響します。

​**RenderBatch：**レンダリングロット

​**SavedRenderBatch：**結合したレンダリングロット；

​**CPUメモリ:**CPUメモリ;

​**GPUMemory：**GPU現存

​**Shader:**Shader提出回数

​**Tri Faces:**三角面

​**Fustumculling:**カメラのパンカット回数。

​**Octree NodeCulling：**八叉ツリーノードの裁断回数；

###どうやってStat統計パネルを開けますか？

1.**編集モード--F 9--プレビュー設定--フレームレート統計パネルにチェックを付ける**	

2.プロジェクト起動後、直接コンソールに入力する**Laya.Stt.show（）**

##### 	