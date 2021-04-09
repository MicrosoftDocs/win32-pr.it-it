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
# <a name="searching-binary-data"></a>Ricerca di dati binari

Anche se la funzionalità di ricerca ADSI supporta solo la ricerca di dati di tipo stringa, è possibile eseguire la ricerca di dati binari. A tale scopo, utilizzare la funzione [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) per convertire i dati binari in una stringa che può essere utilizzata con i metodi di ricerca. La ricerca di dati binari è particolarmente utile quando si cerca un GUID o un SID perché questi tipi di dati vengono archiviati come dati binari.

Quando si usa la funzione [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) , è necessario liberare la memoria allocata usando la funzione [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .

Nell'esempio di codice C++ riportato di seguito viene illustrato come compilare una stringa di query per cercare un oggetto con un valore **objectGUID** specifico.


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



 

 




