---
description: Layout delle chiavi del Registro di sistema
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Layout delle chiavi del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4473027b2612d16b3c6daee4f8e708d90b993397b133db111aa55c58e9c4ceb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502291"
---
# <a name="layout-of-the-registry-keys"></a>Layout delle chiavi del Registro di sistema

DirectShow filtri vengono registrati in due posizioni:

-   La DLL che contiene il filtro viene registrata come server COM del filtro. Quando un'applicazione chiama **CoCreateInstance** per creare il filtro, la libreria COM di Microsoft Windows usa questa voce del Registro di sistema per individuare la DLL.
-   È possibile registrare informazioni aggiuntive sul filtro all'interno di una categoria di filtri. Queste informazioni consentono a [System Device Enumerator](system-device-enumerator.md) e [a Filter Mapper](filter-mapper.md) di individuare il filtro.

I filtri non sono necessari per registrare le informazioni aggiuntive sui filtri. Finché la DLL è registrata come server COM, un'applicazione può creare il filtro e aggiungerlo a un grafico di filtri. Tuttavia, se si vuole che il filtro sia individuabile tramite System Device Enumerator o Filter Mapper, è necessario registrare le informazioni aggiuntive.

La voce del Registro di sistema per la DLL ha le chiavi seguenti:


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



La voce del Registro di sistema per le informazioni sul filtro contiene le chiavi seguenti:


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



è il GUID di una categoria di filtri. Vedere [Categorie di filtro.](filter-categories.md) Le informazioni sul filtro vengono suddivise in un formato binario. [**L'interfaccia IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) decomprime questi dati quando cerca un filtro nel Registro di sistema.

Tutti i GUID della categoria di filtro sono elencati nel Registro di sistema sotto la chiave seguente:


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



