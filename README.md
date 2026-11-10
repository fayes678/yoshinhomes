# Yoshin Homes

Website komunitas Arpy Studio. Statis (HTML tunggal) dengan backend Supabase.

## Isi repo
```
index.html
.nojekyll
CNAME
assets/
  arpy-profile.jpg
  arpy-profile-sm.jpg
  banner-arpy.jpg
```

## Deploy ke GitHub Pages
1. Upload semua file di atas ke branch `main` repo `yoshinhomes`.
2. Buka **Settings → Pages**.
3. Source: **Deploy from a branch**, Branch: **main**, folder **/ (root)**, lalu Save.
4. Tunggu 1–2 menit. Situs aktif di `https://<username>.github.io/yoshinhomes/`.

## Supabase
- Project: **YoshinHomes** (`ygpjhijzccuolxqdghjc`)
- Kunci di `index.html` adalah *publishable key*, memang aman ada di browser. Akses data dijaga RLS.
- Jangan pernah menaruh `service_role` key di repo ini.
- Konten diatur lewat tabel: `site_settings`, `community_stories`, `roblox_maps`, `partners`, `faqs`, `notifications`, `donations`, `reports`.

## Custom domain (yoshin.my.id)
File `CNAME` berisi `yoshin.my.id`. DNS di Cloudflare:

| Type | Name | Content | Proxy |
|---|---|---|---|
| A | @ | 185.199.108.153 | DNS only |
| A | @ | 185.199.109.153 | DNS only |
| A | @ | 185.199.110.153 | DNS only |
| A | @ | 185.199.111.153 | DNS only |
| CNAME | www | `<username-github>.github.io` | DNS only |

Lalu Settings → Pages → Custom domain: `yoshin.my.id` → Save → centang **Enforce HTTPS**.
