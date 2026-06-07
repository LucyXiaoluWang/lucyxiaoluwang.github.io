# Lucy Xiaolu Wang — personal website (GitHub Pages)

A self-contained static rebuild of lucyxiaoluwang.com. One HTML file, no
external fonts or scripts, so it loads reliably (including from China).

---

## 1. Folder structure you want on GitHub

    LucyXiaoluWang.github.io/
    ├── index.html        <- already done
    ├── assets/
    │   └── lucy-photo.jpg
    └── files/
        ├── cv.pdf
        ├── slides-organization-innovation.pdf
        ├── slides-marketing-authorization.pdf
        ├── slides-procurement.pdf
        ├── slides-mpp-60min.pdf
        ├── slides-cannabis-licensing.pdf
        ├── slides-opioid-hit.pdf
        └── slides-secret-menu.pdf

The repo MUST be named exactly `LucyXiaoluWang.github.io` (your username +
.github.io) so it serves at the root.

---

## 2. Download your files from Wix FIRST (do this while the Wix site is still up)

Open each link, save the file, and rename it to the target name. Drop photo
into `assets/`, everything else into `files/`. (If any link 404s, grab the file
from your Wix Media Manager instead.)

PHOTO  -> assets/lucy-photo.jpg
  https://static.wixstatic.com/media/b7b79b_1fe083829bf44cb8804c7c5634cfc791~mv2.jpg

CV     -> files/cv.pdf
  https://www.lucyxiaoluwang.com/_files/ugd/b7b79b_e23a5274021f49db9a13b17ed614320a.pdf

SLIDES:
  files/slides-organization-innovation.pdf
    https://www.lucyxiaoluwang.com/_files/ugd/b7b79b_f8b6f0ae2e9e48e882968211cd626402.pdf
  files/slides-marketing-authorization.pdf
    https://www.lucyxiaoluwang.com/_files/ugd/b7b79b_5305f5fa16cc4e4eaf0809abe57796a0.pdf
  files/slides-procurement.pdf
    https://www.lucyxiaoluwang.com/_files/ugd/b7b79b_bdda0b3cf5584e5e8945bcd925961b1d.pdf
  files/slides-mpp-60min.pdf
    https://www.lucyxiaoluwang.com/_files/ugd/b7b79b_9e07885a16074a97815acc6133023d4a.pdf
  files/slides-cannabis-licensing.pdf
    https://www.lucyxiaoluwang.com/_files/ugd/b7b79b_d2b41812a8b049a09520f1434c5b5711.pdf
  files/slides-opioid-hit.pdf
    https://www.lucyxiaoluwang.com/_files/ugd/b7b79b_ee08362f82184626acfc8e0e61e2f99c.pdf
  files/slides-secret-menu.pdf
    https://www.lucyxiaoluwang.com/_files/ugd/b7b79b_5a51e91f593e44ca9d4bfed0303f7972.pdf

(If you'd rather not bother with a slide deck, just delete its link line in
index.html — the published paper links all still work without it.)

---

## 3. Publish on GitHub Pages (laptop; Claude Code can do these steps for you)

1. Sign in to GitHub. Create a new PUBLIC repo named `LucyXiaoluWang.github.io`.
2. Upload index.html, the assets/ folder, and the files/ folder
   (or `git add . && git commit -m "site" && git push`).
3. Repo Settings -> Pages -> Build and deployment -> Source: "Deploy from a
   branch" -> Branch: main -> /(root) -> Save.
4. Wait ~1 minute. Your site is live at https://lucyxiaoluwang.github.io

---

## 4. Point lucyxiaoluwang.com at it (DNS — do this in Wix, domain stays at Wix)

A) In GitHub: repo Settings -> Pages -> "Custom domain" -> type
   `www.lucyxiaoluwang.com` -> Save. Leave "Enforce HTTPS" checked once it lets you.

B) In Wix: go to your domain's DNS / advanced records and set:

   Four A records (host @ / root), each pointing to one IP:
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153

   One CNAME record:
     host: www   ->   value: lucyxiaoluwang.github.io

   (Optional, IPv6 — add AAAA records for host @:)
     2606:50c0:8000::153
     2606:50c0:8001::153
     2606:50c0:8002::153
     2606:50c0:8003::153

   Remove any old A/CNAME records Wix had pointing the domain at Wix hosting.

DNS usually updates within minutes but can take up to 24h. After it resolves,
GitHub auto-issues a free HTTPS certificate.

---

## 5. Wix housekeeping (don't skip)

- Disable AUTO-RENEWAL on the Premium WEBSITE plan now (stops the ~$898 charge).
- KEEP the domain subscription active (~$15/yr) so you don't lose the domain.
- Do NOT start a registrar transfer right before traveling — not needed for the
  site to work. Move the domain to a cheaper registrar (Cloudflare/Porkbun)
  later if you want.
- Your Wix site stays live until ~July 6, so it's a fallback while DNS switches.

---

## Editing later

Everything is in index.html. To add a paper, copy one `<div class="paper">…</div>`
block and edit the text/links. To update from China, edit the file on GitHub's
web editor (pencil icon) — simplest, no tools needed — ideally over a VPN.
