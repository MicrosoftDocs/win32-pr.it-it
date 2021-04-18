---
title: Limite dimensioni con IDirectorySearch
description: Il client può concentrarsi su un numero ridotto di oggetti restituiti dal server e ignorare il resto del set di risultati.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Limite dimensioni con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, limite dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25127ea945edcf669e71d7d5b3f969d9eb2cb112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297650"
---
# <a name="size-limit-with-idirectorysearch"></a><span data-ttu-id="dc989-105">Limite dimensioni con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="dc989-105">Size Limit with IDirectorySearch</span></span>

<span data-ttu-id="dc989-106">Per ridurre il requisito di memoria o per altri scopi, il client può concentrarsi su un numero ridotto di oggetti restituiti dal server e ignorare il resto del set di risultati che non sono di interesse.</span><span class="sxs-lookup"><span data-stu-id="dc989-106">To reduce the memory requirement or for other purposes, the client can focus on a small number of objects returned from the server and ignore the rest of the result set that are not of interest.</span></span> <span data-ttu-id="dc989-107">A tale scopo, il client specifica il limite delle dimensioni di ricerca e altri criteri di ricerca appropriati.</span><span class="sxs-lookup"><span data-stu-id="dc989-107">To accomplish this, the client specifies the search size limit and other appropriate search criteria.</span></span> <span data-ttu-id="dc989-108">Se, ad esempio, la directory archivia i punteggi dei test di un quartiere School, è possibile eseguire una query sui primi dieci studenti con i punteggi di test più elevati specificando un limite di dimensioni pari a dieci (10) e un ordinamento decrescente.</span><span class="sxs-lookup"><span data-stu-id="dc989-108">For example, if the directory stores the test scores of a school district, you can query the top ten students with the highest test scores by specifying a size limit of ten (10) and a descending sort order.</span></span>

<span data-ttu-id="dc989-109">Il valore predefinito per il limite delle dimensioni non è limite.</span><span class="sxs-lookup"><span data-stu-id="dc989-109">The default for size limit is no limit.</span></span> <span data-ttu-id="dc989-110">Per impostare un limite di dimensioni, impostare un'opzione di ricerca per il **\_ limite di \_ dimensioni \_ ADS SEARCHPREF** con un valore **\_ Integer ADSTYPE** che contenga le dimensioni massime della matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="dc989-110">To set a size limit, set an **ADS\_SEARCHPREF\_SIZE\_LIMIT** search option with an **ADSTYPE\_INTEGER** value that contains the maximum size in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="dc989-111">Nell'esempio di codice riportato di seguito viene illustrato come impostare il limite delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="dc989-111">The following code example shows how to set the size limit.</span></span> <span data-ttu-id="dc989-112">Un valore di limite di dimensioni pari a zero indica un limite di dimensioni.</span><span class="sxs-lookup"><span data-stu-id="dc989-112">A size limit value of zero indicates no size limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="dc989-113">Per Active Directory, il limite di dimensioni specifica il numero massimo di oggetti che devono essere restituiti dalla ricerca.</span><span class="sxs-lookup"><span data-stu-id="dc989-113">For Active Directory, the size limit specifies the maximum number of objects to be returned by the search.</span></span> <span data-ttu-id="dc989-114">Inoltre, per Active Directory, il numero massimo di oggetti restituiti da una ricerca è 1000 oggetti.</span><span class="sxs-lookup"><span data-stu-id="dc989-114">Also for Active Directory, the maximum number of objects returned by a search is 1000 objects.</span></span>

 

 




