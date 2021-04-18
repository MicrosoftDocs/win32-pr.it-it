---
title: Limite tempo di ricerca
description: Quando si richiede una ricerca in un server con un carico di lavoro elevato, è consigliabile indicare al server di limitare la ricerca a un limite di tempo specificato.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- Limite tempo di ricerca ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ff9de38a17fe6ebac4ebb045e2f8b896bc764
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297653"
---
# <a name="search-time-limit"></a><span data-ttu-id="3116f-104">Limite tempo di ricerca</span><span class="sxs-lookup"><span data-stu-id="3116f-104">Search Time Limit</span></span>

<span data-ttu-id="3116f-105">Quando si richiede una ricerca in un server con un carico di lavoro elevato, è consigliabile indicare al server di limitare la ricerca a un limite di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="3116f-105">When you request a search on a server that is under a heavy workload, you may want to instruct the server to restrict the search to a specified time limit.</span></span> <span data-ttu-id="3116f-106">Per eseguire, ad esempio, un'applicazione per generare un report settimanale su un server in cui è in esecuzione near Capacity e per evitare di massimizzare il tempo della CPU e impedire l'esecuzione di altri processi, è possibile impostare il tempo di ricerca su un valore ridotto ed eseguire nuovamente l'applicazione in un secondo momento se non riesce a generare il report.</span><span class="sxs-lookup"><span data-stu-id="3116f-106">For example, to execute an application to generate a weekly report on a server that is running near capacity, and to avoid maximizing the CPU time and preventing other jobs from running, you can set the search time to a small value and rerun the application later if it fails to generate the report.</span></span>

<span data-ttu-id="3116f-107">Alcuni server possono imporre un limite di tempo amministrativo.</span><span class="sxs-lookup"><span data-stu-id="3116f-107">Some servers can impose their own administrative time limit.</span></span> <span data-ttu-id="3116f-108">In questi casi, se si specifica un valore per il limite di tempo di ricerca superiore al limite di tempo amministrativo, il server ignora la specifica e usa il limite di tempo amministrativo interno.</span><span class="sxs-lookup"><span data-stu-id="3116f-108">In these cases, if you specify a search time limit value greater than the administrative time limit, the server ignores your specification and use its internal administrative time limit instead.</span></span>

<span data-ttu-id="3116f-109">Per ulteriori informazioni sull'utilizzo dell'opzione per il limite di tempo di ricerca con un'interfaccia di ricerca specifica, vedere:</span><span class="sxs-lookup"><span data-stu-id="3116f-109">For more information about using the search time limit option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="3116f-110">Limite di tempo del server con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="3116f-110">Server Time Limit with IDirectorySearch</span></span>](server-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="3116f-111">Ricerca con ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="3116f-111">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="3116f-112">Ricerca con OLE DB</span><span class="sxs-lookup"><span data-stu-id="3116f-112">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




