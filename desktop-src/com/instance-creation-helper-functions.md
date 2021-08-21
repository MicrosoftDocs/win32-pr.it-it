---
title: Funzioni helper per la creazione di istanze
description: Funzioni helper per la creazione di istanze
ms.assetid: 0b9b7bcf-f0f0-42c4-945e-63a532640d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bd8535d1dc90ac47210a7ec9b34b5fcced61a3a541b27b2aa5af2ba1cf8b27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918922"
---
# <a name="instance-creation-helper-functions"></a>Funzioni helper per la creazione di istanze

Nelle versioni precedenti di COM, il meccanismo principale usato per creare un'istanza dell'oggetto era la [**funzione CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Questa funzione incapsula il processo di creazione di un oggetto classe, usando per creare una nuova istanza e rilasciare l'oggetto classe. Un'altra funzione di questo tipo è la più specifica [**OleCreate,**](/windows/desktop/api/ole/nf-ole-olecreate)l'helper documento composto OLE che crea un oggetto classe e recupera un puntatore a un oggetto richiesto.

Per smussare il processo di creazione di istanze nei sistemi distribuiti, COM ha introdotto quattro importanti meccanismi di creazione di nuove istanze:

-   Moniker di classe e [ **IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)

Un moniker di classe consente di identificare la classe di un oggetto e viene in genere usato con un altro moniker, ad esempio un moniker di file, per indicare la posizione dell'oggetto. In questo modo è possibile eseguire l'associazione a un oggetto e specificare il server da avviare per tale oggetto. I moniker di classe possono anche essere composti a destra dei moniker che supportano l'associazione [**all'interfaccia IClassActivator.**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) Per altre informazioni, vedere [Moniker della classe](class-monikers.md).

[**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) estende [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per rendere possibile la creazione di un singolo oggetto non inizializzato associato al CLSID specificato in un computer remoto specificato. Inoltre, anziché richiedere una singola interfaccia e ottenere un singolo puntatore a tale interfaccia, **CoCreateInstanceEx** consente di eseguire una query per più interfacce e, se disponibile, di ricevere puntatori a esse in un singolo round trip, permettendo così un minor numero di round trip tra computer. In questo modo l'interazione tra oggetti remoti può essere molto più efficiente. A tale scopo, la funzione usa una matrice di [**strutture MULTI \_ QI.**](/windows/win32/api/objidlbase/ns-objidlbase-multi_qi)

La creazione di un oggetto tramite [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) richiede comunque che l'oggetto sia inizializzato tramite una chiamata a una delle interfacce di inizializzazione , ad esempio [**IPersistStorage::Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-load). Le funzioni helper [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) e [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) incapsulano sia la potenza di creazione dell'istanza di **CoCreateInstanceEx** che l'inizializzazione, la prima da un file e la seconda da un archivio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un oggetto tramite un oggetto classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 