---
name: brp-utskick
description: Skapar HTML-formaterade e-postutskick för BRP-systemet, centrerade med 600px bredd och anpassade till Göteborgs Stads grafiska profil.
---

## Översikt
Denna skill hjälper dig att skapa **HTML-formaterade e-postutskick** för BRP-systemet (Boknings- och ResursPlanering).

Allt innehåll är:
- **Centrerat** med **600px bredd**
- **Anpassat till Göteborgs Stads grafiska profil** (färger, typsnitt, logotyp)
- **Kompatibelt** med de flesta e-postklienter

---

## Grundstruktur

### HTML-mall
```html
<html>
<body style="margin:0; padding:0; background-color:#ffffff; font-family:Open Sans, Arial, Helvetica, sans-serif; color:#333333;">
  <!-- Innehåll här -->
</body>
</html>
```

---

## Färger (Göteborgs Stads profil)

| Användning | HEX | RGB | Beskrivning |
|---|---|---|---|
| Bakgrund | #ffffff | 255/255/255 | Vit bakgrund |
| Text | #333333 | 51/51/51 | Mörkgrå text |
| Länkar/Knappar | #005799 | 0/87/153 | Primär blå |
| Länkar hover | #004172 | 0/65/114 | Mörkare blå |
| Bordrar | #d1d9dc | 209/217/220 | Ljusgrå |

---

## Typsnitt
- **Huvudtypsnitt:** `Open Sans, Arial, Helvetica, sans-serif`
- **Rubriker:** 16px-18px
- **Brödtext:** 14px
- **Tabelltext:** 13px
- **Radavstånd:** 20-24px

---

## Mall för BRP-Utskick

### Header med logotyp
```html
<table width="600" cellpadding="0" cellspacing="0" border="0" align="center">
  <tr>
    <td width="200"></td>
    <td width="200" align="center" style="padding-top:20px; padding-bottom:20px;">
      <img src="https://goteborg.se/wps/wcm/connect/e7f82b03-491f-41b9-b740-be2d141886c4/gbg_li_rgb.png?MOD=AJPERES" 
           alt="Göteborgs Stad" width="200" border="0" style="display:block;">
    </td>
    <td width="200"></td>
  </tr>
</table>
```

### Sektion (rubrik + innehåll)
```html
<table width="600" cellpadding="0" cellspacing="0" border="0" align="center">
  <tr>
    <td style="font-size:16px; line-height:22px; font-weight:bold; padding-top:20px; padding-bottom:10px; border-top:1px solid #d1d9dc;">
      Rubrik
    </td>
  </tr>
  <tr>
    <td style="font-size:14px; line-height:20px; padding-bottom:15px;">
      Innehåll här
    </td>
  </tr>
</table>
<br>
```

### Knappar
```html
<a href="[LÄNK]" 
   style="background-color:#005799; color:#ffffff; padding:10px 18px; text-decoration:none; display:inline-block; border-radius:4px;">
  Knapptext
</a>
```

### Listor
```html
<ul style="padding-left:18px; margin:10px 0;">
  <li>Punk 1</li>
  <li>Punk 2</li>
</ul>
```

### Nummererade listor
```html
<ol style="margin-top:8px; padding-left:18px;">
  <li>Steg 1</li>
  <li>Steg 2</li>
</ol>
```

---

## Vanliga Sektioner

### 1. App och Kundwebb
```html
<table width="600" cellpadding="0" cellspacing="0" border="0" align="center">
  <tr>
    <td colspan="2" style="font-size:16px; line-height:22px; font-weight:bold; padding-top:20px; padding-bottom:10px; border-top:1px solid #d1d9dc;">
      App och kundwebb
    </td>
  </tr>
  <tr>
    <td colspan="2" style="font-size:14px; line-height:20px; padding-bottom:15px;">
      <b>Användarnamn:</b> ${customerNumber}<br>
      <b>Lösenord:</b> ÅÅMMDD (Personnummer)
    </td>
  </tr>
  <tr>
    <td width="290" valign="top" style="font-size:14px; line-height:20px; padding-right:20px;">
      <b>Kundwebb</b><br><br>
      <a href="https://goteborg.goactivebooking.com/" 
         style="background-color:#005799; color:#ffffff; padding:10px 18px; text-decoration:none; display:inline-block; border-radius:4px;">
        Gå till kundwebben
      </a>
    </td>
    <td width="290" valign="top" style="font-size:14px; line-height:20px;">
      <b>App</b><br><br>
      <a href="https://applink.brpsystems.net/?link=https%3A%2F%2Fgoteborg.goactivebookings.com&apn=se.brpsystems.mobility" 
         style="background-color:#005799; color:#ffffff; padding:10px 18px; text-decoration:none; display:inline-block; border-radius:4px;">
        Ladda ner appen
      </a>
    </td>
  </tr>
</table>
<br>
```

### 2. Betala med Autogiro
```html
<table width="600" cellpadding="0" cellspacing="0" border="0" align="center">
  <tr>
    <td style="font-size:16px; line-height:22px; font-weight:bold; padding-top:20px; padding-bottom:10px; border-top:1px solid #d1d9dc;">
      Betala med autogiro
    </td>
  </tr>
  <tr>
    <td style="font-size:14px; line-height:20px; padding-bottom:15px;">
      Betala den första fakturan som vanligt. Registrera sedan autogiro via:
      <br><br>
      <a href="https://www.goteborg.se/minasidor" 
         style="background-color:#005799; color:#ffffff; padding:10px 18px; text-decoration:none; display:inline-block; border-radius:4px;">
        Gå till Mina sidor
      </a>
    </td>
  </tr>
</table>
<br>
```

### 3. Frysning av Abonnemang
```html
<table width="600" cellpadding="0" cellspacing="0" border="0" align="center">
  <tr>
    <td style="font-size:16px; line-height:22px; font-weight:bold; padding-top:20px; padding-bottom:10px; border-top:1px solid #d1d9dc;">
      Frysning av abonnemang
    </td>
  </tr>
  <tr>
    <td style="font-size:14px; line-height:20px; padding-bottom:10px;">
      <b>Regler:</b>
      <ul style="margin-top:0; padding-left:18px;">
        <li>Kostar 100 kr (kostnadsfritt vid graviditet i 3 månader)</li>
        <li>Max 60 dagar per år (årskort/månadsabonnemang)</li>
      </ul>
    </td>
  </tr>
</table>
<br>
```

---

## Variabler

### Personlig info
- `${firstName}` - Förnamn
- `${customerNumber}` - Kundnummer

### Produkt
- `${product}` - Produktnamn

### Anläggning
- `${unit.name}` - Anläggningsnamn
- `${unit.website}` - Hemsida
- `${unit.providerCode}` - Anläggnings-ID

---

## Riktlinjer

### Gör så här:
- Använd alltid `width="600"` och `align="center"`
- Använd `cellpadding="0" cellspacing="0" border="0"`
- Använd `display:block;` på bilder
- Testa i flera e-postklienter

### Undvik:
- Färgad text (endast #333333 eller #ffffff)
- Bakgrundsbilder
- JavaScript
- För stora bilder (>1MB)
