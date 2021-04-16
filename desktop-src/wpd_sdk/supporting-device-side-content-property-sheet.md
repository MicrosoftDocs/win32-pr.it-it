---
title: Supporto del contenuto lato dispositivo (PropertySheet)
description: Supporto di Device-Side contenuto
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7e054e4c545acd8f34583da5cd9ef3af347643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347416"
---
# <a name="supporting-device-side-content"></a><span data-ttu-id="e7aef-103">Supporto del contenuto lato dispositivo</span><span class="sxs-lookup"><span data-stu-id="e7aef-103">Supporting device-side content</span></span>

<span data-ttu-id="e7aef-104">Poiché il contenuto lato dispositivo non è accessibile tramite il file system in Windows Vista, è necessario usare l'API shell di Windows o l'API WPD per recuperare i dati per gli oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7aef-104">Because device-side content is not accessible through the file system in Windows Vista, you'll need to use either the Windows Shell API or the WPD API to retrieve data for device objects.</span></span> <span data-ttu-id="e7aef-105">Questa è la differenza principale tra un normale gestore della finestra delle proprietà e un gestore della finestra delle proprietà WPD.</span><span class="sxs-lookup"><span data-stu-id="e7aef-105">This is the primary difference between a normal property sheet handler and a WPD property sheet handler.</span></span> <span data-ttu-id="e7aef-106">Il codice di esempio seguente illustra il recupero del contenuto sul lato dispositivo tramite l'API shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="e7aef-106">The following sample code demonstrates the retrieval of device-side content using the Windows Shell API.</span></span>

<span data-ttu-id="e7aef-107">Il primo passaggio è l'inizializzazione dell'elenco di identificatori di elemento o di PIDL.</span><span class="sxs-lookup"><span data-stu-id="e7aef-107">The first step is the initialization of the item identifier list or PIDL.</span></span> <span data-ttu-id="e7aef-108">(Questo elenco contiene l'identificatore univoco per l'oggetto dispositivo specificato).</span><span class="sxs-lookup"><span data-stu-id="e7aef-108">(This list contains the unique identifier for the given device object.)</span></span>


```C++
HRESULT CWPDPropSheet::_InitializePIDLArray(IDataObject *pDataObj)
{
    if (m_cfHIDA == 0)
    {
        m_cfHIDA = (CLIPFORMAT)RegisterClipboardFormat(CFSTR_SHELLIDLIST);
    }

    STGMEDIUM   medium;
    FORMATETC   fmte = {m_cfHIDA, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};

    m_pPropInfo = (PROPINFO*)LocalAlloc(LPTR, sizeof(PROPINFO));
    if (m_pPropInfo == NULL)
        return E_OUTOFMEMORY;

    AddRef_PropInfo(m_pPropInfo);

    HRESULT hr = pDataObj->GetData(&fmte, &medium);
    if (SUCCEEDED(hr))
    {
        SIZE_T cb = GlobalSize(medium.hGlobal);
        CIDA *pida = (CIDA*)GlobalAlloc(GPTR, cb);
        if (pida)
        {
            void *pv = GlobalLock(medium.hGlobal);
            if (pv != NULL)
            {
                CopyMemory(pida, pv, cb);
                GlobalUnlock(medium.hGlobal);
                m_pPropInfo->pida = pida;
                _ExaminePIDLArray();
            }
            else
            {
                hr = E_UNEXPECTED;
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
        ReleaseStgMedium(&medium);
    }

    return hr;
}
```



<span data-ttu-id="e7aef-109">La funzione di inizializzazione chiama la \_ funzione ExaminePIDLArray, che recupera le proprietà per l'oggetto identificato da un PIDL nella matrice PIDL.</span><span class="sxs-lookup"><span data-stu-id="e7aef-109">The initialization function calls the \_ExaminePIDLArray function, which retrieves the properties for object identified by a PIDL in the PIDL array.</span></span>


