# LimStudio (limstudio.ai.id)

Official landing page repository for **LimStudio** (`limstudio.ai.id`) — Indonesian AI & Automation Engineering Lab.

---

## 📁 Struktur Berkas

* [`index.html`](file:///D:/PROJECT/LimStudioID/index.html) — Landing page *Segera Hadir* (ultra-ringan, responsive, no external heavy libraries).
* [`CNAME`](file:///D:/PROJECT/LimStudioID/CNAME) — Custom domain binding (`limstudio.ai.id`).
* [`robots.txt`](file:///D:/PROJECT/LimStudioID/robots.txt) & [`sitemap.xml`](file:///D:/PROJECT/LimStudioID/sitemap.xml) — SEO & crawler configuration.
* [`_headers`](file:///D:/PROJECT/LimStudioID/_headers) — Security & caching headers for Cloudflare Pages.
* [`wrangler.jsonc`](file:///D:/PROJECT/LimStudioID/wrangler.jsonc) — Cloudflare Pages configuration.

---

## 🚀 Panduan Setup Domain `limstudio.ai.id`

### 1. Pindahkan Nameserver Domain ke Cloudflare
1. Buka dashboard Cloudflare ([dash.cloudflare.com](https://dash.cloudflare.com/)) -> **Add a Site** -> Masukkan `limstudio.ai.id`.
2. Pilih paket **Free**.
3. Salin 2 Nameserver Cloudflare yang diberikan (contoh: `alfa.ns.cloudflare.com` & `beta.ns.cloudflare.com`).
4. Buka panel registrar tempat kamu membeli domain `limstudio.ai.id` (misal: Niagahoster, DomaiNesia, IDCloudHost, Exabytes, dsb).
5. Ubah **Name Server** domain menjadi 2 nameserver Cloudflare tadi. Tunggu propagasi 5-15 menit.

---

### 2. Opsi Deploy Cepat (Pilih Salah Satu)

#### Opsi A: Deploy ke Cloudflare Pages (Rekomendasi Utama)
Di terminal PowerShell:
```powershell
cd D:\PROJECT\LimStudioID
npx wrangler pages deploy . --project-name limstudio-id
```
Lalu di Cloudflare Pages Dashboard:
* Buka project `limstudio-id` -> **Custom domains** -> Tambahkan `limstudio.ai.id` dan `www.limstudio.ai.id`. Cloudflare akan mengonfigurasi DNS record secara otomatis.

#### Opsi B: Deploy ke GitHub Pages
1. Buat repository baru di GitHub (misal: `limstudio-id`).
2. Push folder ini:
   ```powershell
   cd D:\PROJECT\LimStudioID
   git init
   git add .
   git commit -m "feat: initial release limstudio.ai.id coming soon page"
   git branch -M main
   git remote add origin https://github.com/Limm-web/limstudio-id.git
   git push -u origin main
   ```
3. Di Settings GitHub Repo -> **Pages** -> Source: Deploy from branch `main` -> Custom Domain: `limstudio.ai.id`.
4. Di DNS Cloudflare buat record:
   * **CNAME** `@` -> `Limm-web.github.io` (Proxy: Proxied)
   * **CNAME** `www` -> `Limm-web.github.io` (Proxy: Proxied)

---

### 3. Setup Email Domain Gratis (`contact@limstudio.ai.id`)
1. Di Cloudflare Dashboard -> Pilih domain `limstudio.ai.id` -> Menu **Email Routing**.
2. Klik **Enable Email Routing** (Cloudflare akan otomatis menambahkan MX records ke DNS).
3. Masukkan Destination Address (Gmail pribadimu) lalu klik verifikasi link di Gmail.
4. Buat Routing Rule:
   * `contact@limstudio.ai.id` -> Diteruskan ke email Gmail pribadimu.
   * `halo@limstudio.ai.id` -> Diteruskan ke email Gmail pribadimu.
