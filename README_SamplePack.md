# サンプルパック (tudur_sample)

Tudur's Vehicle Mod の全乗り物タイプ・全武器タイプを網羅した、動作するサンプル
アドオンパックです。`tudursvehiclemod-addons/` 配下にこのフォルダごと配置し、
`/reload` で読み込まれます。モデルは箱を組み合わせたローポリ、テクスチャは
単色スウォッチ(キャノピー部分のみ半透明)です。細部の調整はご自由にどうぞ。

## 乗り物 (data/tudur_sample/vehicles/)

| ファイル | タイプ | 主な実装要素 |
|---|---|---|
| sample_helicopter | helicopter | メイン/テールローター回転、チンターレット(weapon_parts+pilot_fallback+recoil)、ロケット(HEIAP子弾)、対戦車ミサイル(トップアタック、ammo_parts+display_penalty)、スライド式ドア、サーチライト+light_hatch、航法灯、パラシュート降下席、float_capable |
| sample_aircraft | aircraft | 機銃(熱量式+薬莢)、対空ミサイル、ウェポンベイ(weapon_bay扉+ASMissile)、増槽(DropTank+display_penalty)、スモーク、降着装置3脚+扉(landing_gear/landing_gear_hatch)、キャノピー、可変翼(wing_sweep)、射出座席、失速。CAS/Carrierの発艦機としても使用 |
| sample_uav | helicopter | is_uav/is_target_drone、クアッドローター、自爆(Destruct)、weapon_bayハッチ |
| sample_vtol | vtol | ティルトローター(vtol_rotor_parts+vtol_rotor_parent)、爆弾(DelayFuse+Bound)、FAE爆弾、汎用ミサイル(Missile)、MkRocket、後部ランプ、mob_drop_option、降下兵席 |
| sample_halftrack | car | 前輪操舵(wheel_parts)+後部履帯(crawler_tracks)+転輪(track_roller_parts)+ハンドル(steering_wheel_parts)、砲塔(親子weapon_parts)、消火器(Dispenser)、ターゲティングポッド、操舵追従サーチライト、pivot_turn_throttle |
| sample_ship | ship | 滑走路3本(通常/エレベーター連動hatch_offset/hatch_gated)、Carrier発艦(編隊・カタパルト・帰投・回収)、対潜ロケット(ASWeapon)、CIWS(spins_while_firing)、爆雷(Depth)、回転レーダー、補給範囲、航跡 |
| sample_submarine | submarine | 潜航(dive_max_speed)、魚雷(UsableWhileDiving)、ハッチ/潜望鏡、スクリュー |
| sample_emplacement | static_emplacement | 高射砲(空中炸裂+子弾+距離表示)、TVミサイル、CAS呼び出し(3機編隊)、ダミー武器、regeneration |

## 武器 (assets/tudur_sample/weapons/) — 全Type網羅

MachineGun1 (smp_minigun / smp_flak), MachineGun2 (smp_ciws / smp_turret_gun), Rocket (smp_rockets),
Bomb (smp_bomb / smp_fae_bomb / smp_kamikaze), Depth (smp_depth_charge), Torpedo (smp_torpedo),
ASMissile (smp_as_missile), MkRocket (smp_mk_rocket), AAMissile (smp_aa_missile), ATMissile (smp_at_missile),
Missile (smp_missile), ASWeapon (smp_asw), TVMissile (smp_tv_missile), Dispenser (smp_dispenser),
Smoke (smp_smoke), Dummy (smp_dummy), TargetingPod (smp_targeting_pod), DropTank (smp_drop_tank),
CAS (smp_cas), Carrier (smp_carrier)

## その他

- `assets/tudur_sample/hud/sample_hud.txt` … 全描画コマンド・If/Call/Exitを使ったHUD(+`sample_compass.txt`)
- `assets/tudur_sample/textures/gui/sample_needle.png` … HUDの回転針テクスチャ
- `assets/tudur_sample/sound/*.ogg` … 合成音のエンジン音/発射音(smp_engine_jet/rotor/car/boat, smp_gun, smp_launch)
- `assets/tudur_sample/models/obj/bullet_*.obj` … 弾体・薬莢モデル(rocket/missile/bomb/torpedo/shell/cartridge)
- `textures/dummy_pilot/*.png` … テーマ別ダミーパイロットスキン(flight_suit / tank_crew / sailor / submariner / gunner / operator)

