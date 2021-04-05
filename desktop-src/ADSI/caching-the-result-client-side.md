---
title: Memorizzazione dei risultati nella cache (lato client)
description: La memorizzazione nella cache sul lato client archivia il set di risultati nella memoria del client, fornendo miglioramenti delle prestazioni per il lato client.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Memorizzazione nella cache del risultato (lato client) ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb965da1da0c791db215dd7eee925a7c9f67ccf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955109"
---
# <a name="caching-the-result-client-side"></a><span data-ttu-id="463d4-104">Memorizzazione dei risultati nella cache (lato client)</span><span class="sxs-lookup"><span data-stu-id="463d4-104">Caching the Result (Client Side)</span></span>

<span data-ttu-id="463d4-105">La memorizzazione nella cache sul lato client archivia il set di risultati nella memoria del client, fornendo miglioramenti delle prestazioni per il lato client.</span><span class="sxs-lookup"><span data-stu-id="463d4-105">Client-side caching stores the result set in the client memory, providing performance enhancements for the client side.</span></span> <span data-ttu-id="463d4-106">Un client può rivedere ripetutamente un oggetto senza più corse al server.</span><span class="sxs-lookup"><span data-stu-id="463d4-106">A client can revisit an object repeatedly without multiple trips to the server.</span></span> <span data-ttu-id="463d4-107">Per impostazione predefinita, ADSI memorizza nella cache il set di risultati per i client.</span><span class="sxs-lookup"><span data-stu-id="463d4-107">By default, ADSI caches the result set for the clients.</span></span> <span data-ttu-id="463d4-108">In questo modo, ADSI fornisce ai client il supporto del cursore simile a SQL.</span><span class="sxs-lookup"><span data-stu-id="463d4-108">This enables ADSI to provide clients with SQL-like cursor support.</span></span> <span data-ttu-id="463d4-109">È possibile scorrere più volte un determinato set di risultati.</span><span class="sxs-lookup"><span data-stu-id="463d4-109">You may iterate through a given result set several times.</span></span>

<span data-ttu-id="463d4-110">ADSI consente inoltre ai client di disattivare la cache per ridurre i requisiti di memoria.</span><span class="sxs-lookup"><span data-stu-id="463d4-110">ADSI also enables clients to turn off the cache to reduce memory requirements.</span></span> <span data-ttu-id="463d4-111">Se la memorizzazione nella cache sul lato client è disabilitata, il client non mantiene il set di risultati in memoria.</span><span class="sxs-lookup"><span data-stu-id="463d4-111">If client-side caching is disabled, the client does not maintain the result set in memory.</span></span> <span data-ttu-id="463d4-112">Ogni riga viene liberata dopo che è stata recuperata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="463d4-112">Each row is freed after the application retrieves it.</span></span> <span data-ttu-id="463d4-113">La disabilitazione della memorizzazione nella cache sul lato client può essere utile per ridurre i requisiti di memoria sul lato client in questi casi, ad esempio quando si prevede di eseguire un solo passaggio attraverso il set di risultati.</span><span class="sxs-lookup"><span data-stu-id="463d4-113">Disabling client-side caching can be useful for decreasing the client-side memory requirements in such cases as when you intend only to make a single pass through the result set.</span></span> <span data-ttu-id="463d4-114">Tuttavia, quando i client scelgono di non memorizzare nella cache il risultato, rinunciano al supporto del cursore.</span><span class="sxs-lookup"><span data-stu-id="463d4-114">However, when clients elect not to cache the result, they give up cursor support.</span></span>

<span data-ttu-id="463d4-115">Per ulteriori informazioni sulla memorizzazione nella cache dei risultati con un'interfaccia di ricerca specifica, vedere:</span><span class="sxs-lookup"><span data-stu-id="463d4-115">For more information about results caching with a specific search interface, see:</span></span>

-   [<span data-ttu-id="463d4-116">Caching dei risultati con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="463d4-116">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="463d4-117">Ricerca con ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="463d4-117">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="463d4-118">Ricerca con OLE DB</span><span class="sxs-lookup"><span data-stu-id="463d4-118">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




