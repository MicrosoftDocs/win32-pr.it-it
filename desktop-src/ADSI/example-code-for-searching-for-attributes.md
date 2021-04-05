---
title: Codice di esempio per la ricerca di attributi
description: Nell'esempio di codice seguente viene illustrato come utilizzare la \_ preferenza di ricerca ADS SEARCHPREF \_ ATTRIBTYPES \_ solo per recuperare solo i nomi degli attributi a cui sono stati assegnati i valori.
ms.assetid: 0e166f06-6030-4615-a46d-a282961d3b55
ms.tgt_platform: multiple
keywords:
- ADSI, codice di esempio C/C++, ricerca di attributi
- Codice di esempio per la ricerca di attributi
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, restituzione solo dei nomi di attributo, esempio di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344ce99fe9de606212d786ff2e7b88b5eba34d14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707432"
---
# <a name="example-code-for-searching-for-attributes"></a><span data-ttu-id="ef2cf-106">Codice di esempio per la ricerca di attributi</span><span class="sxs-lookup"><span data-stu-id="ef2cf-106">Example Code for Searching for Attributes</span></span>

<span data-ttu-id="ef2cf-107">Nell'esempio di codice seguente viene illustrato come utilizzare la preferenza di ricerca **Ads \_ SEARCHPREF \_ ATTRIBTYPES \_ solo** per recuperare solo i nomi degli attributi a cui sono stati assegnati i valori.</span><span class="sxs-lookup"><span data-stu-id="ef2cf-107">The following code example shows how to use the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search preference to retrieve only the names of attributes to which values have been assigned.</span></span> <span data-ttu-id="ef2cf-108">L'esempio Inizializza una struttura [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) e imposta la preferenza di ricerca chiamando il metodo [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) dell'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="ef2cf-108">The example initializes an [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) structure and sets the search preference by calling the [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method of the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span> <span data-ttu-id="ef2cf-109">Nell'esempio viene quindi chiamato il metodo [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) per eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="ef2cf-109">The example then calls the [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method to perform the search.</span></span>


```C++
// Setting the search preference.
// m_pSearch is a valid pointer to an IDirectorySearch interface.
ADS_SEARCHPREF_INFO prefInfo[1];
LPWSTR pszColumn = NULL;

// Set the search preference to indicate attribute names only.
prefInfo[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
prefInfo[0].vValue.dwType = ADSTYPE_BOOLEAN;
prefInfo[0].vValue.Integer = TRUE;
hr = m_pSearch->SetSearchPreference(prefInfo, 1);

// Execute the search.
hr = m_pSearch->ExecuteSearch(
                L"(|(objectCategory=domainDNS)(objectCategory=organizationalUnit))", 
                NULL, -1, &hSearch );

if(FAILED(hr))
{
   return;
}

// Retrieve the column name.
hr = m_pSearch->GetNextRow(hSearch);

if(FAILED(hr))
{
   return;
}
    
while( m_pSearch->GetNextColumnName( hSearch, &pszColumn ) != S_ADS_NOMORE_COLUMNS )
{
   wprintf(L"%S ", pszColumn );
   FreeADsMem( pszColumn );
}
```



 

 




