---
title: Uso di IConnectionPoint
description: Uso di IConnectionPoint
ms.assetid: afd50b84-1fd6-47ad-a3ef-e8b4a725b72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2449be5f1711457807666e9e2068d13defd8437bedee93402f7b974d5298d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129423"
---
# <a name="using-iconnectionpoint"></a>Uso di IConnectionPoint

Quando il client ha un puntatore a un punto di connessione, può eseguire le operazioni seguenti come espresso tramite [**IConnectionPoint:**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint)

-   In primo [**luogo, IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) recupera l'IID dell'interfaccia in uscita supportato dal punto di connessione. Se usato in combinazione con [**IEnumConnectionPoints,**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints)questo metodo consente al client di esaminare gli ID di tutte le interfacce in uscita supportate nell'oggetto collegabile.
-   In secondo momento, un client può tornare dal punto di connessione all'interfaccia [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) dell'oggetto collegabile tramite il metodo [**IConnectionPoint::GetConnectionPointContainer.**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectionpointcontainer)
-   Terzo, i metodi più interessanti per il client [**sono IConnectionPoint::Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) e [**IConnectionPoint::Unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise). Quando un client vuole connettere il proprio oggetto sink all'oggetto collegabile, il client passa il puntatore [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del sink (o qualsiasi altro puntatore di interfaccia sullo stesso oggetto) a **Advise.** Il punto di connessione esegue una query sul sink per l'interfaccia in uscita specifica prevista. Se tale interfaccia è disponibile nel sink, il punto di connessione archivia il puntatore di interfaccia. Da questo momento fino a quando non viene chiamato **Unadvise,** l'oggetto collegabile effettua chiamate al sink tramite questa interfaccia quando si verificano eventi. Per disconnettere il sink dal punto di connessione, il client passa una chiave restituita da **Advise** al **metodo Unadvise.** **Unadvise deve** chiamare [**Release sull'interfaccia**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sink.
-   Infine, un client può chiedere a un punto di connessione di enumerare tutte le connessioni esistenti tramite [**IConnectionPoint::EnumConnections**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-enumconnections). Questo metodo crea un oggetto enumeratore (con un conteggio dei riferimenti separato) che restituisce un [**puntatore IEnumConnections.**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) Il client deve chiamare [**Release quando**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) l'enumeratore non è più necessario. Inoltre, l'enumeratore restituisce una serie [**di strutture CONNECTDATA,**](/windows/win32/api/ocidl/ns-ocidl-connectdata) una per ogni connessione. Ogni struttura descrive una connessione usando il [**puntatore IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del sink e la chiave di connessione originariamente restituita da [**Advise.**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) Al termine con questi puntatori a interfaccia sink, il client deve chiamare **Release** su ogni puntatore restituito in **una struttura CONNECTDATA.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce a oggetti collegabili](connectable-object-interfaces.md)
</dt> </dl>

 

 