```C++
HRESULT CWPDPropSheet::_ExaminePIDLArray()
{
    CComPtr<IShellFolder2> spParentFolder;

    CComVariant  variant;

    LPITEMIDLIST pidl = NULL;
    HRESULT      hr = S_OK;
    UINT         index = 0;

    pidl = GetPIDL(m_pPropInfo->pida, index);
    if (pidl)
    {
        hr = SHBindToParent(pidl, IID_PPV_ARGS(&spParentFolder), NULL);
        IF_FAILED_JUMP(hr, Exit);
    }

    do
    {
        CComPtr<IPropertySetStorage> spSetStorage;
        CComPtr<IPropertyStorage>    spPropStorage;

        // Get the IpropertySetStorage interface for this PIDL. This method could also
        // be used to retrieve an IPortableDevice interface to allow more low-level interaction
        // with the WPD API.
        hr = spParentFolder->BindToObject(ILFindLastID(pidl), NULL, IID_PPV_ARGS(&spSetStorage));
        if (SUCCEEDED(hr))
        {
            hr = spSetStorage->Open(WPD_FUNCTIONAL_OBJECT_PROPERTIES_V1, STGM_READ, &spPropStorage);
            if (SUCCEEDED(hr))
            {
                PROPVARIANT PropVar = {0};
                PROPSPEC    PropSpec = {0};

                PropSpec.ulKind = PRSPEC_PROPID;
                PropSpec.propid = 2; // WPD_FUNCTIONAL_OBJECT_CATEGORY

                PropVariantInit(&PropVar);

                hr = spPropStorage->ReadMultiple(1, &PropSpec, &PropVar);
                if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                {
                    // The PIDL array contains a non-file object.
                    // This means we don't want to take over the
                    // default menu action.
                    m_bPIDAContainsOnlyFiles = FALSE;
                    PropVariantClear(&PropVar);
                    break;
                }
                else
                {
                    CComPtr<IPropertyStorage>    spObjectProperties;
                    hr = spSetStorage->Open(WPD_OBJECT_PROPERTIES_V1, STGM_READ, &spObjectProperties);
                    if (SUCCEEDED(hr))
                    {
                        PropSpec.ulKind = PRSPEC_PROPID;
                        PropSpec.propid = 7; // WPD_OBJECT_CONTENT_TYPE
                        
                        PropVariantClear(&PropVar);
                        hr = spObjectProperties->ReadMultiple(1, &PropSpec, &PropVar);
                        if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                        {
                            if (IsEqualGUID(*PropVar.puuid, WPD_CONTENT_TYPE_FOLDER))
                            {
                                // The PIDL array contains a folder object.
                                // This means we don't want to take over the
                                // default menu action.
                                m_bPIDAContainsOnlyFiles = FALSE;
                                PropVariantClear(&PropVar);
                                break;
                            }
                        }
                    }
                }

                PropVariantClear(&PropVar);
            }
        }

        UI_SAFE_ILFREE(pidl);

        pidl = GetPIDL(m_pPropInfo->pida, ++index);
    } while (pidl != NULL && index < m_pPropInfo->pida->cidl);

Exit:
    UI_SAFE_ILFREE(pidl);
    return hr;
}
```



<span data-ttu-id="e7aef-110">Oltre all'inizializzazione e all'elaborazione dell'elenco degli identificatori di elemento, l'applicazione dovrà implementare il metodo IShellPropSheetExt:: ReplacePage e inserire i gestori di sostituzione appropriati.</span><span class="sxs-lookup"><span data-stu-id="e7aef-110">In addition to the initialization and processing of the item identifier list, your application will need to implement the IShellPropSheetExt::ReplacePage method and insert the appropriate replacement handlers.</span></span> <span data-ttu-id="e7aef-111">La shell di Windows chiama questo metodo ogni volta che sta per visualizzare una finestra delle proprietà sostituibile, permettendo all'applicazione di richiamare un gestore di sostituzione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e7aef-111">The Windows Shell calls this method each time it is about to display a replaceable property sheet, giving your application a chance to invoke a corresponding replacement handler.</span></span> <span data-ttu-id="e7aef-112">La parola bassa del primo parametro per il metodo ReplacePage è un identificatore della finestra delle proprietà specificata che Windows sta per visualizzare.</span><span class="sxs-lookup"><span data-stu-id="e7aef-112">The low word of the first parameter to the ReplacePage method is an identifier for the given property sheet that Windows is about to display.</span></span> <span data-ttu-id="e7aef-113">I valori passati nella parola bassa del primo parametro corrispondono ai valori definiti nel file WpdShellExtension. h.</span><span class="sxs-lookup"><span data-stu-id="e7aef-113">The values passed in the low word of the first parameter correspond to values defined in the file WpdShellExtension.h.</span></span> <span data-ttu-id="e7aef-114">Questi valori e le relative descrizioni vengono visualizzati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e7aef-114">These values and their descriptions appear in the following table.</span></span>



