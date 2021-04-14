---
title: Recupero di oggetti eliminati
description: Gli oggetti eliminati vengono archiviati nel contenitore degli oggetti eliminati.
ms.assetid: dc9a6466-204b-4a78-b0f3-9c03c13a374b
ms.tgt_platform: multiple
keywords:
- Recupero di oggetti eliminati AD
- oggetto AD, recupero di oggetti eliminati
- Active Directory, utilizzo, recupero di oggetti eliminati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b2062c747e38bc0b3a9b1b793a102006c11512
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472494"
---
# <a name="retrieving-deleted-objects"></a>Recupero di oggetti eliminati

Gli oggetti eliminati vengono archiviati nel contenitore degli oggetti eliminati. Il contenitore degli oggetti eliminati non è in genere visibile, ma il contenitore degli oggetti eliminati può essere associato da un membro del gruppo Administrators. Il contenuto del contenitore degli oggetti eliminati può essere enumerato ed è possibile ottenere singoli attributi dell'oggetto eliminati usando l'interfaccia [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) con la preferenza di ricerca per la **\_ \_ rimozione definitiva ADS SEARCHPREF** .

Il contenitore degli oggetti eliminati può essere ottenuto mediante l'associazione al **\_ \_ \_ contenitore degli oggetti eliminati** GUID ben noto definito in ntdsapi. h. Per ulteriori informazioni sull'associazione ai GUID noti, vedere [associazione a oggetti di Well-Known con WKGUID](binding-to-well-known-objects-using-wkguid.md).

Specificare l'opzione **Ads \_ Fast \_ Bind** durante l'associazione al contenitore degli oggetti eliminati. Ciò significa che le interfacce ADSI utilizzate per lavorare con un oggetto in Active Directory Domain Services, ad esempio [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), non possono essere utilizzate nel contenitore degli oggetti eliminati. Per ulteriori informazioni e un esempio di codice in cui viene illustrato come eseguire l'associazione al contenitore degli oggetti eliminati, vedere la funzione di esempio GetDeletedObjectsContainer riportata di seguito.

-   [Enumerazione degli oggetti eliminati](#enumerating-deleted-objects)
-   [Ricerca di un oggetto eliminato specifico](#finding-a-specific-deleted-object)
    -   [GetDeletedObjectsContainer](#getdeletedobjectscontainer)
    -   [EnumDeletedObjects](#enumdeletedobjects)
    -   [FindDeletedObjectByGUID](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a>Enumerazione degli oggetti eliminati

L'interfaccia [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) viene utilizzata per cercare gli oggetti eliminati.

**Per enumerare gli oggetti eliminati**

1.  Ottenere l'interfaccia [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) per il contenitore degli oggetti eliminati. Questa operazione viene eseguita associando al contenitore degli oggetti eliminati e richiedendo l'interfaccia **IDirectorySearch** . Per ulteriori informazioni e un esempio di codice in cui viene illustrato come eseguire l'associazione al contenitore degli oggetti eliminati, vedere l'esempio di funzione **GetDeletedObjectsContainer** seguente.
2.  Impostare la preferenza di ricerca dell' **\_ ambito di \_ ricerca \_ ADS SEARCHPREF** sull' **\_ ambito Ads \_ unlivello** usando il metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) . È anche possibile usare la preferenza per la **\_ \_ sottostruttura ad ambito ADS** , ma il contenitore degli oggetti eliminati è un solo livello, pertanto l'uso del **\_ \_ sottoalbero con ambito ADS** è ridondante.
3.  Impostare la preferenza di ricerca per la **\_ \_ rimozione definitiva ADS SEARCHPREF** su **true**. In questo modo la ricerca include gli oggetti eliminati.
4.  Impostare la preferenza di ricerca **Ads \_ SEARCHPREF \_ pageSize** su un valore minore o uguale a 1000. Questa operazione è facoltativa, ma se questa operazione non viene eseguita, è possibile recuperare non più di 1000 oggetti eliminati.
5.  Impostare il filtro di ricerca nella chiamata [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) su "(indeleted =**true**)". In questo modo la ricerca recupera solo gli oggetti con l'attributo **Andeleted** impostato su **true**.

Per un codice di esempio di codice che illustra come enumerare gli oggetti eliminati, vedere l'esempio di funzione **EnumDeletedObjects** seguente.

La ricerca può essere ulteriormente perfezionata aggiungendo al filtro di ricerca come illustrato nel [dialetto LDAP](/windows/desktop/ADSI/ldap-dialect). Ad esempio, per cercare tutti gli oggetti eliminati con un nome che inizia con "Jeff", il filtro di ricerca viene impostato su "(& (è stato eliminato =**true**) (CN = Jeff \* ))".

Poiché gli oggetti eliminati hanno la maggior parte degli attributi rimossi quando vengono eliminati, non è possibile eseguire l'associazione diretta a un oggetto eliminato. È necessario specificare l'opzione **Ads \_ Fast \_ Bind** durante l'associazione a un oggetto eliminato. Ciò significa che le interfacce ADSI utilizzate per utilizzare un oggetto Active Directory Domain Services, ad esempio [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), non possono essere utilizzate in un contenitore di oggetti eliminati.

## <a name="finding-a-specific-deleted-object"></a>Ricerca di un oggetto eliminato specifico

È anche possibile trovare un oggetto eliminato specifico. Se il **objectGUID** dell'oggetto è noto, può essere usato per cercare l'oggetto con tale **objectGUID** specifico. Per ulteriori informazioni e un esempio di codice che illustra come trovare un oggetto eliminato specifico, vedere **FindDeletedObjectByGUID** di seguito.

### <a name="getdeletedobjectscontainer"></a>GetDeletedObjectsContainer

Nell'esempio di codice C++ riportato di seguito viene illustrato come eseguire l'associazione al contenitore degli oggetti eliminati.


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

Nell'esempio di codice C++ riportato di seguito viene illustrato come enumerare gli oggetti nel contenitore degli oggetti eliminati.


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

Nell'esempio di codice C++ riportato di seguito viene illustrato come trovare un oggetto eliminato specifico dalla proprietà **objectGUID** dell'oggetto.


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



 

 