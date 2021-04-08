---
title: Categorizzazione in base alle funzionalità del contenitore
description: I componenti richiedono spesso determinate funzionalità dal contenitore e non funzionano con un contenitore che non fornisce il supporto.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987546c20ff77a40666bb74689466a15fab989a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045282"
---
# <a name="categorizing-by-container-capabilities"></a>Categorizzazione in base alle funzionalità del contenitore

I componenti richiedono spesso determinate funzionalità dal contenitore e non funzionano con un contenitore che non fornisce il supporto. L'interfaccia utente deve filtrare i componenti che richiedono funzionalità non supportate dal contenitore. A tale scopo, i componenti possono essere classificati in base alla funzionalità del contenitore richiesta.

Un esempio di componenti che richiedono funzionalità dal contenitore e che non funzionano in contenitori che non supportano tale funzionalità sono semplici controlli OLE frame. La categorizzazione in base alle funzionalità del contenitore viene eseguita da un'altra chiave del registro di sistema all'interno della chiave CLSID del componente:

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

Come illustrato in questo esempio, un componente può appartenere a categorie di componenti che indicano le funzionalità supportate, oltre alle categorie di componenti che indicano la funzionalità richiesta.

Nell'esempio seguente il controllo Button è un controllo OLE generico che non supporta alcuna funzionalità aggiuntiva. Funzionerà in qualsiasi contenitore di controlli OLE.

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

Confrontare l'esempio precedente con l'esempio successivo in cui MyDBControl può usare Visual Basic data binding se il contenitore lo supporta. Tuttavia, è stato definito in modo che funzioni in contenitori che non supportano Visual Basic data binding (probabilmente da un'API di database diversa):

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

Il controllo GroupBox è un semplice controllo frame. Si basa sul contenitore che implementa l'interfaccia [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) e funzionerà correttamente solo in questi contenitori:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

Un contenitore che supporta Visual Basic controlli associati a dati ma non supporta i controlli frame semplici specifica \_ il controllo CATID e il VBDATABOUND CATID nell' \_ interfaccia utente del controllo Insert. L'elenco dei controlli visualizzati per l'utente conterrebbe il pulsante CLSID \_ e CLSID \_ MyDBControl. Il \_ GroupBox del CLSID non verrà visualizzato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione di icone a una categoria](associating-icons-with-a-category.md)
</dt> <dt>

[Categorizzazione in base alle funzionalità del componente](categorizing-by-component-capabilities.md)
</dt> <dt>

[Classi e associazioni predefinite](default-classes-and-associations.md)
</dt> <dt>

[Definizione delle categorie di componenti](defining-component-categories.md)
</dt> <dt>

[Gestione categorie di componenti](the-component-categories-manager.md)
</dt> </dl>

 

 




