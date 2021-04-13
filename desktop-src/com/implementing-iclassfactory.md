---
title: Implementazione di IClassFactory
description: Implementazione di IClassFactory
ms.assetid: 96466756-c135-4ee5-a48c-f31129878473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b057657508b3060506c15c68308ea6a5332e5099
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399752"
---
# <a name="implementing-iclassfactory"></a>Implementazione di IClassFactory

Quando un client utilizza un CLSID per richiedere la creazione di un'istanza dell'oggetto, il primo passaggio consiste nella creazione di un oggetto classe, un oggetto intermedio che contiene un'implementazione dei metodi dell'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) . Sebbene COM fornisca diverse funzioni di creazione di istanze, il primo passaggio nell'implementazione di queste funzioni è la creazione di un oggetto classe.

Di conseguenza, tutti i server devono implementare i metodi dell'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , che contiene due metodi:

-   [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance). Questo metodo deve creare un'istanza non inizializzata dell'oggetto e restituire un puntatore a un'interfaccia richiesta nell'oggetto.
-   [**LockServer**](/windows/win32/api/unknwn/nf-unknwn-iclassfactory-lockserver). Questo metodo incrementa il conteggio dei riferimenti nell'oggetto classe per garantire che il server rimanga in memoria e non venga arrestato prima che il client sia pronto per l'esecuzione.

Per consentire a un server di essere responsabile della propria licenza, COM definisce [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), che eredita la definizione da [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Pertanto, un server che implementa **IClassFactory2** deve, per definizione, implementare i metodi di **IClassFactory**.

COM fornisce anche funzioni di supporto per l'implementazione di server out-of-process. Per ulteriori informazioni, vedere [Helper di implementazione del server out-of-process](out-of-process-server-implementation-helpers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Responsabilità server COM](com-server-responsibilities.md)
</dt> <dt>

[Licenze e IClassFactory2](licensing-and-iclassfactory2.md)
</dt> </dl>

 

 