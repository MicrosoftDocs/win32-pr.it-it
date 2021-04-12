---
title: Ricerche sincrone e asincrone con IDirectorySearch
description: Quando si esegue una ricerca usando l'interfaccia IDirectorySearch, il metodo IDirectorySearch ExecuteSearch non invia la richiesta di ricerca al server.
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- Ricerche sincrone e asincrone con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, ricerche sincrone e asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f369d45aaf4453d310c4bac2259bfa9cd089f567
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395274"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a><span data-ttu-id="cd098-105">Ricerche sincrone e asincrone con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="cd098-105">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>

<span data-ttu-id="cd098-106">Quando si esegue una ricerca usando l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , il metodo [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) non invia la richiesta di ricerca al server.</span><span class="sxs-lookup"><span data-stu-id="cd098-106">When you perform a search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method does not send the search request to the server.</span></span> <span data-ttu-id="cd098-107">Questo metodo salva solo i parametri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="cd098-107">This method only saves the search parameters.</span></span> <span data-ttu-id="cd098-108">La richiesta di ricerca viene effettivamente inviata quando si chiama [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).</span><span class="sxs-lookup"><span data-stu-id="cd098-108">The search request is actually sent when you call [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).</span></span>

<span data-ttu-id="cd098-109">Per Active Directory le ricerche, la differenza principale tra sincrona e asincrona è quando viene restituita la prima riga del risultato, ovvero quando viene restituita la prima chiamata a [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .</span><span class="sxs-lookup"><span data-stu-id="cd098-109">For Active Directory searches, the primary difference between synchronous and asynchronous is when the first row of the result is returned, that is, when the first [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) call returns.</span></span>

<span data-ttu-id="cd098-110">In una ricerca sincrona, se il paging non è abilitato, la prima riga viene restituita quando il server ha costruito e restituito l'intero set di risultati al client.</span><span class="sxs-lookup"><span data-stu-id="cd098-110">In a synchronous search, if paging is not enabled, the first row is returned when the server has constructed and returned the entire result set to the client.</span></span> <span data-ttu-id="cd098-111">Se il paging è abilitato, la prima riga viene restituita quando viene restituita la prima pagina del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="cd098-111">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="cd098-112">In una ricerca asincrona, se il paging non è abilitato, viene restituita la prima riga quando il server ha creato la prima riga del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="cd098-112">In an asynchronous search, if paging is not enabled, the first row is returned when the server has constructed the first row of the result set.</span></span> <span data-ttu-id="cd098-113">Se il paging è abilitato, la prima riga viene restituita quando viene restituita la prima pagina del set di risultati.</span><span class="sxs-lookup"><span data-stu-id="cd098-113">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="cd098-114">Il tipo di ricerca predefinito è sincrono.</span><span class="sxs-lookup"><span data-stu-id="cd098-114">The default search type is synchronous.</span></span> <span data-ttu-id="cd098-115">Per specificare una ricerca asincrona, impostare un'opzione di ricerca **\_ \_ asincrona ADS SEARCHPREF** con un valore **\_ booleano ADSTYPE** **true** nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="cd098-115">To specify an asynchronous search, set an **ADS\_SEARCHPREF\_ASYNCHRONOUS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="cd098-116">Questa operazione è illustrata nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="cd098-116">This operation is shown in the following code example.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




