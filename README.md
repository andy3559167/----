
# MapLock 🗺️ 🔒

一款為 Minecraft 伺服器設計的輕量化地圖保護插件。防止玩家未經許可複製你的地圖畫，並支援自訂經濟成本與多國語言。

## ✨ 功能特色

* **地圖鎖定系統**：防止鎖定的地圖在工作台或製圖台被複製。
* **多國語言支援**：內建繁體中文 (`zh_tw`)、簡體中文 (`zh_cn`) 與英文 (`en`)，支援自動偵測。
* **經濟系統整合**：支援 **Vault** 經濟橋樑，可設定鎖定地圖所需的手續費。
* **自訂物品消耗**：可設定鎖定地圖時需消耗特定物品（支援自訂名稱與 Lore 檢查）。
* **管理員工具**：提供詳細的地圖資訊查詢、強制解鎖功能。
* **權限細分**：所有指令與特權皆有對應權限，方便管理員配置。
* **自動補全**：完整的 Tab-Completion 支援，操作更直覺。

## 🛠️ 指令與權限

| 指令 | 說明 | 預設權限 | 權限節點 |
| --- | --- | --- | --- |
| `/map help` | 顯示插件幫助選單 | 所有人 | `maplock.help` |
| `/map lock` | 鎖定主手上的地圖 | 所有人 | `maplock.lock` |
| `/map unlock` | 解鎖自己擁有的地圖 | 所有人 | `maplock.unlock` |
| `/map admin info` | 查詢地圖鎖定者與日期 | OP | `maplock.admin.info` |
| `/map admin forceunlock` | 強制解鎖任何地圖 | OP | `maplock.admin.forceunlock` |
| `/map admin reload` | 重新載入設定檔與語言檔 | OP | `maplock.admin.reload` |

### 💡 額外特權

* `maplock.admin.bypass`: 擁有此權限者可無視「禁用世界」限制，且鎖定地圖不收費。

## 📦 安裝教學

1. 將 `MapLock.jar` 放入伺服器的 `plugins` 資料夾中。
2. （選配）若要啟用經濟功能，請確保伺服器已安裝 **Vault** 指令與經濟插件（如 CMI, EssentialsX）。
3. 重啟伺服器。
4. 於 `plugins/MapLock/config.yml` 中調整你的設定。

## ⚙️ 設定檔預覽 (config.yml)

```yaml
language: "zh_tw" # 語言設定

disabled-worlds: # 禁用世界清單
  - "disabledworlds1"

economy: # 經濟設定
  enabled: false
  cost: 100.0

item-cost: # 物品消耗設定
  enabled: true
  material: "DIAMOND"
  amount: 1
  display-name: "地圖鎖定憑證"
  strict-meta-check: true # 是否檢查自訂名稱與 Lore

```

---
