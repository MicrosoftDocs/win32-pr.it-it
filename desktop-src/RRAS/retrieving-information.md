---
title: Recupero di informazioni
description: RTMv2 consente a un client di recuperare le informazioni a cui fa riferimento un determinato handle usando le funzioni RtmGetEntityInfo, RtmGetDestInfo, RtmGetRouteInfo e RtmGetNextHopInfo.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058a87c9463011aec55b0c6c8c0574ff1e013f23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221026"
---
# <a name="retrieving-information"></a><span data-ttu-id="ccf61-103">Recupero di informazioni</span><span class="sxs-lookup"><span data-stu-id="ccf61-103">Retrieving Information</span></span>

<span data-ttu-id="ccf61-104">RTMv2 consente a un client di recuperare le informazioni a cui fa riferimento un determinato handle usando le funzioni [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)e [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) .</span><span class="sxs-lookup"><span data-stu-id="ccf61-104">RTMv2 allows a client to retrieve the information referred to by a given handle using the [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo), and [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) functions.</span></span>

<span data-ttu-id="ccf61-105">Queste chiamate di funzione hanno funzioni corrispondenti ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) per rilasciare gli handle associati alla struttura di informazioni restituita da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="ccf61-105">These function calls have corresponding functions ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) to release the handles associated with the information structure returned by the routing table manager.</span></span>

> [!Note]  
> <span data-ttu-id="ccf61-106">Le informazioni per i client sono disponibili solo nell'istanza corrente e nella famiglia di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="ccf61-106">Information for clients is available only in the current instance and address family.</span></span>

 

<span data-ttu-id="ccf61-107">Per il codice di esempio che illustra come usare queste funzioni, vedere [cercare la route migliore](search-for-the-best-route.md).</span><span class="sxs-lookup"><span data-stu-id="ccf61-107">For sample code that shows how to use these functions, see [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a><span data-ttu-id="ccf61-108">Uso di RtmGetExactMatchRoute e RtmGetExactMatchDestination</span><span class="sxs-lookup"><span data-stu-id="ccf61-108">Using RtmGetExactMatchRoute and RtmGetExactMatchDestination</span></span>

<span data-ttu-id="ccf61-109">Le funzioni [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) e [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) vengono usate dai client per trovare una route o una destinazione specifica.</span><span class="sxs-lookup"><span data-stu-id="ccf61-109">The [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) and [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) functions are used by clients to find a specific route or destination.</span></span> <span data-ttu-id="ccf61-110">Queste funzioni risparmiano tempo eseguendo le operazioni di confronto per il client.</span><span class="sxs-lookup"><span data-stu-id="ccf61-110">These functions save time by doing the comparison work for the client.</span></span>

<span data-ttu-id="ccf61-111">Ad esempio, quando RIP Aggiorna una route, RIP deve conservare le informazioni della metrica obsolete.</span><span class="sxs-lookup"><span data-stu-id="ccf61-111">For example, when RIP updates a route, RIP must retain the old metric information.</span></span> <span data-ttu-id="ccf61-112">RIP cerca la route e le relative informazioni.</span><span class="sxs-lookup"><span data-stu-id="ccf61-112">RIP searches for the route and its information.</span></span> <span data-ttu-id="ccf61-113">Quindi, RIP può copiare le informazioni e aggiornare la route.</span><span class="sxs-lookup"><span data-stu-id="ccf61-113">Then RIP can copy the information and update the route.</span></span>

## <a name="using-rtmgetmostspecificdestination"></a><span data-ttu-id="ccf61-114">Uso di RtmGetMostSpecificDestination</span><span class="sxs-lookup"><span data-stu-id="ccf61-114">Using RtmGetMostSpecificDestination</span></span>

<span data-ttu-id="ccf61-115">La funzione [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) viene usata per individuare la destinazione che corrisponde maggiormente al prefisso di rete specificato.</span><span class="sxs-lookup"><span data-stu-id="ccf61-115">The [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) function is used to locate the destination that best matches the specified network prefix.</span></span>

<span data-ttu-id="ccf61-116">Ad esempio, il gestore del gruppo multicast usa questa funzione per eseguire un controllo RPF (Reverse-Path-inoltring) su un singolo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="ccf61-116">For example, the multicast group manager uses this function to perform a reverse-path-forwarding (RPF) check on a single address.</span></span> <span data-ttu-id="ccf61-117">La funzione può essere usata anche per trovare l'hop successivo locale per un determinato hop successivo remoto.</span><span class="sxs-lookup"><span data-stu-id="ccf61-117">The function can also be used to find the local next hop for a given remote next hop.</span></span>

<span data-ttu-id="ccf61-118">Per il codice di esempio che illustra come usare queste funzioni, vedere [cercare le route usando un albero del prefisso](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) e [cercare la route migliore](search-for-the-best-route.md).</span><span class="sxs-lookup"><span data-stu-id="ccf61-118">For sample code that shows how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) and [Search For the Best Route](search-for-the-best-route.md).</span></span>

## <a name="using-rtmgetlessspecificdestination"></a><span data-ttu-id="ccf61-119">Uso di RtmGetLessSpecificDestination</span><span class="sxs-lookup"><span data-stu-id="ccf61-119">Using RtmGetLessSpecificDestination</span></span>

<span data-ttu-id="ccf61-120">La funzione [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) viene usata per individuare la destinazione che rappresenta la corrispondenza migliore successiva per il prefisso di rete specificato.</span><span class="sxs-lookup"><span data-stu-id="ccf61-120">The [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) function is used to locate the destination that is the next-best match for the specified network prefix.</span></span> <span data-ttu-id="ccf61-121">Questa funzione può essere chiamata ripetutamente per restituire la successiva corrispondenza meno specifica successiva, fino a quando non sono presenti altre destinazioni corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="ccf61-121">This function can be called repeatedly to return the next successive less-specific match, until no more destinations match.</span></span>

<span data-ttu-id="ccf61-122">Questa funzione viene chiamata dopo una chiamata a [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).</span><span class="sxs-lookup"><span data-stu-id="ccf61-122">This function is called after a call to [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).</span></span>

<span data-ttu-id="ccf61-123">Per il codice di esempio che illustra come usare queste funzioni, vedere [cercare le route usando un albero del prefisso](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).</span><span class="sxs-lookup"><span data-stu-id="ccf61-123">For sample code that illustrates how to use these functions, see [Search for Routes Using a Prefix Tree](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).</span></span>

## <a name="using-rtmisbestroute"></a><span data-ttu-id="ccf61-124">Uso di RtmIsBestRoute</span><span class="sxs-lookup"><span data-stu-id="ccf61-124">Using RtmIsBestRoute</span></span>

<span data-ttu-id="ccf61-125">La funzione [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) consente a un client di determinare rapidamente se una determinata route è la migliore route a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="ccf61-125">The [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) function enables a client to quickly find out whether or not a particular route is the best route to a destination.</span></span> <span data-ttu-id="ccf61-126">Ad esempio, un client potrebbe dover archiviare una route specifica solo se è la route migliore.</span><span class="sxs-lookup"><span data-stu-id="ccf61-126">For example, a client may need to store a particular route only if it is the best route.</span></span> <span data-ttu-id="ccf61-127">Pertanto, il client può chiamare questa funzione, invece di enumerare tutte le route e di eseguire il confronto.</span><span class="sxs-lookup"><span data-stu-id="ccf61-127">Therefore, the client can call this function, instead of enumerating all routes and making the comparison itself.</span></span>

 

 




