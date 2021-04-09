---
title: Uso di IConnectionPoint
description: Uso di IConnectionPoint
ms.assetid: afd50b84-1fd6-47ad-a3ef-e8b4a725b72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7aa758ec1bd40233b1cc41a6c375ed296fc167
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047387"
---
# <a name="using-iconnectionpoint"></a>Uso di IConnectionPoint

Quando il client dispone di un puntatore a un punto di connessione, può eseguire le operazioni seguenti come espresso tramite [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint):

-   First, [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) recupera l'IID dell'interfaccia in uscita supportato dal punto di connessione. Se usato insieme a [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints), questo metodo consente al client di esaminare il IID di tutte le interfacce in uscita supportate nell'oggetto collegabile.
-   In secondo luogo, un client può passare dal punto di connessione all'interfaccia [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) dell'oggetto collegabile tramite il metodo [**IConnectionPoint:: GetConnectionPointContainer**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectionpointcontainer) .
-   Terzo, i metodi più interessanti per il client sono [**IConnectionPoint:: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) e [**IConnectionPoint:: Unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise). Quando un client desidera connettere il proprio oggetto sink all'oggetto collegabile, il client passa il puntatore [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del sink (o qualsiasi altro puntatore di interfaccia sullo stesso oggetto) a **Advise**. Il punto di connessione esegue una query sul sink per l'interfaccia in uscita specifica prevista. Se tale interfaccia è disponibile sul sink, il punto di connessione archivia il puntatore di interfaccia. Da questo punto fino a quando non viene chiamato **Unadvise** , l'oggetto collegabile effettuerà chiamate al sink tramite questa interfaccia quando si verificano gli eventi. Per disconnettere il sink dal punto di connessione, il client passa una chiave restituita da **Advise** al metodo **Unadvise** . È **necessario che** la chiamata a [**release venga rilasciata**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sull'interfaccia sink.
-   Infine, un client può richiedere a un punto di connessione di enumerare tutte le connessioni esistenti tramite [**IConnectionPoint:: EnumConnections**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-enumconnections). Questo metodo crea un oggetto enumeratore (con un conteggio dei riferimenti separato) che restituisce un puntatore [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) . Il client deve chiamare [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) quando l'enumeratore non è più necessario. L'enumeratore restituisce inoltre una serie di strutture [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata) , una per ogni connessione. Ogni struttura descrive una connessione utilizzando il puntatore [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del sink e la chiave di connessione originariamente restituita da [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise). Quando vengono eseguiti con questi puntatori dell'interfaccia di sink, il client deve chiamare **Release** su ogni puntatore restituito in una struttura **CONNECTDATA** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce di oggetti collegabili](connectable-object-interfaces.md)
</dt> </dl>

 

 