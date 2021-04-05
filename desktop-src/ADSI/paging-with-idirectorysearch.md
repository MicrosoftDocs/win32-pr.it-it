---
title: Paging con IDirectorySearch
description: Il paging specifica il numero di righe restituite dal server al client.
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- Paging con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, paging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e9fdf001f5908f6c3fc7321c8c94cda09f1b96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955090"
---
# <a name="paging-with-idirectorysearch"></a><span data-ttu-id="50f5c-105">Paging con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="50f5c-105">Paging with IDirectorySearch</span></span>

<span data-ttu-id="50f5c-106">Il paging specifica il numero di righe restituite dal server al client.</span><span class="sxs-lookup"><span data-stu-id="50f5c-106">Paging specifies how many rows that the server returns to the client.</span></span> <span data-ttu-id="50f5c-107">È possibile definire una pagina in base al numero di righe o a un limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="50f5c-107">A page can be defined by the number of rows or a time limit.</span></span> <span data-ttu-id="50f5c-108">L'oggetto ADSI COM recupera ogni pagina di risultati in base ai valori elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="50f5c-108">The ADSI COM object retrieves each page of results based on the values listed in the following table.</span></span> <span data-ttu-id="50f5c-109">Il chiamante chiama [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) quando ha raggiunto la fine della pagina e l'oggetto ADSI com recupera la pagina successiva.</span><span class="sxs-lookup"><span data-stu-id="50f5c-109">The caller calls [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) when it has reached the page end, and the ADSI COM object retrieves the next page.</span></span>



| <span data-ttu-id="50f5c-110">Valore</span><span class="sxs-lookup"><span data-stu-id="50f5c-110">Value</span></span>                                   | <span data-ttu-id="50f5c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50f5c-111">Description</span></span>                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50f5c-112">**\_SEARCHPREF Ads \_**</span><span class="sxs-lookup"><span data-stu-id="50f5c-112">**ADS\_SEARCHPREF\_PAGESIZE**</span></span>           | <span data-ttu-id="50f5c-113">Specifica il numero massimo di righe da restituire in una pagina.</span><span class="sxs-lookup"><span data-stu-id="50f5c-113">Specifies the maximum number of rows to return in a page.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="50f5c-114">**\_limite di \_ tempo di \_ paging \_ per ADS SEARCHPREF**</span><span class="sxs-lookup"><span data-stu-id="50f5c-114">**ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT**</span></span> | <span data-ttu-id="50f5c-115">Specifica il tempo massimo, in secondi, impiegato dal server per la raccolta di una pagina di risultati prima che la pagina venga restituita al client.</span><span class="sxs-lookup"><span data-stu-id="50f5c-115">Specifies the maximum time, in seconds, that the server should spend collecting a page of results before returning the page to the client.</span></span> <span data-ttu-id="50f5c-116">Se viene raggiunto il limite, il server interrompe la ricerca e restituisce le righe già recuperate per la pagina.</span><span class="sxs-lookup"><span data-stu-id="50f5c-116">If the limit is reached, the server stops the search and returns the rows already retrieved for the page.</span></span> |



 

<span data-ttu-id="50f5c-117">Se nessuna di queste preferenze di ricerca è impostata, il valore predefinito non è paging.</span><span class="sxs-lookup"><span data-stu-id="50f5c-117">If neither of these search preferences is set, the default is no paging.</span></span> <span data-ttu-id="50f5c-118">Le ricerche delle Active Directory eseguite senza paging sono limitate alla restituzione di un massimo dei primi 1000 record, pertanto è necessario utilizzare una ricerca di paging se è possibile che il set di risultati contenga più di 1000 elementi.</span><span class="sxs-lookup"><span data-stu-id="50f5c-118">Searches of the Active Directory performed without paging are limited to returning a maximum of the first 1000 records, so you must use a paged search if there is the possibility that the result set will contain more than 1000 items.</span></span>

<span data-ttu-id="50f5c-119">Un'operazione di ricerca può comportare la restituzione di un numero elevato di oggetti.</span><span class="sxs-lookup"><span data-stu-id="50f5c-119">A search operation may result in a large number of objects being returned.</span></span> <span data-ttu-id="50f5c-120">Se il server restituisce il risultato in un unico set, potrebbe ridurre le prestazioni del client e del server, nonché influenzare il carico di rete.</span><span class="sxs-lookup"><span data-stu-id="50f5c-120">If the server returns the result in one set, it could decrease the performance of the client and server, as well as affect the network load.</span></span> <span data-ttu-id="50f5c-121">Per evitare questo problema, è possibile utilizzare le ricerche di paging.</span><span class="sxs-lookup"><span data-stu-id="50f5c-121">Paged searches can be used to prevent this.</span></span> <span data-ttu-id="50f5c-122">In una ricerca di paging il client può accettare i risultati in pacchetti più piccoli.</span><span class="sxs-lookup"><span data-stu-id="50f5c-122">In a paged search, the client can accept results in smaller packets.</span></span> <span data-ttu-id="50f5c-123">Le dimensioni di un pacchetto sono note come dimensioni della pagina di ricerca.</span><span class="sxs-lookup"><span data-stu-id="50f5c-123">The size of a packet is known as the search page size.</span></span>

