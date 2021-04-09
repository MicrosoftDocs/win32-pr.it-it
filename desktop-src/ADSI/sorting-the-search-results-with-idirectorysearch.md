---
title: Ordinamento dei risultati della ricerca con IDirectorySearch
description: Per impostazione predefinita, i risultati di una ricerca vengono restituiti in un ordine non garantito. L'opzione ADS \_ SEARCHPREF \_ Sort \_ on preferenza indica al server di ordinare il set di risultati in un valore di attributo specificato prima che venga restituito al client.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Ordinamento dei risultati della ricerca con IDirectorySearch
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, ordinamento dei risultati della ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433d24b06ac4d361d6520d8af3376ea12acac1f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730239"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a><span data-ttu-id="38a3b-106">Ordinamento dei risultati della ricerca con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="38a3b-106">Sorting the Search Results with IDirectorySearch</span></span>

<span data-ttu-id="38a3b-107">Per impostazione predefinita, i risultati di una ricerca vengono restituiti in un ordine non garantito.</span><span class="sxs-lookup"><span data-stu-id="38a3b-107">By default, the results of a search are returned in no guaranteed order.</span></span> <span data-ttu-id="38a3b-108">L'opzione **Ads \_ SEARCHPREF \_ Sort \_ on** preferenza indica al server di ordinare il set di risultati in un valore di attributo specificato prima che venga restituito al client.</span><span class="sxs-lookup"><span data-stu-id="38a3b-108">The **ADS\_SEARCHPREF\_SORT\_ON** preference instructs the server to sort the result set on a specified attribute value before it is returned to the client.</span></span>

<span data-ttu-id="38a3b-109">È consigliabile usare gli attributi indicizzati per l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="38a3b-109">It is recommended that indexed attributes be used for sorting.</span></span> <span data-ttu-id="38a3b-110">In caso contrario, il server deve recuperare il set di risultati completo e ordinarlo prima di inviare i risultati al client.</span><span class="sxs-lookup"><span data-stu-id="38a3b-110">Otherwise, the server must retrieve the complete result set and sort it before sending any results to the client.</span></span> <span data-ttu-id="38a3b-111">Questo vale anche per le ricerche con paging.</span><span class="sxs-lookup"><span data-stu-id="38a3b-111">This also applies to paged searches.</span></span> <span data-ttu-id="38a3b-112">Tenere presente che le prestazioni di una ricerca ordinata verranno aumentate se il filtro include un attributo indicizzato e tale attributo viene specificato come chiave di ordinamento. in questo caso, Active Directory possibile soddisfare l'ordinamento durante l'elaborazione del filtro.</span><span class="sxs-lookup"><span data-stu-id="38a3b-112">Be aware that performance of a sorted search will be increased if the filter includes an indexed attribute and that attribute is specified as the sort key; in this case, Active Directory can satisfy the sort while processing the filter.</span></span> <span data-ttu-id="38a3b-113">Una query di ordinamento efficace per un set di utenti, ad esempio, potrebbe avere un filtro incluso (sn>Smith) e una chiave di ordinamento di sn.</span><span class="sxs-lookup"><span data-stu-id="38a3b-113">For example, an efficient sort query for a set of users could have a filter that included (sn>smith) and a sort key of sn.</span></span>

<span data-ttu-id="38a3b-114">L'ordinamento lato server con l'opzione di ricerca **Ads \_ SEARCHPREF \_ Sort \_ on** consente di ridurre le prestazioni del server.</span><span class="sxs-lookup"><span data-stu-id="38a3b-114">Server-side sorting with the **ADS\_SEARCHPREF\_SORT\_ON** search option will reduce the performance of the server.</span></span> <span data-ttu-id="38a3b-115">Se si eseguono numerose ricerche, è consigliabile ordinare manualmente i risultati sul lato client per ridurre il carico di lavoro nel server.</span><span class="sxs-lookup"><span data-stu-id="38a3b-115">If you will be performing many searches, consider sorting the results manually on the client side to reduce the workload on the server.</span></span>

<span data-ttu-id="38a3b-116">Per impostazione predefinita, l'ordinamento dei risultati è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="38a3b-116">By default, result sorting is disabled.</span></span> <span data-ttu-id="38a3b-117">Per abilitare l'ordinamento dei risultati, impostare un'opzione di ricerca **Ads \_ SEARCHPREF \_ Sort \_ on** con un **ADSTYPE \_ prov \_ specific** che punta a una struttura [**\_ SORTKEY ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="38a3b-117">To enable result sorting, set an **ADS\_SEARCHPREF\_SORT\_ON** search option with an **ADSTYPE\_PROV\_SPECIFIC** that points to an [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="38a3b-118">La **struttura \_ SORTKEY ADS** viene utilizzata per specificare l'attributo in base al quale eseguire l'ordinamento e l'ordine dell'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="38a3b-118">The **ADS\_SORTKEY** structure is used to specify the attribute to sort on and the order of the sort.</span></span>

<span data-ttu-id="38a3b-119">Nell'esempio di codice seguente viene illustrato come abilitare l'ordinamento dei risultati.</span><span class="sxs-lookup"><span data-stu-id="38a3b-119">The following code example shows how to enable result sorting.</span></span>


```C++
ADS_SORTKEY SortKey;
SortKey.pszAttrType = L"cn";
SortKey.pszReserved = NULL;
SortKey.fReverseorder = FALSE;

ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SORT_ON;
SearchPref.vValue.dwType = ADSTYPE_PROV_SPECIFIC;
SearchPref.vValue.ProviderSpecific.dwLength = sizeof(SortKey);
SearchPref.vValue.ProviderSpecific.lpValue = (LPBYTE)&SortKey;
```



<span data-ttu-id="38a3b-120">Active Directory non supporta l'ordinamento sugli attributi costruiti, pertanto non è possibile specificare un attributo costruito per l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="38a3b-120">Active Directory does not support sorting on constructed attributes, so it is not possible to specify a constructed attribute for sorting.</span></span> <span data-ttu-id="38a3b-121">Non è inoltre possibile utilizzare l'attributo [**Distinguishname**](/windows/desktop/ADSchema/a-distinguishedname) per l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="38a3b-121">The [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) attribute also cannot be used for sorting.</span></span> <span data-ttu-id="38a3b-122">Active Directory inoltre non consente l'ordinamento su più di un attributo, pertanto l'opzione **di ricerca Ads \_ SEARCHPREF \_ Sort \_ on** può contenere solo una [**struttura \_ SORTKEY ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) .</span><span class="sxs-lookup"><span data-stu-id="38a3b-122">Active Directory also does not allow sorting on more than one attribute, so the **ADS\_SEARCHPREF\_SORT\_ON** search option can only contain one [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure.</span></span>

 

 