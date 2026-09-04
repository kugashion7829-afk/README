# Unity

## Unityの基本用語や設定

### シリアライズ
シリアライズとは、Unity上のオブジェクトや設定を、ファイルとして保存できる形式へ変換することです。Force Textでは、シーンやPrefabの情報が主にYAML形式のテキストとして保存されます。

### metaファイル
.metaファイルには、そのAssetを識別するGUIDなどが保存されています。<br>.metaを失うと、PrefabやSceneからの参照が外れることがあるため、GitではAssetと対応する.metaを必ず一緒に管理します。

### Layer
Layerは「どの種類のオブジェクトと判定するか」を絞り込むために使います。例えば接地判定をGroundだけに限定すると、敵やアイテムに触れたことを地面として誤認しなくなります。

## UnityCompornent

### Rigidbody

#### Freeze Rotation
回転を固定する

#### Interpolate
*   Interpolate<br>
物理更新の間を補完
表示上の揺れを軽減します。