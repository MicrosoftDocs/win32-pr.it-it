---
title: Recupero di oggetti eliminati
description: Gli oggetti eliminati vengono archiviati nel contenitore Oggetti eliminati.
ms.assetid: dc9a6466-204b-4a78-b0f3-9c03c13a374b
ms.tgt_platform: multiple
keywords:
- Recupero di oggetti eliminati AD
- oggetto AD, recupero di oggetti eliminati
- Active Directory, uso, recupero di oggetti eliminati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b033a992599fecfc372bf578c1bade54867fd8332c3e114103a69264f736b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025089"
---
# <a name="retrieving-deleted-objects"></a>Recupero di oggetti eliminati

Gli oggetti eliminati vengono archiviati nel contenitore Oggetti eliminati. Il contenitore Oggetti eliminati non è in genere visibile, ma il contenitore Oggetti eliminati può essere associato da un membro del gruppo Administrators. Il contenuto del contenitore Degli oggetti eliminati può essere enumerato ed è possibile ottenere singoli attributi degli oggetti eliminati usando [**l'interfaccia IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) con la preferenza di ricerca **\_ ADS SEARCHPREF \_ TOMBSTONE.**

Il contenitore Deleted Objects può essere ottenuto tramite l'associazione al **noto GUID DELETED OBJECTS \_ \_ \_ CONTAINER** definito in Ntdsapi.h. Per altre informazioni sull'associazione a GUID noti, vedere [Binding a oggetti Well-Known mediante WKGUID.](binding-to-well-known-objects-using-wkguid.md)

Specificare **l'opzione ADS \_ FAST \_ BIND** quando si esegue l'associazione al contenitore Degli oggetti eliminati. Ciò significa che le interfacce ADSI usate per lavorare con un oggetto in Active Directory Domain Services, ad esempio [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsPropertyList,**](/windows/desktop/api/iads/nn-iads-iadspropertylist)non possono essere usate nel contenitore degli oggetti eliminati. Per altre informazioni e un esempio di codice che illustra come eseguire l'associazione al contenitore Oggetti eliminati, vedere la funzione di esempio GetDeletedObjectsContainer riportata di seguito.

-   [Enumerazione di oggetti eliminati](#enumerating-deleted-objects)
-   [Ricerca di un oggetto eliminato specifico](#finding-a-specific-deleted-object)
    -   [GetDeletedObjectsContainer](#getdeletedobjectscontainer)
    -   [EnumDeletedObjects](#enumdeletedobjects)
    -   [FindDeletedObjectByGUID](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a>Enumerazione di oggetti eliminati

[**L'interfaccia IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) viene usata per cercare gli oggetti eliminati.

**Per enumerare gli oggetti eliminati**

1.  Ottenere [**l'interfaccia IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) per il contenitore Degli oggetti eliminati. Questa operazione viene eseguita tramite l'associazione al contenitore Oggetti eliminati e la richiesta **dell'interfaccia IDirectorySearch.** Per altre informazioni e un esempio di codice che illustra come eseguire l'associazione al contenitore Oggetti eliminati, vedere l'esempio di funzione **GetDeletedObjectsContainer** seguente.
2.  Impostare la **preferenza di ricerca \_ ADS SEARCHPREF \_ SEARCH \_ SCOPE** su **ADS SCOPE \_ \_ ONELEVEL** usando il [**metodo IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) È anche possibile usare la preferenza **\_ ADS SCOPE \_ SUBTREE,** ma il contenitore Degli oggetti eliminati è un solo livello, quindi l'uso di **ADS \_ SCOPE \_ SUBTREE** è ridondante.
3.  Impostare la **preferenza di \_ ricerca ADS SEARCHPREF \_ TOMBSTONE** su **TRUE.** In questo modo la ricerca include gli oggetti eliminati.
4.  Impostare la **preferenza di \_ ricerca ADS SEARCHPREF \_ PAGESIZE** su un valore minore o uguale a 1000. Questa operazione è facoltativa, ma se questa operazione non viene eseguita, non è possibile recuperare più di 1000 oggetti eliminati.
5.  Impostare il filtro di ricerca [**nella chiamata IDirectorySearch::ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) su "(isDeleted=**TRUE**)". In questo modo la ricerca recupera solo gli oggetti con **l'attributo isDeleted** impostato su **TRUE.**

Per un codice di esempio di codice che illustra come enumerare gli oggetti eliminati, vedere l'esempio di funzione **EnumDeletedObjects** seguente.

La ricerca può essere ulteriormente perfezionata aggiungendo al filtro di ricerca, come illustrato in [Dialetto LDAP.](/windows/desktop/ADSI/ldap-dialect) Ad esempio, per cercare tutti gli oggetti eliminati con un nome che inizia con "Jeff", il filtro di ricerca verrà impostato su "(&(isDeleted=**TRUE**)(cn=Jeff \* ))".

Poiché la maggior parte degli attributi degli oggetti eliminati viene rimossa quando vengono eliminati, non è possibile eseguire direttamente l'associazione a un oggetto eliminato. **L'opzione ADS \_ FAST \_ BIND** deve essere specificata durante l'associazione a un oggetto eliminato. Ciò significa che le interfacce ADSI usate per lavorare con un oggetto Active Directory Domain Services, ad esempio [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsPropertyList,**](/windows/desktop/api/iads/nn-iads-iadspropertylist)non possono essere usate in un contenitore di oggetti eliminato.

## <a name="finding-a-specific-deleted-object"></a>Ricerca di un oggetto eliminato specifico

È anche possibile trovare un oggetto eliminato specifico. Se **l'objectGUID** dell'oggetto è noto, può essere usato per cercare l'oggetto con tale **objectGUID specifico.** Per altre informazioni e un esempio di codice che illustra come trovare un oggetto eliminato specifico, vedere **FindDeletedObjectByGUID** di seguito.

### <a name="getdeletedobjectscontainer"></a>GetDeletedObjectsContainer

Nell'esempio di codice C++ seguente viene illustrato come eseguire l'associazione al contenitore Deleted Objects.


```C++
//***************************************************************************
//
//  GetDeletedObjectsContainer()
//
//  Binds to the Deleted Object container.
//
//***************************************************************************

HRESULT GetDeletedObjectsContainer(IADsContainer **ppContainer)
{
    if(NULL == ppContainer)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppContainer = NULL;

    // Bind to the rootDSE object.
    hr = ADsOpenObject(L"LDAP://rootDSE",
                    NULL,
                    NULL,
                    ADS_SECURE_AUTHENTICATION,
                    IID_IADs,
                    (LPVOID*)&pRoot);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        
        VariantInit(&var);

        // Get the current domain DN.
        hr = pRoot->Get(CComBSTR("defaultNamingContext"), &var);
        if(SUCCEEDED(hr))
        {
            // Build the binding string.
            LPWSTR pwszFormat = L"LDAP://<WKGUID=%s,%s>";
            LPWSTR pwszPath;

            pwszPath = new WCHAR[wcslen(pwszFormat) + wcslen(GUID_DELETED_OBJECTS_CONTAINER_W) + wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, pwszFormat, GUID_DELETED_OBJECTS_CONTAINER_W, var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_FAST_BIND | ADS_SECURE_AUTHENTICATION,
                                IID_IADsContainer,
                                (LPVOID*)ppContainer);

                delete pwszPath;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }

            VariantClear(&var);        
        }

        pRoot->Release(); 
    }

    return hr;
}

```



### <a name="enumdeletedobjects"></a>EnumDeletedObjects

Nell'esempio di codice C++ seguente viene illustrato come enumerare gli oggetti nel contenitore Deleted Objects.


```C++
//***************************************************************************
//
//  EnumDeletedObjects()
//
//  Enumerates all of the objects in the Deleted Objects container.
//
//***************************************************************************

HRESULT EnumDeletedObjects()
{
    HRESULT hr;
    IADsContainer *pDeletedObjectsCont = NULL;
    IDirectorySearch *pSearch = NULL;

    hr = GetDeletedObjectsContainer(&pDeletedObjectsCont);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    hr = pDeletedObjectsCont->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Only search for direct child objects of the container.
    ADS_SEARCHPREF_INFO rgSearchPrefs[3];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_ONELEVEL;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the page size.
    rgSearchPrefs[2].dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
    rgSearchPrefs[2].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[2].vValue.Integer = 1000;

    // Set the search preference
    hr = pSearch->SetSearchPreference(rgSearchPrefs, ARRAYSIZE(rgSearchPrefs));
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    LPWSTR pszSearch = L"(cn=*)";

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search
    hr = pSearch->ExecuteSearch(    pszSearch,
                                    rgAttributes,
                                    ARRAYSIZE(rgAttributes),
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;
                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pDeletedObjectsCont)
    {
        pDeletedObjectsCont->Release();
    }

    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}

```



### <a name="finddeletedobjectbyguid"></a>FindDeletedObjectByGUID

Nell'esempio di codice C++ seguente viene illustrato come trovare un oggetto eliminato specifico dalla proprietà **objectGUID** dell'oggetto.


```C++
HRESULT FindDeletedObjectByGUID(IADs *padsDomain, GUID *pguid)
{
    HRESULT hr;
    IDirectorySearch *pSearch = NULL;
    LPWSTR pwszGuid = NULL;

    hr = padsDomain->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Search the entire tree.
    ADS_SEARCHPREF_INFO rgSearchPrefs[2];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_SUBTREE;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the search preference.
    hr = pSearch->SetSearchPreference(rgSearchPrefs, 2);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    LPWSTR pwszFormat = L"(objectGUID=%s)";

    LPWSTR pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
    if(NULL == pwszSearch)
    {
        goto cleanup;
    }
    
    swprintf_s(pwszSearch, pwszFormat, pwszGuid);
    
    FreeADsMem(pwszGuid);

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search.
    hr = pSearch->ExecuteSearch(    pwszSearch,
                                    rgAttributes,
                                    3,
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data.
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                GUID guid;
                                LPBYTE pb = col.pADsValues[x].OctetString.lpValue;
                                WCHAR wszGUID[MAX_PATH];

                                // Convert the octet string into a GUID.
                                guid.Data1 = *((long*)pb);
                                pb += sizeof(guid.Data1);
                                guid.Data2 = *((short*)pb);
                                pb += sizeof(guid.Data2);
                                guid.Data3 = *((short*)pb);
                                pb += sizeof(guid.Data3);
                                CopyMemory(&guid.Data4, pb, sizeof(guid.Data4));

                                // Convert the GUID into a string.
                                StringFromGUID2(guid, wszGUID, MAX_PATH);
                                wprintf(wszGUID);

                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                                OutputDebugStringW(wszGUID);
                                OutputDebugStringW(L"\n");

                                {
                                    DWORD a;

                                    for(a = 0, *wszGUID = 0; a < col.pADsValues[x].OctetString.dwLength; a++)
                                    {
                                        swprintf_s(wszGUID + lstrlenW(wszGUID), L"%02X", *(LPBYTE)(col.pADsValues[x].OctetString.lpValue + a));
                                    }

                                    OutputDebugStringW(wszGUID);
                                    OutputDebugStringW(L"\n");
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pwszSearch)
    {
        delete pwszSearch;
    }
    
    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}
```



 

 