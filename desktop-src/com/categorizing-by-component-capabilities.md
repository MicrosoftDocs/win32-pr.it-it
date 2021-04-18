---
title: Categorizzazione in base alle funzionalità del componente
description: È possibile utilizzare le categorie di componenti per visualizzare un subset di tutti i componenti installati.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff44e03e9eae0226ac57279c37d4a5dfd32fc6bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297959"
---
# <a name="categorizing-by-component-capabilities"></a>Categorizzazione in base alle funzionalità del componente

È possibile utilizzare le categorie di componenti per visualizzare un subset di tutti i componenti installati. Ogni categoria di componenti è identificata da un GUID, indicato come ID di categoria (CATId). Ogni CATId dispone di un elenco di nomi a cui è stato assegnato un nome leggibile dalle impostazioni locali. Un elenco di CATID e i nomi leggibili sono archiviati in una posizione nota nel registro di sistema.

Ad esempio, tutti i componenti che implementano la funzionalità per l'incorporamento di documenti OLE possono essere classificati all'interno di una categoria di componenti. In passato, questi oggetti venivano identificati dalla chiave "Insertable" nel registro di sistema. Per usare invece le categorie di componenti, al registro di sistema vengono aggiunte le informazioni seguenti:

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

Ogni classe che implementa la funzionalità corrispondente a una categoria di componenti elenca l'ID di categoria per tale categoria all'interno della chiave CLSID nel registro di sistema. Poiché un singolo componente può supportare un'ampia gamma di funzionalità, i componenti possono appartenere a più categorie di componenti. Ad esempio, un particolare controllo OLE potrebbe supportare tutte le funzionalità necessarie per partecipare come incorporamento di documenti OLE, Microsoft Visual Basic data binding e funzionalità Internet. Un controllo di questo tipo avrebbe memorizzato le informazioni seguenti nella relativa chiave CLSID nel registro di sistema:

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

Con queste informazioni, un contenitore può enumerare i controlli installati in un sistema e visualizzare solo i controlli che supportano la funzionalità richiesta dal contenitore. L'uso delle categorie di componenti consente di categorizzare i componenti in base alla funzionalità implementata del componente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione di icone a una categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizzazione in base alle funzionalità del contenitore](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classi e associazioni predefinite](default-classes-and-associations.md)
</dt> <dt>

[Definizione delle categorie di componenti](defining-component-categories.md)
</dt> <dt>

[Gestione categorie di componenti](the-component-categories-manager.md)
</dt> </dl>

 

 




