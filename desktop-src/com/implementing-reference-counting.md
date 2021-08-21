---
title: Implementazione del conteggio dei riferimenti
description: Implementazione del conteggio dei riferimenti
ms.assetid: d4fd98c9-afa4-4c5c-a3c9-44d34881cbdb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa2a3e9827d35d07fa88b62c6f1097fcb3ad3ae3b5b75764deeac1c9c271050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048159"
---
# <a name="implementing-reference-counting"></a>Implementazione del conteggio dei riferimenti

Il conteggio dei riferimenti richiede lavoro sia da parte dell'implementatore di una classe che dei client che usano oggetti di tale classe. Quando si implementa una classe, è necessario implementare i [**metodi AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) come parte dell'interfaccia [**IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Questi due metodi hanno le implementazioni semplici seguenti:

-   [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementa il conteggio dei riferimenti interni dell'oggetto.
-   [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) prima decrementa il conteggio dei riferimenti interno dell'oggetto e quindi controlla se il conteggio dei riferimenti è diminuito a zero. In caso contrario, significa che nessuno usa più l'oggetto, quindi la **funzione Release** dealloca l'oggetto.

Un approccio di implementazione comune per la maggior parte degli oggetti consiste nell'avere una sola implementazione di questi metodi (insieme a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))), che viene condivisa tra tutte le interfacce e quindi un conteggio dei riferimenti che si applica all'intero oggetto. Tuttavia, dal punto di vista di un client, il conteggio dei riferimenti è rigorosamente e chiaramente una nozione di puntatore per interfaccia e pertanto gli oggetti che sfruttano questa funzionalità creando, distruendo, caricando o scaricando parti della funzionalità in modo dinamico in base ai puntatori di interfaccia attualmente esistenti possono essere implementati. Queste interfacce sono chiamate *comunemente interfacce tear-off.*

Ogni volta che un client chiama un metodo (o una funzione API), ad esempio [**QueryInterface,**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))che restituisce un nuovo puntatore a interfaccia, il metodo chiamato è responsabile dell'incremento del conteggio dei riferimenti tramite il puntatore restituito. Ad esempio, quando un client crea un oggetto per la prima volta, riceve un puntatore a interfaccia a un oggetto che, dal punto di vista del client, ha un conteggio dei riferimenti di uno. Se il client chiama quindi [**AddRef sul**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) puntatore a interfaccia, il conteggio dei riferimenti diventa due. Il client deve chiamare [**Release due volte**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sul puntatore di interfaccia per eliminare tutti i relativi riferimenti all'oggetto.

Un esempio di come i conteggi dei riferimenti sono rigorosamente per ogni puntatore a interfaccia si verifica quando un client chiama [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) sul primo puntatore per una nuova interfaccia o per la stessa interfaccia. In uno di questi casi, il client deve chiamare [**Release una volta**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per ogni puntatore. COM non richiede che un oggetto restituirà lo stesso puntatore quando viene richiesta più volte la stessa interfaccia. L'unica eccezione è una query a [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)che identifica un oggetto in COM. Ciò consente all'implementazione dell'oggetto di gestire le risorse in modo efficiente.

La thread safety è anche un problema importante nell'implementazione [**di AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) [**e Release.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) Per altre informazioni, vedere [Processi, thread e apartment.](processes--threads--and-apartments.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della durata degli oggetti tramite il conteggio dei riferimenti](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 