# Lemmikupood

Brauserimäng 7-aastasele: mängija on lemmikuloomapoe müüja abiline. Üks fail, ilma välisteekide ja pildifailideta.

## Käivitamine

Ava `index.html` brauseris (iPad Safari rõhtasendis või arvuti brauser). Server pole vaja.

## Mängutsükkel

1. Klient tuleb leti äärde, soov on piltidena (1 kuni 3 kaupa).
2. Kaubad riiulilt korvi (vajutus). Kui korv on õige, läheb mäng ise edasi.
3. Vali õige kogusumma (3 varianti).
4. Klient maksab. Tagasi andmisel vajuta kassasahtlis münte ja rahatähti (1, 2, 5, 10 €).
5. Õige tehing annab raha ja tähe. Päevas on 5 klienti, siis päevakokkuvõte ja pood.

Vale vastus: "Proovi uuesti!", raha ei kao. Teise vea järel ilmub abi: mündid, mida saab vajutades ükshaaval kokku lugeda.

## Raskusastmed

| Aste | Sisu |
|---|---|
| 1 | üks kaup, klient maksab täpselt |
| 2 | kaks kaupa, summa kuni 10 € |
| 3 | tagasi andmine 10 € pealt |
| 4 | kolm kaupa, summa kuni 20 €, tagasi andmine 20 € pealt |

Uus aste avaneb pärast 5 õiget tehingut.

## Poed ja ülesanded

Iga pood on üks ülesanne: osta kõik täiendused ja abilised. Kui ülesanne on täiesti tehtud, avaneb järgmine, uhkem pood.

1. Väike lemmikupood: 4 uut kaupa, riiul, kaunistused, poekass, abiline Mari
2. Linna lemmikupood: suur riiul, taimed, poekoer, abilised Peeter ja Liisa
3. Lemmikute loss: kuldne riiul, purskkaev, papagoi, abilised Jaan ja Printsess

Täiendused: riiul (rohkem kaupa), kaunistused ja lemmikud (+ raha iga kliendi eest), abilised (toovad iga päev kaupa). Kaupa tellitakse poes, 1 € tükk.

## Tehnika

- Pointer events (puute ja hiir sama koodiga), topeltpuute suum ja teksti valimine keelatud
- Edenemine `localStorage`'is (try/catch, mäng töötab ka ilma), nupp "Alusta otsast"
- Heli Web Audio API-ga, vaigistusnupp
- Andmepõhine: kaubad, poed ja täiendused on faili alguses (`GOODS`, `SHOPS`), tasakaalu saab muuta numbreid vahetades
