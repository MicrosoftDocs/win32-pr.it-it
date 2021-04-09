---
title: Funzioni di supporto per la creazione di istanze
description: Funzioni di supporto per la creazione di istanze
ms.assetid: 0b9b7bcf-f0f0-42c4-945e-63a532640d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84956f6040aaba13b46dea92bea611a49d5d8de3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047407"
---
# <a name="instance-creation-helper-functions"></a>Funzioni di supporto per la creazione di istanze

Nelle versioni precedenti di COM, il meccanismo principale utilizzato per creare un'istanza dell'oggetto era la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) . Questa funzione incapsula il processo di creazione di un oggetto classe, usando tale oggetto per creare una nuova istanza e rilasciare l'oggetto classe. Un'altra funzione di questo tipo è la [**OleCreate**](/windows/desktop/api/ole/nf-ole-olecreate)più specifica, l'helper del documento composito OLE che crea un oggetto classe e recupera un puntatore a un oggetto richiesto.

Per semplificare il processo di creazione dell'istanza nei sistemi distribuiti, COM ha introdotto quattro importanti nuovi meccanismi di creazione dell'istanza:

-   Moniker della classe e [ **IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)

Un moniker della classe consente di identificare la classe di un oggetto e viene in genere usata con un altro moniker, ad esempio un moniker di file, per indicare la posizione dell'oggetto. Ciò consente di eseguire il binding a un oggetto e di specificare il server da avviare per l'oggetto. I moniker della classe possono anche essere composti a destra dei moniker che supportano l'associazione all'interfaccia [**IClassActivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) . Per ulteriori informazioni, vedere [moniker della classe](class-monikers.md).

[**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) estende [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per consentire la creazione di un singolo oggetto non INIZIALIZZAto associato al CLSID specificato in un computer remoto specificato. Inoltre, anziché richiedere una singola interfaccia e ottenere un singolo puntatore a tale interfaccia, **CoCreateInstanceEx** consente di eseguire una query per più interfacce e, se disponibili, di ricevere puntatori in un unico round trip, consentendo così un minor numero di round trip tra i computer. In questo modo è possibile rendere più efficiente l'interazione con gli oggetti remoti. A tale scopo, la funzione usa una matrice di strutture a più [**livelli di \_ Qi**](/windows/win32/api/objidlbase/ns-objidlbase-multi_qi) .

Per la creazione di un oggetto tramite [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) è ancora necessario che l'oggetto venga inizializzato tramite una chiamata a una delle interfacce di inizializzazione (ad esempio [**IPersistStorage:: Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-load)). Le funzioni di supporto [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) e [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) incapsulano sia la potenza di creazione dell'istanza di **CoCreateInstanceEx** che l'inizializzazione, la prima da un file e la seconda da una risorsa di archiviazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un oggetto tramite un oggetto classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 