<span data-ttu-id="50f5c-124">Le ricerche di paging offrono vantaggi sia per il client che per il server.</span><span class="sxs-lookup"><span data-stu-id="50f5c-124">Paged searches offer benefits to both the client and the server.</span></span> <span data-ttu-id="50f5c-125">Il client può essere più reattivo nella presentazione dei risultati agli utenti.</span><span class="sxs-lookup"><span data-stu-id="50f5c-125">The client can be more responsive in presenting the results to users.</span></span> <span data-ttu-id="50f5c-126">Questo è particolarmente importante per gli strumenti dell'interfaccia utente grafica che possono iniziare il processo di visualizzazione della finestra mentre l'altro thread riceve contemporaneamente i dati.</span><span class="sxs-lookup"><span data-stu-id="50f5c-126">This is especially relevant to graphical user interface tools that can begin the window display process while the other thread concurrently receives the data.</span></span>

<span data-ttu-id="50f5c-127">Sul lato server, le ricerche di paging rendono l'operazione scalabile.</span><span class="sxs-lookup"><span data-stu-id="50f5c-127">On the server side, paged searches make the operation scalable.</span></span> <span data-ttu-id="50f5c-128">Se, ad esempio, i client 100 inviano richieste di ricerca simultaneamente e, in media, ogni client riceve gli oggetti 200.</span><span class="sxs-lookup"><span data-stu-id="50f5c-128">For example, if one hundred clients issue search requests simultaneously and, on the average, each client receives two hundred objects.</span></span> <span data-ttu-id="50f5c-129">Se non viene specificata alcuna dimensione di pagina, nello scenario peggiore il server deve disporre di memoria sufficiente per contenere gli oggetti 20.000.</span><span class="sxs-lookup"><span data-stu-id="50f5c-129">If no page size is specified, in the worst-case scenario, the server must have sufficient memory to hold 20,000 objects.</span></span> <span data-ttu-id="50f5c-130">Viceversa, se ogni client specifica una dimensione di pagina, ad esempio dieci oggetti, il requisito di memoria sul server viene ridotto di un fattore pari a 20.</span><span class="sxs-lookup"><span data-stu-id="50f5c-130">Conversely, if each client specifies a page size to be, for example, ten objects, the memory requirement on the server is thus reduced by a factor of 20.</span></span>

<span data-ttu-id="50f5c-131">Inoltre, l'utilizzo di una ricerca di paging consente a un client di abbandonare l'operazione in corso.</span><span class="sxs-lookup"><span data-stu-id="50f5c-131">In addition, using a paged search, a client can abandon the operation in progress.</span></span> <span data-ttu-id="50f5c-132">Al contrario, in una ricerca non di paging, il client riceve un set di risultati in un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="50f5c-132">In contrast, in a non-paged search, the client receives a result set in one packet.</span></span> <span data-ttu-id="50f5c-133">Ciò può ridurre le prestazioni della rete.</span><span class="sxs-lookup"><span data-stu-id="50f5c-133">This can decrease network performance.</span></span>

<span data-ttu-id="50f5c-134">ADSI gestisce le dimensioni di pagina per il client.</span><span class="sxs-lookup"><span data-stu-id="50f5c-134">ADSI handles the page size for the client.</span></span> <span data-ttu-id="50f5c-135">Il client non deve contare il numero di oggetti in corso.</span><span class="sxs-lookup"><span data-stu-id="50f5c-135">The client does not have to count the number of objects in progress.</span></span> <span data-ttu-id="50f5c-136">ADSI incapsula l'interazione del server per il client.</span><span class="sxs-lookup"><span data-stu-id="50f5c-136">ADSI encapsulates the server interaction for the client.</span></span> <span data-ttu-id="50f5c-137">Dal punto di vista del client, la ricerca restituisce un set di risultati completo.</span><span class="sxs-lookup"><span data-stu-id="50f5c-137">From the client perspective, the search returns a complete result set.</span></span>

<span data-ttu-id="50f5c-138">Si consiglia di utilizzare il paging.</span><span class="sxs-lookup"><span data-stu-id="50f5c-138">It is recommended that paging is used.</span></span>

<span data-ttu-id="50f5c-139">Per specificare una dimensione massima della pagina, impostare un'opzione di ricerca **Ads \_ SEARCHPREF \_ pageSize** con un valore **\_ Integer ADSTYPE** impostato sul numero massimo di righe per pagina nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="50f5c-139">To specify a maximum page size, set an **ADS\_SEARCHPREF\_PAGESIZE** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of rows per page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="50f5c-140">Nell'esempio di codice riportato di seguito viene illustrato come impostare le dimensioni massime della pagina.</span><span class="sxs-lookup"><span data-stu-id="50f5c-140">The following code example shows how to set the maximum page size.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="50f5c-141">Per specificare un'ora di pagina, impostare un'opzione di ricerca per il **\_ limite di tempo di \_ paging \_ \_ ADS SEARCHPREF** con un valore **\_ Integer ADSTYPE** impostato sul numero massimo di secondi che il server deve spendere per recuperare una pagina nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="50f5c-141">To specify a page time, set an **ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of seconds that the server should spend retrieving a page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="50f5c-142">Nell'esempio di codice seguente viene illustrato come specificare l'ora della pagina.</span><span class="sxs-lookup"><span data-stu-id="50f5c-142">The following code example shows how to specify page time.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




