---
title: Implementazione del conteggio dei riferimenti
description: Implementazione del conteggio dei riferimenti
ms.assetid: d4fd98c9-afa4-4c5c-a3c9-44d34881cbdb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d4dfe2b0faf2fc6557d1b089e33ae6ce4b98cb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300554"
---
# <a name="implementing-reference-counting"></a>Implementazione del conteggio dei riferimenti

Il conteggio dei riferimenti richiede il lavoro sulla parte sia dell'implementatore di una classe che dei client che utilizzano oggetti di tale classe. Quando si implementa una classe, è necessario implementare i metodi [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) come parte dell'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Questi due metodi hanno le seguenti implementazioni semplici:

-   [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementa il conteggio dei riferimenti interni dell'oggetto.
-   [**Rilascia**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) innanzitutto decrementa il conteggio dei riferimenti interni dell'oggetto, quindi controlla se il conteggio dei riferimenti è sceso a zero. In caso affermativo, significa che nessuno sta usando più l'oggetto, quindi la funzione **Release** dealloca l'oggetto.

Un approccio di implementazione comune per la maggior parte degli oggetti consiste nel disporre di una sola implementazione di questi metodi (insieme a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))), che viene condivisa tra tutte le interfacce e, di conseguenza, un conteggio dei riferimenti applicato all'intero oggetto. Tuttavia, dal punto di vista del client, il conteggio dei riferimenti è rigorosamente e chiaramente una nozione di puntatore per interfaccia e pertanto gli oggetti che sfruttano questa funzionalità creando dinamicamente, eliminando, caricando o scaricando parti della loro funzionalità in base ai puntatori di interfaccia attualmente esistenti possono essere implementati. Queste interfacce sono comunemente dette *interfacce di strappo*.

Ogni volta che un client chiama un metodo (o funzione API), ad esempio [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), che restituisce un nuovo puntatore di interfaccia, il metodo chiamato è responsabile dell'incremento del conteggio dei riferimenti tramite il puntatore restituito. Ad esempio, quando un client crea prima un oggetto, riceve un puntatore di interfaccia a un oggetto che, dal punto di vista del client, ha un conteggio dei riferimenti di uno. Se il client chiama [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sul puntatore a interfaccia, il conteggio dei riferimenti diventa due. Il client deve chiamare il [**rilascio**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) due volte sul puntatore a interfaccia per eliminare tutti i relativi riferimenti all'oggetto.

Un esempio di come i conteggi dei riferimenti sono rigorosamente per interfaccia-puntatore si verifica quando un client chiama [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) sul primo puntatore per una nuova interfaccia o la stessa interfaccia. In entrambi i casi, è necessario che il client chiami [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) una volta per ogni puntatore. COM non richiede che un oggetto restituisca lo stesso puntatore quando viene richiesta la stessa interfaccia più volte. L'unica eccezione è costituita da una query a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), che identifica un oggetto a com. Ciò consente all'implementazione dell'oggetto di gestire le risorse in modo efficiente.

La thread-safety rappresenta anche un problema importante nell'implementazione di [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Per ulteriori informazioni, vedere [processi, thread e Apartment](processes--threads--and-apartments.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della durata degli oggetti tramite il conteggio dei riferimenti](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 