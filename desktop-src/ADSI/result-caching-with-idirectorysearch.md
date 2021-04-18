---
title: Caching dei risultati con IDirectorySearch
description: La \_ \_ preferenza per i risultati della cache ADS SEARCHPREF memorizza nella \_ cache il set di risultati nel client.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Caching dei risultati con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, Caching di risultati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95016699eb4de36344b7e40f35e1a4a9cce761b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328372"
---
# <a name="result-caching-with-idirectorysearch"></a><span data-ttu-id="5b55e-105">Caching dei risultati con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="5b55e-105">Result Caching with IDirectorySearch</span></span>

<span data-ttu-id="5b55e-106">La preferenza per i **\_ Risultati della \_ cache \_ ADS SEARCHPREF** memorizza nella cache il set di risultati nel client.</span><span class="sxs-lookup"><span data-stu-id="5b55e-106">The **ADS\_SEARCHPREF\_CACHE\_RESULTS** preference caches the result set on the client.</span></span> <span data-ttu-id="5b55e-107">La memorizzazione nella cache dei risultati consente a un'applicazione di mantenere un set di risultati recuperato e di eseguire nuovamente le righe recuperate.</span><span class="sxs-lookup"><span data-stu-id="5b55e-107">Result caching enables an application to retain a retrieved result set and go through the retrieved rows again.</span></span> <span data-ttu-id="5b55e-108">Consente inoltre il supporto dei cursori in cui è possibile utilizzare i metodi [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) e [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) per spostarsi verso l'alto e verso il basso del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="5b55e-108">It also enables cursor support where the [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) and [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) methods can be used to move up and down the result set.</span></span>

<span data-ttu-id="5b55e-109">Per impostazione predefinita, la memorizzazione nella cache dei risultati è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="5b55e-109">By default, result caching is disabled.</span></span> <span data-ttu-id="5b55e-110">La memorizzazione nella cache dei risultati deve essere abilitata se si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5b55e-110">Result caching should be enabled if any one of the following is true:</span></span>

-   <span data-ttu-id="5b55e-111">Se lo stesso set di risultati deve essere enumerato più volte senza eseguire di nuovo la ricerca nel server.</span><span class="sxs-lookup"><span data-stu-id="5b55e-111">If the same result set must be enumerated multiple times without performing the search again on the server.</span></span>
-   <span data-ttu-id="5b55e-112">Se l'esecuzione della ricerca prevede un utilizzo intensivo delle risorse sul server (connessione lenta, set di risultati di grandi dimensioni o query complesse).</span><span class="sxs-lookup"><span data-stu-id="5b55e-112">If performing the search is resource-intensive on the server (slow connection, large result set, or complex query).</span></span>
-   <span data-ttu-id="5b55e-113">Se è richiesto il supporto del cursore.</span><span class="sxs-lookup"><span data-stu-id="5b55e-113">If cursor support is required.</span></span>

<span data-ttu-id="5b55e-114">Disattivare la memorizzazione nella cache se l'applicazione deve ridurre i requisiti di memoria per la memorizzazione nella cache di un set di risultati di grandi dimensioni nel client.</span><span class="sxs-lookup"><span data-stu-id="5b55e-114">Turn off caching if your application must reduce memory requirements for caching a large result set at the client.</span></span>

<span data-ttu-id="5b55e-115">La memorizzazione nella cache dei risultati aumenta i requisiti di memoria sul client, quindi la memorizzazione dei risultati nella cache dovrebbe essere disabilitata se si tratta di un problema.</span><span class="sxs-lookup"><span data-stu-id="5b55e-115">Result caching increases the memory requirements on the client, so result caching should be disabled if this is a concern.</span></span>

<span data-ttu-id="5b55e-116">Per abilitare la memorizzazione nella cache dei risultati, impostare un'opzione di ricerca per i **\_ \_ \_ Risultati della cache ADS SEARCHPREF** con un valore **\_ booleano ADSTYPE** **true** nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="5b55e-116">To enable result caching, set an **ADS\_SEARCHPREF\_CACHE\_RESULTS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="5b55e-117">Nell'esempio di codice seguente viene illustrato come abilitare la memorizzazione dei risultati nella cache.</span><span class="sxs-lookup"><span data-stu-id="5b55e-117">The following code example shows how to enable result caching.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




