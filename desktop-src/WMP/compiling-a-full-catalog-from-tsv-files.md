---
title: Compilazione di un catalogo completo da file TSV
description: Compilazione di un catalogo completo da file TSV
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Windows Media Player Online Stores, compilazione di cataloghi
- archivi online, compilazione di cataloghi
- digitare 1 negozi online, compilazione di cataloghi
- Windows Media Player Online Stores, file TSV
- archivi online, file TSV
- digitare 1 archivi online, file TSV
- Windows Media Player Online Stores, catcomp.exe
- archivi online, catcomp.exe
- digitare 1 Store online, catcomp.exe
- catcomp.exe
- compilazione di cataloghi
- file con valori delimitati da tabulazioni (TSV)
- File TSV (con valori delimitati da tabulazioni)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b68af019a5e2302f52f615d5a1dba2180e27cfe5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299379"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a>Compilazione di un catalogo completo da file TSV

I nuovi cataloghi vengono creati da un set di file con valori delimitati da tabulazioni (TSV). I file devono essere in formato Unicode. Inserire i file TSV richiesti elencati di seguito in una cartella (l'argomento del percorso di input per catcomp.exe) e chiamare catcomp.exe usando la sintassi seguente:


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



Se non viene specificato un numero di versione, il numero di versione verrà impostato su 0. Se non viene specificato alcun ID delle impostazioni locali, vengono usate le impostazioni locali del sistema. Se viene fornito un solo argomento numerico facoltativo, si presuppone che corrisponda al numero di versione. Se viene specificato debug, l'output sullo schermo fornirà informazioni di diagnostica più dettagliate.

Ad esempio, il codice seguente compila un catalogo dai file in C: \\ CatalogData \\ 210 e assegna al catalogo un numero di versione di 210:


```C++
catcomp C:\CatalogData\210 210
```



Per visualizzare messaggi di errore più dettagliati, è possibile aggiungere l'argomento facoltativo debug, come indicato di seguito:


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a>File TSV richiesti

Ognuno dei seguenti file deve essere presente, ma è possibile usare un file vuoto se non sono presenti dati per un file. Ad esempio, se il catalogo non contiene canali radio, radio.csv può essere vuoto. I file devono essere denominati esattamente come elencato.

[track.csv](track-csv.md)

[album.csv](album-csv.md)

[artist.csv](artist-csv.md)

[genre.csv](genre-csv.md)

[subgenre.csv](subgenre-csv.md)

[list.csv](list-csv.md)

[listitem.csv](listitem-csv.md)

[radio.csv](radio-csv.md)

> [!Note]  
> Sebbene i nomi file debbano includere estensioni CSV, i file non sono in formato CSV (valori separati da virgola). È necessario che i file siano in formato TSV (Tab Separated Values).

 

Se la compilazione ha esito positivo, catcomp.exe crea tre file di output.



| Nome file                   | Descrizione                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Catalog. WMDB                | Catalogo compilato non compresso.                                                                                                                                                      |
| Catalog. WMDB. LZ             | Catalogo in formato compresso. Il plug-in può assegnare il percorso di questo file a Windows Media Player in [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). |
| \_words.txt univoca compilata \_ | Un file di output intermedio. Non utilizzato da Windows Media Player.                                                                                                                      |



 

 

 




