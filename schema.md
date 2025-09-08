# Schema & Data Dictionary

## Dataset: processed_app_interactions.csv

### Base Schema (from cleaned CSV)

| Column               | Type         | Description                                |
|----------------------|--------------|--------------------------------------------|
| timestamp            | datetime     | 事件發生時間                               |
| user_id              | string       | 使用者唯一識別碼                           |
| session_id           | string       | 單次使用 session 識別碼                    |
| ip_address           | string       | 使用者 IP 位址                             |
| device_os            | string       | 裝置作業系統 (Android / iOS / 其他)        |
| device_os_version    | string       | 裝置作業系統版本                           |
| device_model         | string       | 裝置型號                                   |
| screen_resolution    | string       | 螢幕解析度                                 |
| location_country     | string       | 使用者所在國家                             |
| location_city        | string       | 使用者所在城市                             |
| app_language         | string       | App 使用語言                               |
| network_type         | string       | 網路型態 (WiFi / 4G / 5G / 其他)          |
| battery_level        | float        | 電池電量百分比 (0–100)                     |
| memory_usage_mb      | float        | 記憶體使用量 (MB)                          |
| event_type           | string       | 事件類型 (如 click, view, purchase)        |
| event_target         | string       | 事件目標 (按鈕/頁面/功能)                  |
| event_value          | string       | 事件相關值 (數值或 ID)                     |
| app_version          | string       | App 版本號                                 |
| session_duration_sec | float        | Session 持續時間 (秒)                      |
| is_subscribed        | boolean      | 是否轉換成功 (1=是, 0=否)                  |
| user_age             | float        | 使用者年齡                                 |
| phone_number         | string       | 使用者電話（建議匿名化或刪除於公開版本）   |
| push_enabled         | boolean      | 是否允許推播通知                           |

---

### Derived Fields (added during EDA / feature engineering)

| Column             | Type     | Description                      |
|--------------------|----------|----------------------------------|


---

### Notes
- `timestamp` 已轉換為 `datetime64[ns]` 型別。
- Derived Fields 區塊會隨著 Notebook 分析進度更新。
