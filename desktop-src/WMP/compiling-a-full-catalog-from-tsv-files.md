---
title: Compilazione di un catalogo completo da file TSV
description: Compilazione di un catalogo completo da file TSV
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Windows Media Player negozi online, compilazione di cataloghi
- negozi online, compilazione di cataloghi
- tipo 1 negozi online, compilazione di cataloghi
- Windows Media Player negozi online, file TSV
- negozi online, file TSV
- tipo 1 negozi online, file TSV
- Windows Media Player negozi online, catcomp.exe
- negozi online, catcomp.exe
- Tipo 1 di negozi online, catcomp.exe
- catcomp.exe
- compilazione di cataloghi
- File con valori delimitati da tabulazioni (TSV)
- File TSV (con valori separati da tabulazioni)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c5bc0648c19c3c8a6f9ddb819d77e48235bcd684d4911bc8a324a109c49daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863801"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a>Compilazione di un catalogo completo da file TSV

I nuovi cataloghi vengono creati da un set di file TSV (Tab-Separated-Value). I file devono essere in formato Unicode. Inserire i file TSV necessari elencati di seguito in una cartella (l'argomento del percorso di input catcomp.exe) e chiamare catcomp.exe usando la sintassi seguente:


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



Se non viene specificato un numero di versione, il numero di versione verrà impostato su 0. Se non viene specificato alcun ID delle impostazioni locali, vengono usate le impostazioni locali del sistema. Se viene specificato un solo argomento facoltativo numerico, si presuppone che sia il numero di versione. Se si specifica debug, l'output sullo schermo fornirà informazioni di diagnostica più dettagliate.

Ad esempio, il codice seguente compilerà un catalogo dai file in C: CatalogData 210 e assegna al catalogo un numero di versione \\ \\ 210:


```C++
catcomp C:\CatalogData\210 210
```



Per visualizzare messaggi di errore più dettagliati, è possibile aggiungere l'argomento di debug facoltativo, come indicato di seguito:


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a>File TSV necessari

Ognuno dei file seguenti deve essere presente, ma è possibile usare un file vuoto se non sono presenti dati per un file. Ad esempio, se il catalogo non contiene canali radio, radio.csv può essere vuoto. I file devono essere denominati esattamente come elencati.

[track.csv](track-csv.md)

[album.csv](album-csv.md)

[artist.csv](artist-csv.md)

[genre.csv](genre-csv.md)

[subgenre.csv](subgenre-csv.md)

[list.csv](list-csv.md)

[listitem.csv](listitem-csv.md)

[radio.csv](radio-csv.md)

> [!Note]  
> Anche se i nomi di file devono .csv, i file non sono in formato CSV (Comma Separated Values). I file devono essere in formato TSV (Tab Separated Values).

 

Se la compilazione ha esito positivo, catcomp.exe tre file di output.



| Nome file                   | Descrizione                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| catalog.wmdb                | Catalogo compilato non compresso.                                                                                                                                                      |
| catalog.wmdb.lz             | Catalogo in formato compresso. Il plug-in può fornire il percorso di questo file Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). |
| file \_ univoci \_ compilatiwords.txt | File di output intermedio. Non usato da Windows Media Player.                                                                                                                      |



 

 

 




