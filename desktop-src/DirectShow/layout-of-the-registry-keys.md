---
description: Layout delle chiavi del registro di sistema
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Layout delle chiavi del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5783a9f083f639912188f418238f46a5d45ed922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303710"
---
# <a name="layout-of-the-registry-keys"></a>Layout delle chiavi del registro di sistema

I filtri DirectShow sono registrati in due posizioni:

-   La DLL che contiene il filtro è registrata come server COM del filtro. Quando un'applicazione chiama **CoCreateInstance** per creare il filtro, la libreria COM di Microsoft Windows utilizza questa voce del registro di sistema per individuare la dll.
-   È possibile registrare informazioni aggiuntive sul filtro all'interno di una categoria di filtro. Queste informazioni consentono a [System Device Enumerator](system-device-enumerator.md) e a [Filter Mapper](filter-mapper.md) di individuare il filtro.

I filtri non sono necessari per registrare le informazioni aggiuntive sul filtro. Finché la DLL viene registrata come server COM, un'applicazione può creare il filtro e aggiungerlo a un grafico di filtro. Tuttavia, se si desidera che il filtro sia individuabile dall'enumeratore del dispositivo di sistema o dal mapper del filtro, è necessario registrare le informazioni aggiuntive.

La voce del registro di sistema per la DLL presenta le chiavi seguenti:


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



La voce del registro di sistema per le informazioni sul filtro presenta le chiavi seguenti:


```
HKEY_CLASSES_ROOT
    CLSID
        Category
            Instance
                Filter CLSID
                    REG_SZ: CLSID = Filter CLSID
                    REG_BINARY: FilterData = Filter information
                    REG_SZ: FriendlyName = Friendly name
```




```
Category
```



GUID di una categoria di filtro. (Vedere [categorie di filtro](filter-categories.md)). Le informazioni sul filtro vengono compresse in un formato binario. L'interfaccia [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) decomprime questi dati quando cerca un filtro nel registro di sistema.

Tutti i GUID della categoria Filter sono elencati nel registro di sistema nella chiave seguente:


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



