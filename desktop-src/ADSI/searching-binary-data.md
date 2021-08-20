---
title: Ricerca di dati binari
description: Anche se la funzionalità di ricerca ADSI supporta solo la ricerca di dati stringa, è possibile cercare dati binari.
ms.assetid: 52b75ae0-dbf1-4310-8b6b-a176de9f1b7d
ms.tgt_platform: multiple
keywords:
- Ricerca di dati binari ADSI
- DATI BINARI ADSI
- Dati binari ADSI , ricerca di dati binari
- ADSI ADSI , Codice di esempio C/C++, Ricerca di dati binari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f77ead11f4e2d02c6e7ef3e25975a7059c2c057dbc62f71e406bbda3e24c3b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005421"
---
# <a name="searching-binary-data"></a>Ricerca di dati binari

Anche se la funzionalità di ricerca ADSI supporta solo la ricerca di dati stringa, è possibile cercare dati binari. A tale scopo, usare la [**funzione ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) per convertire i dati binari in una stringa che può essere usata con i metodi di ricerca. La ricerca di dati binari è particolarmente utile quando si cerca un GUID o un SID perché questi tipi di dati vengono archiviati come dati binari.

Quando si usa [**la funzione ADsEncodeBinaryData,**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) la memoria allocata deve essere liberata usando la [**funzione FreeADsMem.**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)

Nell'esempio di codice C++ seguente viene illustrato come compilare una stringa di query per cercare un oggetto con un **valore objectGUID** specifico.


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



 

 




