# Excretion Quest SaaS

**Excretion Quest** adalah gamifikasi IPA sistem ekskresi dengan gaya **chibi science adventure** dan fondasi produk SaaS untuk sekolah/lembaga.

## Sudah tersedia

- Avatar pemain chibi + custom name.
- Faceless Muslimah Scientist sebagai guide.
- 12 arena: Body Entry → Bloodstream → Kidney City → Nephron Lab → Filtration → Reabsorption → Urine Pathway → Urine Detective → Skin → Lung → Liver → Final Boss.
- XP, rank, badge, arena unlock, progress.
- Teacher SaaS dashboard.
- Tenant/school selector.
- Class roster demo.
- Student join code.
- Assignment demo.
- Pricing/feature gate: Free, School, Pro.
- Local persistence dengan localStorage untuk demo.
- GitHub Pages deployment workflow.

## Model SaaS

Struktur data produksi yang direkomendasikan:

`tenants → users → classes → memberships → assignments → attempts → progress → avatar_items`

### Paket contoh

| Paket | Kelas | Siswa | Fitur |
|---|---:|---:|---|
| Free | 1 | 10 | Basic game + progress |
| School | 20 | 500 | Semua arena + analytics + assignment |
| Pro | Unlimited | Unlimited | White-label + API/export + advanced analytics |

Harga di UI adalah **contoh product positioning**, bukan transaksi aktif.

## Production stack yang direkomendasikan

- Frontend: static web/React/Next.js.
- Auth + database: Supabase atau Firebase.
- Payment: Midtrans, Xendit, atau Stripe.
- API/webhook: serverless functions.
- Storage: object storage untuk asset/avatar.
- Analytics: event tracking per arena, question, mastery, retention.
- White-label: tenant branding + custom domain/subdomain.

> Jangan menyimpan secret key database atau payment provider di frontend GitHub Pages.

## Deployment

Workflow `.github/workflows/pages.yml` akan menjalankan deployment setiap push ke `main`. Repository settings tetap perlu mengizinkan **GitHub Actions / Pages** sebagai source jika Pages belum pernah diaktifkan.

Repository:
https://github.com/1120008/Sistem-Pernapasan-

## Tahap komersialisasi berikutnya

1. Auth guru/siswa.
2. Database multi-tenant.
3. Class + join code persisten.
4. Content authoring: guru dapat membuat/edit arena dan soal.
5. Payment subscription + webhook.
6. White-label per sekolah.
7. Analytics dan laporan PDF/CSV.
8. Admin super-tenant untuk mengelola pelanggan.
9. Custom domain.
10. Privacy, terms, consent, backup, dan audit log.

Current build tetap dapat dimainkan tanpa backend sebagai **MVP/product validation**.
