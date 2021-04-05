---
title: Specifica di altre opzioni di ricerca con IDirectorySearch
description: L'interfaccia IDirectorySearch fornisce un controllo aggiuntivo sul modo in cui viene eseguita la ricerca tramite l'utilizzo delle opzioni di ricerca.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Specifica di altre opzioni di ricerca con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7064a291c3a299a5435ec454a17b1a666f20d0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955080"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a><span data-ttu-id="73f02-105">Specifica di altre opzioni di ricerca con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="73f02-105">Specifying Other Search Options with IDirectorySearch</span></span>

<span data-ttu-id="73f02-106">L'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) fornisce un controllo aggiuntivo sul modo in cui viene eseguita la ricerca tramite l'utilizzo delle opzioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="73f02-106">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provide additional control over how the search is performed through the use of search options.</span></span> <span data-ttu-id="73f02-107">Queste opzioni di ricerca vengono impostate compilando una matrice di [**inserzioni \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) Structures e chiamando il metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="73f02-107">These search options are set by filling in an array of [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) structures and calling the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="73f02-108">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="73f02-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="73f02-109">Utilizzo del metodo SetSearchPreference</span><span class="sxs-lookup"><span data-stu-id="73f02-109">Using the SetSearchPreference Method</span></span>](using-the-setsearchpreference-method.md)
-   [<span data-ttu-id="73f02-110">Ricerche sincrone e asincrone con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="73f02-110">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="73f02-111">Paging con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="73f02-111">Paging with IDirectorySearch</span></span>](paging-with-idirectorysearch.md)
-   [<span data-ttu-id="73f02-112">Caching dei risultati con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="73f02-112">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="73f02-113">Esecuzione di una query sull'ambito degli attributi</span><span class="sxs-lookup"><span data-stu-id="73f02-113">Performing an Attribute Scope Query</span></span>](performing-an-attribute-scoped-query.md)
-   [<span data-ttu-id="73f02-114">Ordinamento dei risultati della ricerca con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="73f02-114">Sorting the Search Results with IDirectorySearch</span></span>](sorting-the-search-results-with-idirectorysearch.md)
-   [<span data-ttu-id="73f02-115">Inseguimento dei riferimenti con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="73f02-115">Referral Chasing with IDirectorySearch</span></span>](referral-chasing-with-idirectorysearch.md)
-   [<span data-ttu-id="73f02-116">Limite dimensioni con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="73f02-116">Size Limit with IDirectorySearch</span></span>](size-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="73f02-117">Limite di tempo del server con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="73f02-117">Server Time Limit with IDirectorySearch</span></span>](server-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="73f02-118">Limite di tempo client con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="73f02-118">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="73f02-119">Restituzione solo dei nomi di attributo con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="73f02-119">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)

 

 




