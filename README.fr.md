# ☢️ Fallout Pip-Boy — Bruce Theme

<p align="center">🇺🇸 <a href="README.md">English</a> · 🇫🇷 <b>Français</b></p>

[![Bruce firmware](https://img.shields.io/badge/firmware-Bruce-8A2BE2?logo=github)](https://github.com/BruceDevices/firmware) [![Device](https://img.shields.io/badge/device-LilyGO%20T--Embed%20CC1101-1E90FF)](https://github.com/BruceDevices/firmware) [![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

Un thème UI **Fallout Pip-Boy** pour le firmware **[Bruce](https://github.com/BruceDevices/firmware)** sur LilyGO T-Embed CC1101 (320×170). Cadre métal rouillé, CRT vert phosphore, Vault Boy dans le coin. Chaque entrée affiche un picto vert à gauche et une pile **terminal VT323** à droite : menu précédent (petit), courant (grand), suivant (petit).

![Fallout Pip-Boy theme](docs/hero.png)

## 🎮 Rendu / Look

Le libellé du menu est **intégré dans l'image** (`label: 0`), façon terminal Pip-Boy :

- 🟢 **Picto vert** de l'entrée courante à gauche (halo phosphore + scanlines CRT).
- 🔠 À droite, de haut en bas : **précédent** (petite police) · **COURANT** (très grande) · **suivant** (petite police).
- ⚙️ 14 pictos dessinés à la main : WiFi, BLE, RF, NRF24, LoRa, IR, Ethernet, GPS, RFID, Files, Scripts, Clock, Others, Config (+ FM & Connect).

## 📦 Contenu

`Fallout_PipBoy/` contient **4 tailles** (une par gabarit d'écran Bruce), chacune avec **16 PNG** + son `.json` :

| Dossier | Image | Écran cible |
|---|---|---|
| `105px/` | 240×105 | M5StickC Plus (240×135) |
| `140px/` | 320×140 | **T-Embed CC1101 / Cardputer (320×170)** |
| `180px/` | 320×180 | écrans ~320×210 |
| `192px/` | 320×192 | écrans ~320×222 |

> ℹ️ **Barre d'état** — Bruce réserve **30 px en haut** (batterie / heure / WiFi). La bonne taille = **hauteur de ton écran − 30**. Pour le **T-Embed CC1101 (320×170) → `140px`**. Le firmware place l'image sous la barre d'état, donc les icônes ne mordent pas le cadre et ne clignotent pas au changement de menu.

## 🚀 Installation

1. Copie le dossier **`Fallout_PipBoy`** à la racine de la carte SD.
2. Sur l'appareil : **Config → UI Theme → `Fallout_PipBoy/<taille>/Theme_Fallout_PipBoy.json`** (taille = hauteur écran − 30 ; **`140px` pour le T-Embed CC1101**).
3. Via WiFi : **Files → WebUI**, upload le dossier, puis sélectionne le `.json`.

## ⚠️ Ordre du menu (voisins)

Les libellés **précédent / suivant** sont peints dans chaque image selon l'**ordre par défaut** du menu Bruce T-Embed CC1101 :
`WiFi → BLE → RF → NRF24 → LoRa → IR → Ethernet → GPS → RFID → Files → Scripts → Clock → Others → Config` (en boucle).

Si tu **désactives ou réordonnes** des menus (`Config → Main Menu`), les voisins affichés ne correspondront plus. Dans ce cas, ouvre une issue avec ton ordre exact et je régénère le thème pour ta config.

## 🛒 Matériel

*Liens partenaires Amazon : si vous achetez via ces liens, le projet touche une petite commission, sans surcoût pour vous.*

<table>
<tr>
<td align="center" width="33%">
  <a href="https://www.amazon.fr/dp/B0D45MSMJR?linkCode=ll2&amp;tag=koua29bfallouttheme-21&amp;ref_=as_li_ss_tl"><img src="docs/amazon-B0D45MSMJR.jpg" width="200" alt="Batterie Anker 545 (10 000 mAh)"></a><br>
  <b><a href="https://www.amazon.fr/dp/B0D45MSMJR?linkCode=ll2&amp;tag=koua29bfallouttheme-21&amp;ref_=as_li_ss_tl">Batterie Anker 545 (10 000 mAh)</a></b><br><sub>Pour faire tourner le T-Embed loin d'une prise</sub>
</td>
<td align="center" width="33%">
  <a href="https://www.amazon.fr/dp/B0C1FCZM94?linkCode=ll2&amp;tag=koua29bfallouttheme-21&amp;ref_=as_li_ss_tl"><img src="docs/amazon-B0C1FCZM94.jpg" width="200" alt="Antenne SMA 433 MHz (lot de 2)"></a><br>
  <b><a href="https://www.amazon.fr/dp/B0C1FCZM94?linkCode=ll2&amp;tag=koua29bfallouttheme-21&amp;ref_=as_li_ss_tl">Antenne SMA 433 MHz (lot de 2)</a></b><br><sub>Antenne sub-GHz pour la radio CC1101</sub>
</td>
<td align="center" width="33%">
  <a href="https://www.amazon.fr/dp/B0B7NVMBPL?linkCode=ll2&amp;tag=koua29bfallouttheme-21&amp;ref_=as_li_ss_tl"><img src="docs/amazon-B0B7NVMBPL.jpg" width="200" alt="microSD SanDisk 64 Go (lot de 2)"></a><br>
  <b><a href="https://www.amazon.fr/dp/B0B7NVMBPL?linkCode=ll2&amp;tag=koua29bfallouttheme-21&amp;ref_=as_li_ss_tl">microSD SanDisk 64 Go (lot de 2)</a></b><br><sub>Pour les thèmes, scripts et captures Bruce</sub>
</td>
</tr>
</table>

<sub>En tant que Partenaire Amazon, je réalise un bénéfice sur les achats remplissant les conditions requises.</sub>

## 🎨 Crédits

- Fond Pip-Boy & thème par **koua29**.
- Police de rendu : **[VT323](https://fonts.google.com/specimen/VT323)** (SIL Open Font License).
- Tourne sur l'excellent **[Bruce firmware](https://github.com/BruceDevices/firmware)**.

## ☕ Un café ?

Si ce thème te plaît :

<img src="docs/paypal-qr.png" width="180" alt="PayPal" />

## 📄 Licence

**MIT** — voir [LICENSE](LICENSE). Fallout / Pip-Boy / Vault Boy sont des marques de Bethesda ; ce thème est un projet fan non officiel, non affilié.
