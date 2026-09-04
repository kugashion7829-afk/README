# Unity

## Unityの基本用語や設定

### シリアライズ
シリアライズとは、Unity上のオブジェクトや設定を、ファイルとして保存できる形式へ変換することです。Force Textでは、シーンやPrefabの情報が主にYAML形式のテキストとして保存されます。

### metaファイル
.metaファイルには、そのAssetを識別するGUIDなどが保存されています。<br>.metaを失うと、PrefabやSceneからの参照が外れることがあるため、GitではAssetと対応する.metaを必ず一緒に管理します。

### Layer
Layerは「どの種類のオブジェクトと判定するか」を絞り込むために使います。例えば接地判定をGroundだけに限定すると、敵やアイテムに触れたことを地面として誤認しなくなります。

### Development Build
Development Buildはデバッグ情報とProfiler対応を含める設定です。

### Deep Profiling
Deep Profilingは全スクリプト呼び出しを詳細に記録するため、ゲームの実行が大きく遅くなる可能性があります

### Library
LibraryはUnityがAssetを読み込んで生成するキャッシュです。容量が大きく、別の環境で再生成できるためGitには含めません。

## UnityCompornent

### Rigidbody

#### Freeze Rotation
回転を固定する

#### Interpolate
*   Interpolate<br>
物理更新の間を補完
表示上の揺れを軽減します。

#### Collision Detection
*   Continuous<br>
高速移動時のすり抜けを減らす

## MainCamera

### Orthographic Camera
Orthographic Cameraは遠近法を使わないカメラです。カメラから遠い物体も小さく表示されないため、2Dアクションに近い見た目になります。