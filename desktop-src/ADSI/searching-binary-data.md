---
title: Ricerca di dati binari
description: Anche se la funzionalità di ricerca ADSI supporta solo la ricerca di dati di tipo stringa, è possibile eseguire la ricerca di dati binari.
ms.assetid: 52b75ae0-dbf1-4310-8b6b-a176de9f1b7d
ms.tgt_platform: multiple
keywords:
- Ricerca di dati binari ADSI
- Dati binari ADSI
- Dati binari ADSI, ricerca di dati binari
- ADSI ADSI, codice di esempio C/C++, ricerca di dati binari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0973ff7a769d68abf85e6557fef2e1d434ba3ff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044057"
---
# <a name="searching-binary-data"></a><span data-ttu-id="347f6-107">Ricerca di dati binari</span><span class="sxs-lookup"><span data-stu-id="347f6-107">Searching Binary Data</span></span>

<span data-ttu-id="347f6-108">Anche se la funzionalità di ricerca ADSI supporta solo la ricerca di dati di tipo stringa, è possibile eseguire la ricerca di dati binari.</span><span class="sxs-lookup"><span data-stu-id="347f6-108">Even though the ADSI search feature only supports searching for string data, it is possible to search for binary data.</span></span> <span data-ttu-id="347f6-109">A tale scopo, utilizzare la funzione [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) per convertire i dati binari in una stringa che può essere utilizzata con i metodi di ricerca.</span><span class="sxs-lookup"><span data-stu-id="347f6-109">To do this, use the [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) function to convert the binary data into a string that can be used with the search methods.</span></span> <span data-ttu-id="347f6-110">La ricerca di dati binari è particolarmente utile quando si cerca un GUID o un SID perché questi tipi di dati vengono archiviati come dati binari.</span><span class="sxs-lookup"><span data-stu-id="347f6-110">Searching for binary data is particularly useful when searching for a GUID or a SID because these data types are stored as binary data.</span></span>

<span data-ttu-id="347f6-111">Quando si usa la funzione [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) , è necessario liberare la memoria allocata usando la funzione [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .</span><span class="sxs-lookup"><span data-stu-id="347f6-111">When using the [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) function, the memory allocated must be freed using the [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) function.</span></span>

<span data-ttu-id="347f6-112">Nell'esempio di codice C++ riportato di seguito viene illustrato come compilare una stringa di query per cercare un oggetto con un valore **objectGUID** specifico.</span><span class="sxs-lookup"><span data-stu-id="347f6-112">The following C++ code example shows how to build a query string to search for an object that has a particular **objectGUID** value.</span></span>


```C++
LPWSTR pwszGuid = NULL;
LPWSTR pwszFormat = L"(objectGUID=%s)";
LPWSTR pwszSearch = NULL;
hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
if(FAILED(hr))
{
    goto cleanup;
}

pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
if(NULL == pwszSearch)
{
    goto cleanup;
}
    
swprintf_s(pwszSearch, pwszFormat, pwszGuid);

// Use pwszSearch to perform a query for the object.

cleanup:    
if(pwszGuid)
{
    FreeADsMem(pwszGuid);
}
if(pwszSearch)
{
    delete pwszSearch;
}

```



 

 




