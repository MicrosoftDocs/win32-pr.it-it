---
title: Codice di esempio per la ricerca di attributi
description: Nell'esempio di codice seguente viene illustrato come usare la preferenza di ricerca ADS \_ SEARCHPREF ATTRIBTYPES ONLY per recuperare solo i nomi degli attributi a cui sono stati assegnati \_ \_ valori.
ms.assetid: 0e166f06-6030-4615-a46d-a282961d3b55
ms.tgt_platform: multiple
keywords:
- ADSI, codice di esempio C/C++, ricerca di attributi
- Codice di esempio per la ricerca di attributi
- ADSI, Ricerca, IDirectorySearch, altre opzioni di ricerca, restituzione solo di nomi di attributi, codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207fcfd2bd688f5bb6ddcd19dcb9b1a87a2e40ddb0a7db1e63e9457e671f9947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428464"
---
# <a name="example-code-for-searching-for-attributes"></a>Codice di esempio per la ricerca di attributi

Nell'esempio di codice seguente viene illustrato come usare la preferenza di ricerca **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** per recuperare solo i nomi degli attributi a cui sono stati assegnati valori. Nell'esempio viene inizializzata una struttura [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) e viene impostata la preferenza di ricerca chiamando il [**metodo SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) dell'interfaccia [**IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) Nell'esempio viene quindi chiamato [**il metodo ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) per eseguire la ricerca.


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



 

 




