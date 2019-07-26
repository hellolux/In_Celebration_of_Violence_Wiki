# Locations(地点)

## 路线图

```flow
ts=>condition: The Sanctuary 圣地
desert=>condition: Desert 沙漠 :>?file=008-地点/002-沙漠
cave=>operation: Cave 洞穴 :>?file=008-地点/004-洞穴
labvrinth=>operation: Labvrinth 迷宫 :>?file=008-地点/008-迷宫
tomb=>operation: Tomb 墓穴 :>?file=008-地点/015-墓穴
obelisk=>subroutine: Obelisk 冠军之神 :>?file=005-神社/008-冠军之神
town=>condition: Town 城镇 :>?file=008-地点/005-城镇
hedgemaze=>operation: Hedge Maze 丛林迷宫 :>?file=008-地点/009-丛林迷宫
sewer=>condition: Sewer 下水道 :>?file=008-地点/010-下水道
castle=>operation: Castle 城堡 :>?file=008-地点/016-城堡
shield=>subroutine: Shield 争议之神 :>?file=005-神社/002-争议之神
plains=>condition: Plains 平原 :>?file=008-地点/003-平原
forest=>condition: Forest 森林 :>?file=008-地点/006-森林
winter=>operation: Winter 极地 :>?file=008-地点/011-极地
village=>operation: Village 村庄 :>?file=008-地点/012-村庄
prison=>operation: Prison 监狱 :>?file=008-地点/017-监狱
brearg=>subroutine: Brearg 锁链之神 :>?file=005-神社/004-锁链之神
swamp=>condition: Swamp 湿地 :>?file=008-地点/007-湿地
cemetery=>operation: Cemetery 墓地 :>?file=008-地点/013-墓地
crypt=>operation: Crypt 地窖 :>?file=008-地点/018-地窖
veil=>subroutine: Veil 死神 :>?file=005-神社/009-死神
marsh=>operation: Marsh 沼泽 :>?file=008-地点/014-沼泽
grotto=>operation: Grotto 岩穴 :>?file=008-地点/019-岩穴
free=>subroutine: Free 残疾之神 :>?file=005-神社/003-残疾之神

ts(yes)->desert(yes)->cave->labvrinth->tomb->obelisk
desert(no)->town(yes)->hedgemaze->castle->shield
town(no)->sewer(yes)->castle->shield
sewer(no)->marsh->grotto->free

ts(no)->plains(yes)->forest(yes)->winter->prison->brearg
forest(no)->village->cemetery->crypt->veil

plains(no)->swamp(yes)->cemetery->crypt->veil
swamp(no)->marsh->grotto->free

```
