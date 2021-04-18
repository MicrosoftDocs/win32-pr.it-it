---
title: Limite di tempo client con IDirectorySearch
description: Un client può imporre un limite di tempo per la restituzione del set di risultati da parte di un server. Quando il server non riesce a rispondere a una query entro il periodo di tempo specificato, il client può abbandonare la ricerca e riprovare più tardi.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Limite di tempo client con IDirectorySearch
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, limite di tempo client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed25bd8499f7166d7ea494f71e6f78193f9c778a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297693"
---
# <a name="client-time-limit-with-idirectorysearch"></a><span data-ttu-id="0112f-106">Limite di tempo client con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="0112f-106">Client Time Limit with IDirectorySearch</span></span>

<span data-ttu-id="0112f-107">Un client può imporre un limite di tempo per la restituzione del set di risultati da parte di un server.</span><span class="sxs-lookup"><span data-stu-id="0112f-107">A client can impose a time limit for a server to return the result set.</span></span> <span data-ttu-id="0112f-108">Quando il server non riesce a rispondere a una query entro il periodo di tempo specificato, il client può abbandonare la ricerca e riprovare più tardi.</span><span class="sxs-lookup"><span data-stu-id="0112f-108">When the server fails to respond to a query within the specified time period, the client can abandon the search and try it again later.</span></span>

<span data-ttu-id="0112f-109">La preferenza per il limite di tempo client è utile quando un client richiede una ricerca asincrona.</span><span class="sxs-lookup"><span data-stu-id="0112f-109">The client time limit preference is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="0112f-110">In una ricerca asincrona, il client effettua una richiesta e quindi procede con altre attività in attesa che il server restituisca i risultati.</span><span class="sxs-lookup"><span data-stu-id="0112f-110">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="0112f-111">È possibile che il server sia offline senza notificare al client.</span><span class="sxs-lookup"><span data-stu-id="0112f-111">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="0112f-112">In questo caso, il client non avrà alcuna notifica se il server sta ancora elaborando la query o se non è più attiva.</span><span class="sxs-lookup"><span data-stu-id="0112f-112">In this case, the client will have no notification of whether the server is still processing the query, or if it no longer live.</span></span> <span data-ttu-id="0112f-113">La preferenza per il limite di tempo client fornisce al client un controllo di situazioni come questa.</span><span class="sxs-lookup"><span data-stu-id="0112f-113">The client time limit preference gives the client some control of situations like this.</span></span>

<span data-ttu-id="0112f-114">Il valore predefinito per il limite di tempo client non è limite.</span><span class="sxs-lookup"><span data-stu-id="0112f-114">The default for the client time limit is no limit.</span></span> <span data-ttu-id="0112f-115">Per impostare un limite di tempo client, impostare un'opzione di ricerca **Ads \_ SEARCHPREF \_ timeout** con un valore **\_ Integer ADSTYPE** che contenga il limite di tempo client, espresso in secondi, nella matrice di [**\_ \_ informazioni SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="0112f-115">To set a client time limit, set an **ADS\_SEARCHPREF\_TIMEOUT** search option with an **ADSTYPE\_INTEGER** value that contains the client time limit, in seconds, in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="0112f-116">Un limite di tempo del client pari a zero indica nessun limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="0112f-116">A client time limit of zero indicates no time limit.</span></span>

<span data-ttu-id="0112f-117">Nell'esempio di codice seguente viene illustrato come impostare il limite di tempo del client.</span><span class="sxs-lookup"><span data-stu-id="0112f-117">The following code example shows how to set the client time limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




