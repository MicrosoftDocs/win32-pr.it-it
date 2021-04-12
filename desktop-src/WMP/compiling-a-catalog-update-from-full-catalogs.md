---
title: Compilazione di un aggiornamento del catalogo da cataloghi completi
description: Compilazione di un aggiornamento del catalogo da cataloghi completi
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Windows Media Player Online Stores, compilazione di cataloghi
- archivi online, compilazione di cataloghi
- digitare 1 negozi online, compilazione di cataloghi
- Windows Media Player Online Stores, aggiornamenti del catalogo
- archivi online, aggiornamenti del catalogo
- digitare 1 negozi online, aggiornamenti del catalogo
- Windows Media Player Online Stores, cataloghi completi
- archivi online, cataloghi completi
- digitare 1 Online Stores, cataloghi completi
- compilazione di cataloghi
- aggiornamenti del catalogo
- cataloghi completi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336249"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a>Compilazione di un aggiornamento del catalogo da cataloghi completi

Un aggiornamento del catalogo contenente le modifiche tra due versioni di un catalogo compilato può essere creato usando la sintassi seguente, dove *path1* è la directory che contiene il primo catalogo, *path2* è la directory che contiene il secondo catalogo e il debug può essere incluso facoltativamente per visualizzare informazioni dettagliate sull'errore sullo schermo. I file di catalogo devono essere in formato non compresso. il nome file del catalogo compilato sarà Catalog. WMDB, anziché Catalog. WMDB. LZ.


```C++
catcomp diff <path1> <path2> [debug]
```



Se, ad esempio, la directory C: \\ Catalog210 \\ contiene la versione 210 di un catalogo compilato completo e C: \\ Catalog211 \\ contiene la versione 211, il comando seguente crea un file di differenze che contiene le modifiche tra le due versioni:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



Per visualizzare informazioni dettagliate sull'errore, è possibile aggiungere il parametro di debug facoltativo come indicato di seguito:


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



Se la compilazione ha esito positivo, catcomp.exe crea i file di output elencati di seguito e li salva nella directory che contiene il primo catalogo.



| Nome file             | Descrizione                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Catalog. diff          | File delle differenze compilate non compresso.                                                                                                                                                           |
| Catalog. diff. LZ       | Versione compressa del file di aggiornamento del catalogo. Il plug-in può assegnare il percorso di questo file a Windows Media Player in [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). |
| Catalog. WMDB. Delta    | File di output intermedio. Non utilizzato da Windows Media Player                                                                                                                                       |
| Catalog. WMDB. Modified | File di output intermedio. Non utilizzato da Windows Media Player                                                                                                                                       |



 

 

 




