---
title: Ricerche asincrone
description: L'abilitazione dei risultati della ricerca asincrona (Async) in una chiamata a GetFirstRow o alla prima chiamata a GetNextRow blocca fino a quando non viene restituita la prima voce dal server.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- ADSI per ricerche asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8b8fff875af18b85cdffa4ce67d631d94ed14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955114"
---
# <a name="asynchronous-searches"></a><span data-ttu-id="fc283-104">Ricerche asincrone</span><span class="sxs-lookup"><span data-stu-id="fc283-104">Asynchronous Searches</span></span>

<span data-ttu-id="fc283-105">L'abilitazione dei risultati della ricerca asincrona (Async) in una chiamata a **GetFirstRow** o alla prima chiamata a **GetNextRow** blocca fino a quando non viene restituita la prima voce dal server.</span><span class="sxs-lookup"><span data-stu-id="fc283-105">Enabling asynchronous (async) search results in a call to **GetFirstRow** or the first call to **GetNextRow** blocks until the first entry is returned from the server.</span></span> <span data-ttu-id="fc283-106">Ovvero, se la ricerca sul server richiede molto tempo, i primi risultati vengono restituiti rapidamente.</span><span class="sxs-lookup"><span data-stu-id="fc283-106">That is, if the search on the server requires much time, the first few results are returned quickly.</span></span> <span data-ttu-id="fc283-107">Questo può essere utile quando si popola una casella di riepilogo con i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="fc283-107">This can help when populating a list box with search results.</span></span> <span data-ttu-id="fc283-108">I risultati della ricerca vengono visualizzati quando vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="fc283-108">Search results are displayed as they are returned.</span></span>

<span data-ttu-id="fc283-109">Se Async è disabilitato, la prima chiamata a **GetFirstRow** o **GetNextRow** si bloccherà fino a quando il server non calcola l'intero set di risultati e restituisce.</span><span class="sxs-lookup"><span data-stu-id="fc283-109">If async is disabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server computes the entire result set and returns.</span></span> <span data-ttu-id="fc283-110">Solo a questo punto viene restituita la prima riga.</span><span class="sxs-lookup"><span data-stu-id="fc283-110">Only then is the first row returned.</span></span> <span data-ttu-id="fc283-111">Questa operazione non è consigliata se si prevede che il set di risultati sia di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="fc283-111">This is not recommended if the result set is expected to be large.</span></span>

<span data-ttu-id="fc283-112">Se il paging e async sono abilitati, la prima chiamata a **GetFirstRow** o **GetNextRow** si bloccherà fino a quando il server non genera e non invia la prima pagina di risultati.</span><span class="sxs-lookup"><span data-stu-id="fc283-112">If both paging and async are enabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server generates and sends the first page of results.</span></span> <span data-ttu-id="fc283-113">Se è stata impostata una dimensione di pagina ragionevole, i risultati vengono visualizzati immediatamente.</span><span class="sxs-lookup"><span data-stu-id="fc283-113">If a reasonable page size was set, results will appear immediately.</span></span> <span data-ttu-id="fc283-114">Ancora più importante, se i risultati della ricerca sono molto grandi e si cerca una voce specifica, non è necessario richiedere altri risultati dal server dopo aver trovato le voci che interessano.</span><span class="sxs-lookup"><span data-stu-id="fc283-114">More importantly, if the search results are expected to be very large, and you search for a particular entry, it is not required that you request more results from the server after you have found the entries that interest you.</span></span>

<span data-ttu-id="fc283-115">Una ricerca asincrona di paging fornisce un controllo accurato di una ricerca.</span><span class="sxs-lookup"><span data-stu-id="fc283-115">A paged async search provides fine control of a search.</span></span> <span data-ttu-id="fc283-116">Questa operazione è utile se i risultati della ricerca possono avere dimensioni molto elevate e richiedono tempi estesi dal server.</span><span class="sxs-lookup"><span data-stu-id="fc283-116">This is useful if the search results may be very large and require extensive time from the server.</span></span>

<span data-ttu-id="fc283-117">Per ulteriori informazioni sull'utilizzo di ricerche asincrone con un'interfaccia di ricerca specifica, vedere:</span><span class="sxs-lookup"><span data-stu-id="fc283-117">For more information about using asynchronous searches with a specific search interface, see:</span></span>

-   [<span data-ttu-id="fc283-118">Ricerche sincrone e asincrone con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="fc283-118">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="fc283-119">Ricerca con ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="fc283-119">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="fc283-120">Ricerca con OLE DB</span><span class="sxs-lookup"><span data-stu-id="fc283-120">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




