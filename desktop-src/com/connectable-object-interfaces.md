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
# <a name="connectable-object-interfaces"></a><span data-ttu-id="84d16-103">Interfacce di oggetti collegabili</span><span class="sxs-lookup"><span data-stu-id="84d16-103">Connectable Object Interfaces</span></span>

<span data-ttu-id="84d16-104">Il supporto per gli oggetti collegabili richiede il supporto per quattro interfacce:</span><span class="sxs-lookup"><span data-stu-id="84d16-104">Support for connectable objects requires support for four interfaces:</span></span>

-   <span data-ttu-id="84d16-105">[**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) sull'oggetto collegabile</span><span class="sxs-lookup"><span data-stu-id="84d16-105">[**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) on the connectable object</span></span>
-   <span data-ttu-id="84d16-106">[**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) nell'oggetto punto di connessione</span><span class="sxs-lookup"><span data-stu-id="84d16-106">[**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) on the connection point object</span></span>
-   <span data-ttu-id="84d16-107">[**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) su un oggetto enumeratore</span><span class="sxs-lookup"><span data-stu-id="84d16-107">[**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) on an enumerator object</span></span>
-   <span data-ttu-id="84d16-108">[**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) su un oggetto enumeratore</span><span class="sxs-lookup"><span data-stu-id="84d16-108">[**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) on an enumerator object</span></span>

<span data-ttu-id="84d16-109">Le ultime due sono definite come enumeratori standard per i tipi **IConnectionPoint \*** e [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).</span><span class="sxs-lookup"><span data-stu-id="84d16-109">The latter two are defined as standard enumerators for the types **IConnectionPoint \*** and [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata).</span></span>

<span data-ttu-id="84d16-110">Inoltre, l'oggetto collegabile può supportare facoltativamente [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) e [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) per fornire informazioni sufficienti a un client, in modo che il client possa fornire supporto per l'interfaccia in uscita in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="84d16-110">Additionally, the connectable object can optionally support [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) to provide enough information to a client so that the client can provide support for the outgoing interface at run time.</span></span>

<span data-ttu-id="84d16-111">Infine, il client deve fornire un oggetto sink che implementi l'interfaccia in uscita, ovvero un'interfaccia COM personalizzata definita dall'oggetto collegabile.</span><span class="sxs-lookup"><span data-stu-id="84d16-111">Finally, the client must provide a sink object that implements the outgoing interface, which is a custom COM interface defined by the connectable object.</span></span>

<span data-ttu-id="84d16-112">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="84d16-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="84d16-113">Uso di IConnectionPointContainer</span><span class="sxs-lookup"><span data-stu-id="84d16-113">Using IConnectionPointContainer</span></span>](using-iconnectionpointcontainer.md)
-   [<span data-ttu-id="84d16-114">Uso di IConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="84d16-114">Using IConnectionPoint</span></span>](using-iconnectionpoint.md)
-   [<span data-ttu-id="84d16-115">Uso di IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="84d16-115">Using IProvideClassInfo</span></span>](using-iprovideclassinfo.md)

## <a name="related-topics"></a><span data-ttu-id="84d16-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84d16-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84d16-117">Architettura degli oggetti collegabili</span><span class="sxs-lookup"><span data-stu-id="84d16-117">Architecture of Connectable Objects</span></span>](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




