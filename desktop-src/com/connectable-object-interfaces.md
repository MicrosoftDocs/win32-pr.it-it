---
title: Interfacce di oggetti collegabili
description: Interfacce di oggetti collegabili
ms.assetid: 136fb7bd-7a38-4051-b47b-3d08f1dbee79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc2d747d7aabe25788c34d80bddb8ca1466e9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856909"
---
# <a name="connectable-object-interfaces"></a>Interfacce di oggetti collegabili

Il supporto per gli oggetti collegabili richiede il supporto per quattro interfacce:

-   [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) sull'oggetto collegabile
-   [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) nell'oggetto punto di connessione
-   [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) su un oggetto enumeratore
-   [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) su un oggetto enumeratore

Le ultime due sono definite come enumeratori standard per i tipi **IConnectionPoint \*** e [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).

Inoltre, l'oggetto collegabile può supportare facoltativamente [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) e [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) per fornire informazioni sufficienti a un client, in modo che il client possa fornire supporto per l'interfaccia in uscita in fase di esecuzione.

Infine, il client deve fornire un oggetto sink che implementi l'interfaccia in uscita, ovvero un'interfaccia COM personalizzata definita dall'oggetto collegabile.

Per altre informazioni, vedere i seguenti argomenti:

-   [Uso di IConnectionPointContainer](using-iconnectionpointcontainer.md)
-   [Uso di IConnectionPoint](using-iconnectionpoint.md)
-   [Uso di IProvideClassInfo](using-iprovideclassinfo.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Architettura degli oggetti collegabili](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




