# アリーナの作り方 (0.2.x)

!!! Warning "ワールドについて"

    このドキュメントでは、「Multiverse」や「SlimeWorldManager」などのプラグインを使用して、
    指定したBedWarsマップがロードされたワールドを持っており、既にそのBedWarsマップのワールドにいることを前提としています。

## アリーナの作成方法

次のコマンドを実行してアリーナを作成します。

`/bw admin <アリーナ名> add`

**最初**の位置を設定するには、マップの**端**の隅に移動し、`/bw admin <アリーナ名> pos1`を実行します。

**2番目**の位置を設定するには、マップの**最初の端と反対側**の隅に移動し、`/bw admin <アリーナ名> pos2`を実行します。

!!! note "ポジションについて"

    `pos1`はアリーナの一角であり、`pos2`を指定する際はアリーナの`pos1`の反対側の角です。

## チームの追加

今度はチームを追加します。チームを追加するには、`/bw admin <アリーナ名> team add <チーム名> <チーム色> <チームの人数>`を実行してください。

色には、[TeamColor](https://jd.screamingsandals.org/sbw-0-2-x/BedWars-API/org/screamingsandals/bedwars/api/TeamColor.html)列挙型、`RED`、`BLUE`、`GREEN`、`YELLOW`などを使用できます。

`MAGENTA`,`PINK`,`LIME`,`BLACK`,`WHITE`,`ORANGE`,`LIGHT_GRAY`,`GRAY`,`LIGHT_BLUE`,`CYAN`,`BROWN`

!!! Warning

    少なくとも**２つ**のチームを作成する必要があります！

## チームがスポーンする場所の設定方法

チームをスポーンさせたい場所に立ち、プレーヤーがスポーンするときに見る向きを見ながら、コマンドを実行してください。(スポーンする際に視点も変えれるため)

`/bw admin <アリーナ名> Team spawn <チーム名>`を使用して、それぞれのチームのスポーンを設定してください。

※すべてのチームがスポーンするように、`/bw admin <アリーナ名> Team spawn <チーム名>`を設定してください。

!!! note "例"

    `/bw admin <アリーナ名> Team spawn Red` - Redチームのスポーン場所を設定する

    `/bw admin <アリーナ名> Team spawn Blue` - Blueチームのスポーン場所を設定する

    `/bw admin <アリーナ名> Team spawn Yellow` - Yellowチームのスポーン場所を設定する
    
    `/bw admin <アリーナ名> Team spawn Green` - Greenチームのスポーン場所を設定する

## チームベッドの設定

ベッドの上に立って、ベッドの枕らへんを見ながら`/bw admin <アリーナ名> team bed <team name>`を実行して、ベッドの位置を設定します。

すべてのチームのベッド設定ができるまで繰り返してください！

!!! tip "ターゲットブロックの場合"

    チームのターゲットブロックはベッドに限定されません。この`BedWars`はあらゆるブロックをサポートしています。
    
    (ドラゴンの卵、ケーキ、及びリスポーンアンカーには特別なサポートがあり、BedWarsがすぐに`EggWars`、
    
    `AnchorWars`、または`CakeWars`として動作できるようになります)。

!!! tip "設定するときの工夫"

    どこを設定したかわからなくなるのを防ぐために、チャットで`赤のベッドを設定した`みたいな記録を残しておくと便利です。

## 資源ジェネレーターの追加方法

ジェネレーターを配置するブロックに立って、`/bw admin <アリーナ名> spawner add <資源名> <true/false>`を実行してください。

有効なデフォルトの資源種類: bronze、iron、gold

!!! Warning

    ダイヤモンドとエメラルドは初期状態では含まれていません。構成に自分で追加する必要があります！

`true/false`部分は、ホログラムがあるべきか( true )、ホログラムがないべきか( false )を意味します。

## アイテム販売の村人の追加方法

今度はショップを追加します。お店のエンティティを配置したい場所に立ち、前を向いて`/bw admin <アリーナ名> store add <エンティティまたはVillager> [file with shop] [use main shop]`を実行します。

(最後の[file with shop]と[use main shop]は書かなくても大丈夫です。)

!!! info "お店のエンティティタイプについて"
    
    ストアとして別のエンティティを使用したい場合は、次のコマンドを実行してください。

    `/bw admin <アリーナ名> store type <エンティティ名>`

    これにより、ストアのエンティティ タイプ (村人、馬、牛など) が設定されます。

    スキンを備えたプレイヤーを店主にしたい場合は、次のコマンドを実行してください。
    
    `/bw admin <アリーナ名> store type Player:skinname`

    村人を設定する場合

    `/bw admin <アリーナ名> store add Villager`

## 最後の準備

`/bw admin <アリーナ名> lobby`を実行して、アリーナのロビーの場所を追加します！

`/bw admin <アリーナ名> spec`を実行して、アリーナのスペクテイターのスポーン位置を追加します！

!!! info "設定するときのおすすめポイント"

    Lobby場所は、スペクテイタースポーン場所の上が一番いいかも？(地面を作ってください。)

    スペクテイタースポーンは、Lobbyの下の方がいいかも？(景観的に)


最後になりましたが、絶対に、アリーナの保存を行ってください！`/bw admin <アリーナ名> save`

!!! Warning "絶対してね？"
    
    アリーナの保存をしないと、設定がパーになるので絶対保存してくださいね！

    `/bw admin <アリーナ名> save`

## チームを選ぶ時に簡単にする設定方法

看板を右クリックすることで、簡単に自分のチームを設定することができます！

- 1行目に「BedWars」または「BWGame」と書きます。
- 2行目に参加するアリーナ名を書きます。
- 最初の看板の更新では、ゲームに参加することになります！

`leave`または、アリーナ名の代わりの単語を書いて退出することができる看板を作成できます。

