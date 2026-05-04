# Éttermi rendelés kezelő

Étterem rendelés-kezelő rendszer — szoftverfejlesztő technikum vizsgaremek (WPF + ASP.NET Core)

Egy közepes méretű étterem napi működését támogató rendelés-kezelő rendszer.
A pincérek WPF asztali alkalmazásban dolgoznak (érintőképernyős kassza),
a menedzser pedig böngészőből, ASP.NET Core webes felületen — közös háttérrendszerrel.

## Készítők

- **Név:** Nagy Anna
- **Név:** Kiss Péter
- **Iskola:** BGSZC Logisztikai és Kereskedelmi Technikum és Szakképző Iskola, Budapest
- **tanév:** 2026/2027
- **Vizsgaidőszak:** 2027. május-június

## Architektúra

- `Etterem.Asztali` — menedzseri webes felület (ASP.NET Core MVC, .NET 8)
- `Etterem.WebClient` — pincéri webes felület (React + TypeScript)
- `Etterem.Domain` — Express alkalmazás, a háttérrendszer (Node.js, Express, TypeScript)

## Telepítési feltételek

- .NET 8 SDK
- Visual Studio 2022 (vagy `dotnet` CLI)
- MáriaDb (alapértelmezett)
- node.js v24 vagy újabb a backendhez

## Build és futtatás

```bash
dotnet restore
dotnet build
 
# Web API indítása (a kliensek ezzel beszélgetnek)
cd Etterem.Domain
npm run dev
 
# WPF kliens indítása
dotnet run --project src/Etterem.WpfClient
```

## Dokumentáció

- Felhasználói kézikönyv: `docs/felhasznaloi-kezikonyv.md`
- Fejlesztői dokumentáció: `docs/fejlesztoi-dokumentacio.md`
- Adatmodell: `docs/adatmodell.md`

## Licenc

MIT — lásd [LICENSE](LICENSE).
