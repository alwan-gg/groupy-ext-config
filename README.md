# groupy-ext-config

Remote config buat Groupy extension (private repo — jangan public).

## Cara update endpoint tanpa update extension

1. Edit `config.json` (sync_url / api_base kalau IP/domain VPS ganti)
2. Commit → selesai. Semua device fetch ulang otomatis (cache 10 menit).

## Field

| key | arti |
|---|---|
| `sync_url` | endpoint token sync extension → VPS |
| `api_base` | base URL groupy-cli (health/service/session) |
| `groupy_backend` | backend resmi groupy.id |
| `legacy_hosts` | host LAMA yang di-rewrite interceptor ke `api_base` |

## Raw URL yang dibaca extension

```
https://raw.githubusercontent.com/alwan-gg/groupy-ext-config/main/config.json
```

Fallback: kalau fetch gagal (offline/blocked), extension pake nilai default
built-in di `background.js` (shim).
