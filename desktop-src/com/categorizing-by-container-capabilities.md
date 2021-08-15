---
title: Categorizzazione in base alle funzionalità del contenitore
description: I componenti spesso richiedono determinate funzionalità dal contenitore e non funzionano con un contenitore che non fornisce il supporto.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67811a40c2c1bbffd4529b3f7c885a0d3e2bea19bda04035ffb80b601c266807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310888"
---
# <a name="categorizing-by-container-capabilities"></a>Categorizzazione in base alle funzionalità del contenitore

I componenti spesso richiedono determinate funzionalità dal contenitore e non funzionano con un contenitore che non fornisce il supporto. L'interfaccia utente deve filtrare i componenti che richiedono funzionalità non supportate dal contenitore. A tale scopo, i componenti possono essere classificati in base alla funzionalità contenitore richiesta.

Un esempio di componenti che richiedono funzionalità dal contenitore e non funzionano nei contenitori che non supportano tale funzionalità sono semplici controlli OLE con frame. La categorizzazione in base alle funzionalità del contenitore viene eseguita da una chiave del Registro di sistema aggiuntiva all'interno della chiave CLSID del componente:

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

Come illustrato in questo esempio, un componente può appartenere a categorie di componenti che indicano funzionalità supportate e a categorie di componenti che indicano le funzionalità necessarie.

Nell'esempio seguente il controllo pulsante è un controllo OLE generico che non supporta alcuna funzionalità aggiuntiva. Funzionerà in qualsiasi contenitore di controlli OLE.

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

Confrontare l'esempio precedente con l'esempio successivo in cui MyDBControl può usare Visual Basic data binding se il contenitore lo supporta. Tuttavia, è stato definito in modo che funzioni in contenitori che non supportano Visual Basic data binding (ad esempio da un'API di database diversa):

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

Il controllo GroupBox è un controllo frame semplice. Si basa sul contenitore che implementa [**l'interfaccia ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) e funzionerà correttamente solo in tali contenitori:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

Un contenitore che supporta Visual Basic controlli associati a dati ma non supporta controlli frame semplici specifica il controllo CATID e IL CATID VBDatabound nell'interfaccia utente \_ \_ del controllo di inserimento. L'elenco dei controlli visualizzati all'utente conterrà il pulsante CLSID \_ e il CLSID \_ MyDBControl. GroupBox \_ CLSID non viene visualizzato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione di icone a una categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizzazione in base alle funzionalità dei componenti](categorizing-by-component-capabilities.md)
</dt> <dt>

[Classi e associazioni predefinite](default-classes-and-associations.md)
</dt> <dt>

[Definizione delle categorie di componenti](defining-component-categories.md)
</dt> <dt>

[Gestione categorie componenti](the-component-categories-manager.md)
</dt> </dl>

 

 




