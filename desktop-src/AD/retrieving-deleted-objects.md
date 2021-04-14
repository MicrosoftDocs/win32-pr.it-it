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
# <a name="retrieving-deleted-objects"></a><span data-ttu-id="73f7c-106">Recupero di oggetti eliminati</span><span class="sxs-lookup"><span data-stu-id="73f7c-106">Retrieving Deleted Objects</span></span>

<span data-ttu-id="73f7c-107">Gli oggetti eliminati vengono archiviati nel contenitore degli oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="73f7c-107">Deleted objects are stored in the Deleted Objects container.</span></span> <span data-ttu-id="73f7c-108">Il contenitore degli oggetti eliminati non è in genere visibile, ma il contenitore degli oggetti eliminati può essere associato da un membro del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="73f7c-108">The Deleted Objects container is not normally visible, but the Deleted Objects container can be bound to by a member of the administrators group.</span></span> <span data-ttu-id="73f7c-109">Il contenuto del contenitore degli oggetti eliminati può essere enumerato ed è possibile ottenere singoli attributi dell'oggetto eliminati usando l'interfaccia [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) con la preferenza di ricerca per la **\_ \_ rimozione definitiva ADS SEARCHPREF** .</span><span class="sxs-lookup"><span data-stu-id="73f7c-109">The contents of the Deleted Objects container can be enumerated and individual deleted object attributes can be obtained using the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface with the **ADS\_SEARCHPREF\_TOMBSTONE** search preference.</span></span>

<span data-ttu-id="73f7c-110">Il contenitore degli oggetti eliminati può essere ottenuto mediante l'associazione al **\_ \_ \_ contenitore degli oggetti eliminati** GUID ben noto definito in ntdsapi. h.</span><span class="sxs-lookup"><span data-stu-id="73f7c-110">The Deleted Objects container can be obtained by binding to the well-known GUID **GUID\_DELETED\_OBJECTS\_CONTAINER** defined in Ntdsapi.h.</span></span> <span data-ttu-id="73f7c-111">Per ulteriori informazioni sull'associazione ai GUID noti, vedere [associazione a oggetti di Well-Known con WKGUID](binding-to-well-known-objects-using-wkguid.md).</span><span class="sxs-lookup"><span data-stu-id="73f7c-111">For more information about binding to well-known GUIDs, see [Binding to Well-Known Objects Using WKGUID](binding-to-well-known-objects-using-wkguid.md).</span></span>

<span data-ttu-id="73f7c-112">Specificare l'opzione **Ads \_ Fast \_ Bind** durante l'associazione al contenitore degli oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="73f7c-112">Specify the **ADS\_FAST\_BIND** option when binding to the Deleted Objects container.</span></span> <span data-ttu-id="73f7c-113">Ciò significa che le interfacce ADSI utilizzate per lavorare con un oggetto in Active Directory Domain Services, ad esempio [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), non possono essere utilizzate nel contenitore degli oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="73f7c-113">This means that the ADSI interfaces used to work with an object in Active Directory Domain Services, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on the Deleted Objects container.</span></span> <span data-ttu-id="73f7c-114">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come eseguire l'associazione al contenitore degli oggetti eliminati, vedere la funzione di esempio GetDeletedObjectsContainer riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="73f7c-114">For more information and a code example that shows how to bind to the Deleted Objects container, see the GetDeletedObjectsContainer example function below.</span></span>

