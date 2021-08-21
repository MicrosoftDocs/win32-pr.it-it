---
title: Categorizzazione in base alle funzionalità dei componenti
description: Le categorie di componenti possono essere usate per visualizzare un subset di tutti i componenti installati.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251e8197c00a39c8d9666dee7122be7445402fc84ce7b3508987bcf79f27df15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048749"
---
# <a name="categorizing-by-component-capabilities"></a>Categorizzazione in base alle funzionalità dei componenti

Le categorie di componenti possono essere usate per visualizzare un subset di tutti i componenti installati. Ogni categoria di componenti è identificata da un GUID, definito ID categoria (CATID). A ogni CATID è associato un elenco di nomi leggibili e con tag delle impostazioni locali. Un elenco dei CATID e dei nomi leggibili viene archiviato in una posizione nota nel Registro di sistema.

Ad esempio, tutti i componenti che implementano la funzionalità per l'incorporamento di documenti OLE possono essere classificati all'interno di una categoria di componenti. In passato questi oggetti sarebbero stati identificati dalla chiave "Insertable" nel Registro di sistema. Per usare invece le categorie di componenti, al Registro di sistema verranno aggiunte le informazioni seguenti:

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

Ogni classe che implementa la funzionalità corrispondente a una categoria di componenti elenca l'ID categoria per tale categoria all'interno della chiave CLSID nel Registro di sistema. Poiché un singolo componente può supportare un'ampia gamma di funzionalità, i componenti possono appartenere a più categorie di componenti. Ad esempio, un particolare controllo OLE potrebbe supportare tutte le funzionalità necessarie per partecipare come incorporamento di documenti OLE, microsoft Visual Basic data binding e funzionalità Internet. Per un controllo di questo tipo, nella chiave CLSID del Registro di sistema vengono archiviate le informazioni seguenti:

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

Con queste informazioni, un contenitore può enumerare i controlli installati in un sistema e visualizzare solo i controlli che supportano la funzionalità richiesta dal contenitore. L'uso delle categorie di componenti consente di classificare i componenti in base alla funzionalità implementata del componente.

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

[Gestione categorie componenti](the-component-categories-manager.md)
</dt> </dl>

 

 