| <span data-ttu-id="e7aef-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e7aef-115">Value</span></span>                                  | <span data-ttu-id="e7aef-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7aef-116">Description</span></span>                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="e7aef-117">WPDNSE \_ PROPSHEET \_ dispositivo \_ generale</span><span class="sxs-lookup"><span data-stu-id="e7aef-117">WPDNSE\_PROPSHEET\_DEVICE\_GENERAL</span></span>     | <span data-ttu-id="e7aef-118">Corrisponde alla scheda generale del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7aef-118">Corresponds to the general tab for the device.</span></span>                              |
| <span data-ttu-id="e7aef-119">WPDNSE \_ PROPSHEET \_ storage \_ generale</span><span class="sxs-lookup"><span data-stu-id="e7aef-119">WPDNSE\_PROPSHEET\_STORAGE\_GENERAL</span></span>    | <span data-ttu-id="e7aef-120">Corrisponde alla scheda generale per un oggetto di archiviazione trovato nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7aef-120">Corresponds to the general tab for a storage object found on the device.</span></span>    |
| <span data-ttu-id="e7aef-121">WPDNSE \_ PROPSHEET \_ contenuto \_ generale</span><span class="sxs-lookup"><span data-stu-id="e7aef-121">WPDNSE\_PROPSHEET\_CONTENT\_GENERAL</span></span>    | <span data-ttu-id="e7aef-122">Corrisponde alla scheda generale per l'oggetto contenuto trovato nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7aef-122">Corresponds to the general tab for content object found on the device.</span></span>      |
| <span data-ttu-id="e7aef-123">\_riferimenti al \_ contenuto \_ PROPSHEET di WPDNSE</span><span class="sxs-lookup"><span data-stu-id="e7aef-123">WPDNSE\_PROPSHEET\_CONTENT\_REFERENCES</span></span> | <span data-ttu-id="e7aef-124">Corrisponde alla scheda riferimenti per un oggetto contenuto trovato nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7aef-124">Corresponds to the references tab for a content object found on the device.</span></span> |
| <span data-ttu-id="e7aef-125">\_risorse di \_ contenuto \_ PROPSHEET di WPDNSE</span><span class="sxs-lookup"><span data-stu-id="e7aef-125">WPDNSE\_PROPSHEET\_CONTENT\_RESOURCES</span></span>  | <span data-ttu-id="e7aef-126">Corrisponde alla scheda risorse per un oggetto contenuto trovato nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7aef-126">Corresponds to the resources tab for a content object found on the device.</span></span>  |
| <span data-ttu-id="e7aef-127">dettagli del contenuto di WPDNSE \_ PROPSHEET \_ \_</span><span class="sxs-lookup"><span data-stu-id="e7aef-127">WPDNSE\_PROPSHEET\_CONTENT\_DETAILS</span></span>    | <span data-ttu-id="e7aef-128">Corrisponde a una scheda Dettagli per un oggetto contenuto trovato nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7aef-128">Corresponds to a details tab for a content object found on the device.</span></span>      |



 

<span data-ttu-id="e7aef-129">Nell'estensione della finestra delle proprietà di esempio, il metodo ReplacePage richiama due gestori di sostituzione: \_ ReplaceDeviceGeneral e \_ ReplaceContentReferences.</span><span class="sxs-lookup"><span data-stu-id="e7aef-129">In the sample property sheet extension, the ReplacePage method invokes two replacement handlers: \_ReplaceDeviceGeneral and \_ReplaceContentReferences.</span></span> <span data-ttu-id="e7aef-130">Questi gestori sostituiscono le schede Generale del dispositivo e riferimenti al contenuto nelle finestre delle proprietà estendibili.</span><span class="sxs-lookup"><span data-stu-id="e7aef-130">These handlers replace the general device and the content references tabs in the extensible property sheets.</span></span>


```C++
STDMETHODIMP CWPDPropSheet::ReplacePage(UINT uPageID, LPFNADDPROPSHEETPAGE lpfnReplacePage, LPARAM lParam)
{
    HRESULT       hr = S_OK;

    if (LOWORD(uPageID) == WPDNSE_PROPSHEET_DEVICE_GENERAL)
    {
        hr = _ReplaceDeviceGeneral(HIWORD(uPageID), lpfnReplacePage, lParam);
    }
    else if (LOWORD(uPageID) == WPDNSE_PROPSHEET_CONTENT_REFERENCES)
    {
        hr = _ReplaceContentReferences(HIWORD(uPageID), lpfnReplacePage, lParam);
    }

    return hr;
}
```



<span data-ttu-id="e7aef-131">Poiché è possibile che un utente selezioni più dispositivi, un'applicazione dovrà salvare la matrice PIDL restituita da IShellExtInit:: Initialize, quindi esaminare la parola alta del primo parametro su ReplacePage.</span><span class="sxs-lookup"><span data-stu-id="e7aef-131">Because it is possible for a user to select multiple devices, an application will need to save the PIDL array returned by IShellExtInit::Initialize and then examine the high word of the first parameter to ReplacePage.</span></span> <span data-ttu-id="e7aef-132">Un valore pari a zero in questa parola alta corrisponde al primo elemento nella matrice PIDL, un valore di uno corrisponde al secondo elemento e così via.</span><span class="sxs-lookup"><span data-stu-id="e7aef-132">A value of zero in this high word corresponds to the first element in the PIDL array, a value of one corresponds to the second element, and so on.</span></span> <span data-ttu-id="e7aef-133">Nella funzione ReplacePage dell'applicazione di esempio, questo valore di parola alta viene passato a entrambi i gestori di sostituzione.</span><span class="sxs-lookup"><span data-stu-id="e7aef-133">In the sample application's ReplacePage function, this high word value is passed to both replacement handlers.</span></span> <span data-ttu-id="e7aef-134">Questi gestori, a loro volta, usano questo valore per identificare un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="e7aef-134">These handlers, in turn, use this value to identify a particular device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7aef-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7aef-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7aef-136">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="e7aef-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



