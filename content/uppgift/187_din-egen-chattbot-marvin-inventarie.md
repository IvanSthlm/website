---
author: sylvanas
category: python
revision:
  "2018-06-29": (H, aar) Uppdaterade mappstruktur mot kursrepo.
  "2017-06-14": (G, lew) Uppdaterade med en asciinema och ett krav. Förtydligande av uppgift.
  "2015-10-12": (F, mos) Förtydligade (lade till) krav om att spara på fil.
  "2015-09-03": (E, mos) Ändrade max antal till 4 istället för 7 samt tog bort grundkrav
    om att det redan skall finnas 4 i ryggsäcken.
  "2015-08-25": (D, mos) Uppgraderade till dbwebb v2 samt flyttade två krav till extrauppgifter.
  "2015-05-05": (C, mos) Förtydligade att kommunicera via text och inte menyval.
  "2015-02-03": (B, mos) Länkade till artikel med introduktion av JSON.
  "2015-02-02": (A, sylvanas, mos) Första utgåvan i samband med  uppgradering av kursen
    python.
updated: "2015-10-12 08:04:36"
created: "2015-02-02 16:53:39"
...
Din egen chattbot - Marvin - inventarie
==================================

Programmering och problemlösning i Python. Använd listor och fil för att hjälpa Marvin att ha koll på sina inventarier.

<!--more-->


Förkunskaper {#forkunskaper}
-----------------------

Du kan grunderna i Python, listor och filhantering. Du har även byggt [tredje delen av Marvin](uppgift/din-egen-chattbot-marvin-steg-3).



Introduktion {#intro}
-----------------------

<!--
Studera gärna [exemplet för hur man skriver och läser listor till fil](https://github.com/mosbth/python/blob/master/example/file/list-to-file.py) samt [tutorialen om att använda `with` tillsammans med filer](https://github.com/mosbth/python/blob/master/tutorial/with-files.md). Det kan underlätta när du löser uppgiften.
-->
Du skall bygga en ryggsäck till Marvin och du skall spara innehållet i ryggsäcken till fil.

Du skall kommunicera med Marvin via text och inte via ett menyval. 

Du skall istället kommunicera via text, på liknande sätt som du gjorde i [Marvin citat-uppgiften](uppgift/din-egen-chattbot-marvin-steg-3). Så här.

```text
> inv
*marvin svarar med innehållet i inventoriet* 

> inv pick mumintrollet
*marvin svarar med att han tog upp mumintrollet*

> inv drop mumintrollet
*marvin svarar med att han släppte mumintrollet*
```

Se hur det kan se ut när uppgiften är klar:  

[ASCIINEMA src=124668]



Krav {#krav}
-----------------------

Bygg vidare på din Marvin 3.

```bash
# Ställ dig i kurskatalogen
cp -ri me/kmom04/marvin3/* me/kmom05/marvin4
cd me/kmom05/marvin4
```

1. Uppgradera din Marvin så att han kan hantera en *ryggsäck*, eller ett *inventory*, där han kan bära saker.

1. Marvin ska kunna plocka upp vad som helst.

1. Spara innehållet i ryggsäcken i en fil som du döper till `inv.data`.

1. När du börjar så läser du in ryggsäckens innehåll från filen.

1. När du ger inventory-kommandon till Marvin så skall det ske i klartext. Genom att prata med Marvin, via kommandon, så ska han kunna visa och förändra innehållet i sitt *inventory*.

Följande kommandon skall fungera. Notera att Marvin ska kunna plocka upp vad som helst. Nedan visas `flower` **enbart som exempel**.

| Kommando        | Vad händer                       |
|-----------------|----------------------------------|
| inv             | Visa vad som finns i inventoryt och hur många saker det finns där. |
| inv pick flower | Plocka upp en blomma, en *flower*. |
| inv drop flower | Kasta bort blomman.                |



5\. Validera din kod.

```bash
# Ställ dig i kurskatalogen
dbwebb validate marvin4
```

Rätta eventuella fel som dyker upp och validera igen. När det ser grönt ut så är du klar. 



Extrauppgift {#extra}
-----------------------

1\. Lägg till följande kommando.

| Kommando        | Vad händer                       |
|-----------------|----------------------------------|
| inv drop        | kasta bort allt som ligger i inventoryt.|


2\. Marvin ska inte kunna bära mer än 4 saker. Om du ber honom att plocka upp något när han har fullt så ska han svara att han inte kan plocka upp det.


3\. Spara Marvins inventory som JSON istället. Tips: [python/example/json/](https://github.com/mosbth/python/tree/master/example/json) samt [introduktion till JSON (del av kmom06)](kunskap/anvand-externa-moduler-i-python-for-att-hamta-information-pa-webben#json).



Tips från coachen {#tips}
-----------------------

Validera ofta. Så slipper du en massa valideringsfel i slutet av övningen.

Lycka till och hojta till i forumet om du behöver hjälp!