-   [<span data-ttu-id="73f7c-115">Enumerazione degli oggetti eliminati</span><span class="sxs-lookup"><span data-stu-id="73f7c-115">Enumerating Deleted Objects</span></span>](#enumerating-deleted-objects)
-   [<span data-ttu-id="73f7c-116">Ricerca di un oggetto eliminato specifico</span><span class="sxs-lookup"><span data-stu-id="73f7c-116">Finding a Specific Deleted Object</span></span>](#finding-a-specific-deleted-object)
    -   [<span data-ttu-id="73f7c-117">GetDeletedObjectsContainer</span><span class="sxs-lookup"><span data-stu-id="73f7c-117">GetDeletedObjectsContainer</span></span>](#getdeletedobjectscontainer)
    -   [<span data-ttu-id="73f7c-118">EnumDeletedObjects</span><span class="sxs-lookup"><span data-stu-id="73f7c-118">EnumDeletedObjects</span></span>](#enumdeletedobjects)
    -   [<span data-ttu-id="73f7c-119">FindDeletedObjectByGUID</span><span class="sxs-lookup"><span data-stu-id="73f7c-119">FindDeletedObjectByGUID</span></span>](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a><span data-ttu-id="73f7c-120">Enumerazione degli oggetti eliminati</span><span class="sxs-lookup"><span data-stu-id="73f7c-120">Enumerating Deleted Objects</span></span>

<span data-ttu-id="73f7c-121">L'interfaccia [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) viene utilizzata per cercare gli oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="73f7c-121">The [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface is used to search for deleted objects.</span></span>

<span data-ttu-id="73f7c-122">**Per enumerare gli oggetti eliminati**</span><span class="sxs-lookup"><span data-stu-id="73f7c-122">**To enumerate deleted objects**</span></span>

1.  <span data-ttu-id="73f7c-123">Ottenere l'interfaccia [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) per il contenitore degli oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="73f7c-123">Obtain the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interface for the Deleted Objects container.</span></span> <span data-ttu-id="73f7c-124">Questa operazione viene eseguita associando al contenitore degli oggetti eliminati e richiedendo l'interfaccia **IDirectorySearch** .</span><span class="sxs-lookup"><span data-stu-id="73f7c-124">This is accomplished by binding to the Deleted Objects container and requesting the **IDirectorySearch** interface.</span></span> <span data-ttu-id="73f7c-125">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come eseguire l'associazione al contenitore degli oggetti eliminati, vedere l'esempio di funzione **GetDeletedObjectsContainer** seguente.</span><span class="sxs-lookup"><span data-stu-id="73f7c-125">For more information and a code example that shows how to bind to the Deleted Objects container, see the following **GetDeletedObjectsContainer** function example.</span></span>
2.  <span data-ttu-id="73f7c-126">Impostare la preferenza di ricerca dell' **\_ ambito di \_ ricerca \_ ADS SEARCHPREF** sull' **\_ ambito Ads \_ unlivello** usando il metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="73f7c-126">Set the **ADS\_SEARCHPREF\_SEARCH\_SCOPE** search preference to **ADS\_SCOPE\_ONELEVEL** using the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="73f7c-127">È anche possibile usare la preferenza per la **\_ \_ sottostruttura ad ambito ADS** , ma il contenitore degli oggetti eliminati è un solo livello, pertanto l'uso del **\_ \_ sottoalbero con ambito ADS** è ridondante.</span><span class="sxs-lookup"><span data-stu-id="73f7c-127">The **ADS\_SCOPE\_SUBTREE** preference can also be used, but the Deleted Objects container is only one level, so using **ADS\_SCOPE\_SUBTREE** is redundant.</span></span>
3.  <span data-ttu-id="73f7c-128">Impostare la preferenza di ricerca per la **\_ \_ rimozione definitiva ADS SEARCHPREF** su **true**.</span><span class="sxs-lookup"><span data-stu-id="73f7c-128">Set the **ADS\_SEARCHPREF\_TOMBSTONE** search preference to **TRUE**.</span></span> <span data-ttu-id="73f7c-129">In questo modo la ricerca include gli oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="73f7c-129">This causes the search to include deleted objects.</span></span>
4.  <span data-ttu-id="73f7c-130">Impostare la preferenza di ricerca **Ads \_ SEARCHPREF \_ pageSize** su un valore minore o uguale a 1000.</span><span class="sxs-lookup"><span data-stu-id="73f7c-130">Set the **ADS\_SEARCHPREF\_PAGESIZE** search preference to a value less than, or equal to, 1000.</span></span> <span data-ttu-id="73f7c-131">Questa operazione è facoltativa, ma se questa operazione non viene eseguita, è possibile recuperare non più di 1000 oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="73f7c-131">This is optional, but if this is not done, no more than 1000 deleted objects can be retrieved.</span></span>
5.  <span data-ttu-id="73f7c-132">Impostare il filtro di ricerca nella chiamata [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) su "(indeleted =**true**)".</span><span class="sxs-lookup"><span data-stu-id="73f7c-132">Set the search filter in the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) call to "(isDeleted=**TRUE**)".</span></span> <span data-ttu-id="73f7c-133">In questo modo la ricerca recupera solo gli oggetti con l'attributo **Andeleted** impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="73f7c-133">This causes the search to only retrieve objects with the **isDeleted** attribute set to **TRUE**.</span></span>

<span data-ttu-id="73f7c-134">Per un codice di esempio di codice che illustra come enumerare gli oggetti eliminati, vedere l'esempio di funzione **EnumDeletedObjects** seguente.</span><span class="sxs-lookup"><span data-stu-id="73f7c-134">For a code example code that shows how to enumerate deleted objects, see the following **EnumDeletedObjects** function example.</span></span>

<span data-ttu-id="73f7c-135">La ricerca può essere ulteriormente perfezionata aggiungendo al filtro di ricerca come illustrato nel [dialetto LDAP](/windows/desktop/ADSI/ldap-dialect).</span><span class="sxs-lookup"><span data-stu-id="73f7c-135">The search can be refined further by adding to the search filter as shown in [LDAP Dialect](/windows/desktop/ADSI/ldap-dialect).</span></span> <span data-ttu-id="73f7c-136">Ad esempio, per cercare tutti gli oggetti eliminati con un nome che inizia con "Jeff", il filtro di ricerca viene impostato su "(& (è stato eliminato =**true**) (CN = Jeff \* ))".</span><span class="sxs-lookup"><span data-stu-id="73f7c-136">For example, to search for all of the deleted objects with a name that begins with "Jeff", the search filter would be set to "(&(isDeleted=**TRUE**)(cn=Jeff\*))".</span></span>

<span data-ttu-id="73f7c-137">Poiché gli oggetti eliminati hanno la maggior parte degli attributi rimossi quando vengono eliminati, non è possibile eseguire l'associazione diretta a un oggetto eliminato.</span><span class="sxs-lookup"><span data-stu-id="73f7c-137">Because deleted objects have most of their attributes removed when they are deleted, it is not possible to bind directly to a deleted object.</span></span> <span data-ttu-id="73f7c-138">È necessario specificare l'opzione **Ads \_ Fast \_ Bind** durante l'associazione a un oggetto eliminato.</span><span class="sxs-lookup"><span data-stu-id="73f7c-138">The **ADS\_FAST\_BIND** option must be specified when binding to a deleted object.</span></span> <span data-ttu-id="73f7c-139">Ciò significa che le interfacce ADSI utilizzate per utilizzare un oggetto Active Directory Domain Services, ad esempio [**IADs**](/windows/desktop/api/iads/nn-iads-iads) e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), non possono essere utilizzate in un contenitore di oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="73f7c-139">This means that the ADSI interfaces used to work with an Active Directory Domain Services object, such as [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist), cannot be used on a deleted object container.</span></span>

## <a name="finding-a-specific-deleted-object"></a><span data-ttu-id="73f7c-140">Ricerca di un oggetto eliminato specifico</span><span class="sxs-lookup"><span data-stu-id="73f7c-140">Finding a Specific Deleted Object</span></span>

<span data-ttu-id="73f7c-141">È anche possibile trovare un oggetto eliminato specifico.</span><span class="sxs-lookup"><span data-stu-id="73f7c-141">It is also possible to find a specific deleted object.</span></span> <span data-ttu-id="73f7c-142">Se il **objectGUID** dell'oggetto è noto, può essere usato per cercare l'oggetto con tale **objectGUID** specifico.</span><span class="sxs-lookup"><span data-stu-id="73f7c-142">If the **objectGUID** of the object is known, it can be used to search for the object with that specific **objectGUID**.</span></span> <span data-ttu-id="73f7c-143">Per ulteriori informazioni e un esempio di codice che illustra come trovare un oggetto eliminato specifico, vedere **FindDeletedObjectByGUID** di seguito.</span><span class="sxs-lookup"><span data-stu-id="73f7c-143">For more information and a code example that shows how to find a specific deleted object, see **FindDeletedObjectByGUID** below.</span></span>

### <a name="getdeletedobjectscontainer"></a><span data-ttu-id="73f7c-144">GetDeletedObjectsContainer</span><span class="sxs-lookup"><span data-stu-id="73f7c-144">GetDeletedObjectsContainer</span></span>

<span data-ttu-id="73f7c-145">Nell'esempio di codice C++ riportato di seguito viene illustrato come eseguire l'associazione al contenitore degli oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="73f7c-145">The following C++ code example shows how to bind to the Deleted Objects container.</span></span>


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



### <a name="enumdeletedobjects"></a><span data-ttu-id="73f7c-146">EnumDeletedObjects</span><span class="sxs-lookup"><span data-stu-id="73f7c-146">EnumDeletedObjects</span></span>

<span data-ttu-id="73f7c-147">Nell'esempio di codice C++ riportato di seguito viene illustrato come enumerare gli oggetti nel contenitore degli oggetti eliminati.</span><span class="sxs-lookup"><span data-stu-id="73f7c-147">The following C++ code example shows how to enumerate the objects in the Deleted Objects container.</span></span>


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



### <a name="finddeletedobjectbyguid"></a><span data-ttu-id="73f7c-148">FindDeletedObjectByGUID</span><span class="sxs-lookup"><span data-stu-id="73f7c-148">FindDeletedObjectByGUID</span></span>

<span data-ttu-id="73f7c-149">Nell'esempio di codice C++ riportato di seguito viene illustrato come trovare un oggetto eliminato specifico dalla proprietà **objectGUID** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="73f7c-149">The following C++ code example shows how to find a specific deleted object from the object's **objectGUID** property.</span></span>


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



 

 