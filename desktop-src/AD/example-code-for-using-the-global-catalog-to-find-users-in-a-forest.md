---
title: Codice di esempio per l'uso del catalogo globale per trovare gli utenti in una foresta
description: Questo argomento include esempi di codice usati per cercare gli utenti in una foresta.
ms.assetid: bdcbfb7e-e1ea-4275-96b0-1c895e28e176
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, uso del catalogo globale per trovare gli utenti in una foresta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea13ac3dbc4455d10dbd56f78e50c0f2ea27301
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707630"
---
# <a name="example-code-for-using-the-global-catalog-to-find-users-in-a-forest"></a><span data-ttu-id="a0e06-104">Codice di esempio per l'uso del catalogo globale per trovare gli utenti in una foresta</span><span class="sxs-lookup"><span data-stu-id="a0e06-104">Example Code for Using the Global Catalog to Find Users in a Forest</span></span>

<span data-ttu-id="a0e06-105">Questo argomento include esempi di codice usati per cercare gli utenti in una foresta.</span><span class="sxs-lookup"><span data-stu-id="a0e06-105">This topic includes code examples used to search for users in a forest.</span></span>

<span data-ttu-id="a0e06-106">Nell'esempio di codice Visual Basic riportato di seguito viene illustrato come utilizzare ADSI per cercare gli utenti in una foresta.</span><span class="sxs-lookup"><span data-stu-id="a0e06-106">The following Visual Basic code example shows how to use ADSI to search for users in a forest.</span></span>


```VB
''''''''''''''''''''''''''''''''''''''''
'
'   PrintAllUsersInGlobalCatalog()
'
'   Prints to the debug window the cn and disintguishedName of all users in the
'   current forest whose givenName begins with "jeff". This is accomplished
'   by binding to the global catalog and then searching for all users
'   objects that meet the criteria.
'
'   Be aware that this code example can be modified to print all users in the
'   forest, but on a large enterprise, it can take a long time to search for
'   and print all users. The filter in this example is only given to
'   avoid excessive network traffic.
'
''''''''''''''''''''''''''''''''''''''''
Public Sub PrintAllUsersInGlobalCatalog()
    Const ADS_SECURE_AUTHENTICATION = 1
    
    Dim oGC As IADsContainer
    Dim oEntrprise As IADs
    
    ' Get the enterprise object from the GC namespace.
    Set oGC = GetObject("GC:")
    For Each child In oGC
        Set oEntrprise = child
        Exit For
    Next
    
    ' Setup ADO.
    Set oConn = CreateObject("ADODB.Connection")
    Set oComm = CreateObject("ADODB.Command")
     
    oConn.Provider = "ADsDSOObject"
    oConn.Properties("ADSI Flag") = ADS_SECURE_AUTHENTICATION
    
    oConn.Open
    oComm.ActiveConnection = oConn
    
    ' Set the search command and filter.
    oComm.CommandText = "<" & oEntrprise.ADsPath & ">;(&(objectCategory=person)(objectClass=user)(givenName=jeff*));cn,distinguishedName;subTree"
    
    ' Execute the query.
    Set oRS = oComm.Execute
    
    ' Print the results.
    oRS.MoveFirst
    While Not oRS.EOF
        For Each field In oRS.Fields
            Debug.Print field
        Next
        
        Debug.Print ""
        oRS.MoveNext
    Wend
End Sub
```



<span data-ttu-id="a0e06-107">Nell'esempio di codice C++ riportato di seguito viene utilizzato ADSI per cercare gli utenti in una foresta.</span><span class="sxs-lookup"><span data-stu-id="a0e06-107">The following C++ code example uses ADSI to search for users in a forest.</span></span>


