---
title: Compilazione di un aggiornamento del catalogo da cataloghi completi
description: Compilazione di un aggiornamento del catalogo da cataloghi completi
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Windows Media Player negozi online, compilazione di cataloghi
- negozi online, compilazione di cataloghi
- tipo 1 negozi online, compilazione di cataloghi
- Windows Media Player online store, aggiornamenti del catalogo
- negozi online, aggiornamenti del catalogo
- tipo 1 negozi online, aggiornamenti del catalogo
- Windows Media Player online, cataloghi completi
- negozi online, cataloghi completi
- tipo 1 negozi online, cataloghi completi
- compilazione di cataloghi
- aggiornamenti del catalogo
- cataloghi completi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306412d98f315a6a63aa40974b03a51a388b6db5c9e09c8d5b8907ef2cc15704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763951"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a>Compilazione di un aggiornamento del catalogo da cataloghi completi

È possibile creare un aggiornamento del catalogo contenente le modifiche tra due versioni di un catalogo compilato usando la sintassi seguente, dove *path1* è la directory contenente il primo catalogo, *path2* è la directory contenente il secondo catalogo e il debug può essere incluso facoltativamente per visualizzare informazioni dettagliate sugli errori sullo schermo. I file del catalogo devono essere in formato non compresso. Il nome file del catalogo compilato sarà catalog.wmdb, anziché catalog.wmdb.lz.


```C++
catcomp diff <path1> <path2> [debug]
```



Ad esempio, se la directory C: Catalog210 contiene la versione 210 di un catalogo compilato completo e \\ \\ C: \\ Catalog211 contiene la versione 211, il comando seguente crea un file delle differenze che contiene le modifiche tra le due \\ versioni:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



Per visualizzare informazioni dettagliate sugli errori, è possibile aggiungere il parametro di debug facoltativo come indicato di seguito:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



Se la compilazione ha esito positivo, catcomp.exe crea i file di output elencati di seguito e li salva nella directory che contiene il primo catalogo.



| Nome file             | Descrizione                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| catalog.diff          | File delle differenze compilato non compresso.                                                                                                                                                           |
| catalog.diff.lz       | Versione compressa del file di aggiornamento del catalogo. Il plug-in può fornire il percorso di questo file Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). |
| catalog.wmdb.delta    | File di output intermedio. Non usato da Windows Media Player                                                                                                                                       |
| catalog.wmdb.modified | File di output intermedio. Non usato da Windows Media Player                                                                                                                                       |



 

 

 




