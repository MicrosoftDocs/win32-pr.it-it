---
title: Restituzione solo dei nomi di attributo con IDirectorySearch
description: È possibile eseguire una ricerca per determinare il tipo di dati disponibile per un oggetto specifico.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Restituzione solo dei nomi di attributo con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, restituzione solo di nomi di attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055acbb3fe19969ce95ea77a633e20b195c0257d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297655"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a><span data-ttu-id="0cbdf-105">Restituzione solo dei nomi di attributo con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="0cbdf-105">Returning Only Attribute Names with IDirectorySearch</span></span>

<span data-ttu-id="0cbdf-106">È possibile eseguire una ricerca per determinare il tipo di dati disponibile per un oggetto specifico.</span><span class="sxs-lookup"><span data-stu-id="0cbdf-106">You can perform a search to determine what type of data is available for a particular object.</span></span> <span data-ttu-id="0cbdf-107">In questo caso, si è interessati solo ai nomi degli attributi, non ai valori dell'attributo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0cbdf-107">In this case, you are only interested in the attributes names, not the attribute values of the object.</span></span> <span data-ttu-id="0cbdf-108">L' **opzione \_ Ads \_ SEARCHPREF \_ solo ATTRIBTYPES** fa sì che il server restituisca solo i nomi di attributo e non i valori di attributo.</span><span class="sxs-lookup"><span data-stu-id="0cbdf-108">The **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option causes the server to only return the attribute names and not the attribute values.</span></span> <span data-ttu-id="0cbdf-109">Il set di risultati include tuttavia solo gli attributi a cui sono assegnati valori.</span><span class="sxs-lookup"><span data-stu-id="0cbdf-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="0cbdf-110">Si consideri, ad esempio, un oggetto con gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0cbdf-110">For example, consider an object with the following attributes:</span></span>

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

<span data-ttu-id="0cbdf-111">Quando viene impostata l'opzione **Ads \_ SEARCHPREF \_ ATTRIBTYPES \_ only** , il set di risultati include:</span><span class="sxs-lookup"><span data-stu-id="0cbdf-111">When the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option is set, the result set includes:</span></span>

``` syntax
name
sn
department
phone
```

<span data-ttu-id="0cbdf-112">Il valore predefinito è sia per i valori di attributo che per i nomi da restituire.</span><span class="sxs-lookup"><span data-stu-id="0cbdf-112">The default is for both attribute values and names to be returned.</span></span>

<span data-ttu-id="0cbdf-113">Per recuperare solo i nomi di attributo, impostare un'opzione di ricerca **\_ \_ \_ solo ADS SEARCHPREF ATTRIBTYPES** con un valore **\_ booleano ADSTYPE** **true** nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="0cbdf-113">To retrieve only attribute names, set an **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="0cbdf-114">Nell'esempio di codice seguente viene illustrato come recuperare solo i nomi di attributo.</span><span class="sxs-lookup"><span data-stu-id="0cbdf-114">The following code example shows how to retrieve attribute names only.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



<span data-ttu-id="0cbdf-115">Per altre informazioni e un esempio di codice che illustra come usare l'opzione di ricerca **\_ \_ \_ solo ADS SEARCHPREF ATTRIBTYPES** , vedere il [codice di esempio per la ricerca di attributi](example-code-for-searching-for-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="0cbdf-115">For more information and a code example that shows how to use the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option, see [Example Code for Searching for Attributes](example-code-for-searching-for-attributes.md).</span></span>

 

 




