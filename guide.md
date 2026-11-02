# Guide: Starta webbläsaren och surfa till Aftonbladet

## Steg 1: Öppna webbläsaren
- Tryck på `Ctrl + Alt + T` för att öppna terminalen
- Skriv `firefox` eller `google-chrome` (beroende på vilken webbläsare du har installerad)
- Tryck Enter

## Steg 2: Surfa till Aftonbladet
- I webbläsarens adressfält, skriv: `https://www.aftonbladet.se`
- Tryck Enter

## Steg 3: Pusha ändringar till Git

```bash
# Lägg till den nya filen i staging
.git add guide.md

# Commit ändringarna
git commit -m "Lade till guide för Aftonbladet"

# Pusha till remote repository
git push origin main
```