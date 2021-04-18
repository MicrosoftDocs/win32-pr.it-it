---
title: Timeout della ricerca
description: Un client può inoltre imporre un limite di tempo che attende che un server restituisca il set di risultati.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- Timeout della ricerca ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfdc63dd4490a840a16eb61598b2461c3e1a40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328359"
---
# <a name="search-time-out"></a><span data-ttu-id="46cc8-104">Timeout della ricerca</span><span class="sxs-lookup"><span data-stu-id="46cc8-104">Search Time Out</span></span>

<span data-ttu-id="46cc8-105">Un client può inoltre imporre un limite di tempo che attende che un server restituisca il set di risultati.</span><span class="sxs-lookup"><span data-stu-id="46cc8-105">A client can also impose a time limit that it will wait for a server to return the result set.</span></span> <span data-ttu-id="46cc8-106">Il valore dell'opzione "timeout di ricerca" specifica questo limite.</span><span class="sxs-lookup"><span data-stu-id="46cc8-106">The value of the "search time out" option specifies this limit.</span></span> <span data-ttu-id="46cc8-107">Quando il server non riesce a rispondere a una query entro il periodo di tempo specificato, il client può arrestare la ricerca e riprovare più tardi.</span><span class="sxs-lookup"><span data-stu-id="46cc8-107">When the server fails to respond to a query within the specified time period, the client can stop the search and try again later.</span></span>

<span data-ttu-id="46cc8-108">La proprietà di timeout è utile quando un client richiede una ricerca asincrona.</span><span class="sxs-lookup"><span data-stu-id="46cc8-108">The time-out property is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="46cc8-109">In una ricerca asincrona, il client effettua una richiesta e quindi procede con altre attività in attesa che il server restituisca i risultati.</span><span class="sxs-lookup"><span data-stu-id="46cc8-109">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="46cc8-110">È possibile che il server sia offline senza notificare al client.</span><span class="sxs-lookup"><span data-stu-id="46cc8-110">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="46cc8-111">In questo caso, il client non è in grado di riconoscere che il server sta ancora elaborando la query o se è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="46cc8-111">In this case, the client has no way of recognizing that the server is still processing the query, or if it has ceased to be live.</span></span> <span data-ttu-id="46cc8-112">La proprietà di timeout fornisce al client un controllo in tali istanze.</span><span class="sxs-lookup"><span data-stu-id="46cc8-112">The time-out property provides the client some control in such instances.</span></span>

<span data-ttu-id="46cc8-113">Per ulteriori informazioni sull'utilizzo dell'opzione di timeout di ricerca con un'interfaccia di ricerca specifica, vedere:</span><span class="sxs-lookup"><span data-stu-id="46cc8-113">For more information about using the search time-out option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="46cc8-114">Limite di tempo client con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="46cc8-114">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="46cc8-115">Ricerca con ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="46cc8-115">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="46cc8-116">Ricerca con OLE DB</span><span class="sxs-lookup"><span data-stu-id="46cc8-116">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