```C++
/***************************************************************************

    PrintAllUsersInGlobalCatalog()

    Prints to the console the cn and disintguishedName of all users in the 
    current forest whose givenName begins with "jeff". This is accomplished 
    by binding to the global catalog and then searching for all users 
    objects that meet the criteria.

    Be aware that this code example can be modified to print all users in the
    forest, but on a large enterprise, it can take a long time to search for
    and print all users. The filter in this example is only given to
    avoid excessive network traffic.

***************************************************************************/

HRESULT PrintAllUsersInGlobalCatalog()
{
    HRESULT hr;
    CComPtr<IADsContainer> spContainer;
 
    // Bind to global catalog.
    hr = ADsOpenObject(L"GC:",
                NULL,
                NULL,
                ADS_SECURE_AUTHENTICATION,
                IID_IADsContainer,
                (void**)&spContainer);
    if(FAILED(hr))
    {
        return hr;
    }
 
    CComPtr<IEnumVARIANT> spEnum;
    hr = spContainer->get__NewEnum((IUnknown**)&spEnum);
    if(FAILED(hr))
    {
        return hr;
    }

    // Enumerate. There should be only one item.
    CComPtr<IDirectorySearch> spGCSearch;
    CComVariant svar;
    ULONG ulFetched;

    /*
    Get the first item in the enumeration. The global catalog container will 
    only have one object in it.
    */
    hr = spEnum->Next(1, &svar, &ulFetched);
    if(SUCCEEDED(hr) && (ulFetched == 1) && (VT_DISPATCH == svar.vt))
    {
        hr = svar.pdispVal->QueryInterface(IID_IDirectorySearch, (LPVOID*)&spGCSearch);
    }

    if(FAILED(hr))
    {
        return hr;
    }
    else if(NULL == spGCSearch.p)
    {
        return E_FAIL;
    }
 
    ADS_SEARCHPREF_INFO SearchPrefs[2];

    // Search entire subtree from root.
    SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    SearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    SearchPrefs[0].vValue.Integer = ADS_SCOPE_SUBTREE;
 
    /*
    Use paging in case there are more results than the server can provide in a single page.
    */
    SearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
    SearchPrefs[1].vValue.dwType = ADSTYPE_INTEGER;
    SearchPrefs[1].vValue.Integer = 1000;
 
    // Set the search preference.
    hr = spGCSearch->SetSearchPreference(SearchPrefs, sizeof(SearchPrefs)/sizeof(ADS_SEARCHPREF_INFO));
    if(FAILED(hr))
    {
        return hr;
    }

    ADS_SEARCH_HANDLE hSearch;
    
    // Create the search filter.
    LPWSTR pwszSearchFilter = L"(&(objectCategory=person)(objectClass=user)(givenName=jeff*))";
 
    // Set attributes to return.
    LPWSTR rgpwszAttributes[] = {L"cn", L"distinguishedName"};
    DWORD dwNumAttributes = sizeof(rgpwszAttributes)/sizeof(LPWSTR);
 
    // Execute the search.
    hr = spGCSearch->ExecuteSearch( pwszSearchFilter,
                                    rgpwszAttributes,
                                    dwNumAttributes,
                                    &hSearch);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the first result row.
    hr = spGCSearch->GetFirstRow(hSearch);
    while(S_OK == hr)
    {
        ADS_SEARCH_COLUMN col;

        // Enumerate the retrieved attributes.
        for(DWORD i = 0; i < dwNumAttributes; i++)
        {
            hr = spGCSearch->GetColumn(hSearch, rgpwszAttributes[i], &col);
            if(SUCCEEDED(hr))
            {
                switch(col.dwADsType)
                {
                case ADSTYPE_DN_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].DNString);
                    break;

                case ADSTYPE_CASE_IGNORE_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].CaseExactString);
                    break;

                default:
                    break;
                }
                
                // Free the column.
                spGCSearch->FreeColumn(&col);
            }
        }
        
        // Get the next row.
        hr = spGCSearch->GetNextRow(hSearch);
    }

    // Close the search handle to cleanup.
    hr = spGCSearch->CloseSearchHandle(hSearch);

    return hr;
}
```



 

 




