---
title: Supporto del contenuto sul lato dispositivo (PropertySheet)
description: Informazioni su come usare l'API Shell di Windows o l'API WPD per ottenere dati per gli oggetti dispositivo, che non sono accessibili tramite l'api file system in Windows Vista.
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aeade3745c37296b334c54af9edcc768fb8c93e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404194"
---
# <a name="supporting-device-side-content"></a><span data-ttu-id="fa59a-103">Supporto del contenuto sul lato dispositivo</span><span class="sxs-lookup"><span data-stu-id="fa59a-103">Supporting device-side content</span></span>

<span data-ttu-id="fa59a-104">Poiché il contenuto sul lato dispositivo non è accessibile tramite il file system in Windows Vista, è necessario usare l'API Shell di Windows o l'API WPD per recuperare i dati per gli oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa59a-104">Because device-side content is not accessible through the file system in Windows Vista, you'll need to use either the Windows Shell API or the WPD API to retrieve data for device objects.</span></span> <span data-ttu-id="fa59a-105">Questa è la differenza principale tra un normale gestore della finestra delle proprietà e un gestore della finestra delle proprietà WPD.</span><span class="sxs-lookup"><span data-stu-id="fa59a-105">This is the primary difference between a normal property sheet handler and a WPD property sheet handler.</span></span> <span data-ttu-id="fa59a-106">Il codice di esempio seguente illustra il recupero di contenuto sul lato dispositivo usando l'API Shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="fa59a-106">The following sample code demonstrates the retrieval of device-side content using the Windows Shell API.</span></span>

<span data-ttu-id="fa59a-107">Il primo passaggio è l'inizializzazione dell'elenco di identificatori di elemento o PIDL.</span><span class="sxs-lookup"><span data-stu-id="fa59a-107">The first step is the initialization of the item identifier list or PIDL.</span></span> <span data-ttu-id="fa59a-108">Questo elenco contiene l'identificatore univoco per l'oggetto dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="fa59a-108">(This list contains the unique identifier for the given device object.)</span></span>


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



<span data-ttu-id="fa59a-109">La funzione di inizializzazione chiama la funzione ExaminePIDLArray, che recupera le proprietà per l'oggetto identificato da \_ un PIDL nella matrice PIDL.</span><span class="sxs-lookup"><span data-stu-id="fa59a-109">The initialization function calls the \_ExaminePIDLArray function, which retrieves the properties for object identified by a PIDL in the PIDL array.</span></span>


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



<span data-ttu-id="fa59a-110">Oltre all'inizializzazione e all'elaborazione dell'elenco di identificatori di elemento, l'applicazione dovrà implementare il metodo IShellPropSheetExt::ReplacePage e inserire i gestori di sostituzione appropriati.</span><span class="sxs-lookup"><span data-stu-id="fa59a-110">In addition to the initialization and processing of the item identifier list, your application will need to implement the IShellPropSheetExt::ReplacePage method and insert the appropriate replacement handlers.</span></span> <span data-ttu-id="fa59a-111">La shell di Windows chiama questo metodo ogni volta che sta per visualizzare una finestra delle proprietà sostituibile, offrendo all'applicazione la possibilità di richiamare un gestore di sostituzione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="fa59a-111">The Windows Shell calls this method each time it is about to display a replaceable property sheet, giving your application a chance to invoke a corresponding replacement handler.</span></span> <span data-ttu-id="fa59a-112">La parola bassa del primo parametro del metodo ReplacePage è un identificatore per la finestra delle proprietà specificata che Windows sta per visualizzare.</span><span class="sxs-lookup"><span data-stu-id="fa59a-112">The low word of the first parameter to the ReplacePage method is an identifier for the given property sheet that Windows is about to display.</span></span> <span data-ttu-id="fa59a-113">I valori passati nella parola bassa del primo parametro corrispondono ai valori definiti nel file WpdShellExtension.h.</span><span class="sxs-lookup"><span data-stu-id="fa59a-113">The values passed in the low word of the first parameter correspond to values defined in the file WpdShellExtension.h.</span></span> <span data-ttu-id="fa59a-114">Questi valori e le relative descrizioni vengono visualizzati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fa59a-114">These values and their descriptions appear in the following table.</span></span>



| <span data-ttu-id="fa59a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fa59a-115">Value</span></span>                                  | <span data-ttu-id="fa59a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa59a-116">Description</span></span>                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="fa59a-117">WPDNSE \_ PROPSHEET \_ DEVICE \_ GENERAL</span><span class="sxs-lookup"><span data-stu-id="fa59a-117">WPDNSE\_PROPSHEET\_DEVICE\_GENERAL</span></span>     | <span data-ttu-id="fa59a-118">Corrisponde alla scheda Generale per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa59a-118">Corresponds to the general tab for the device.</span></span>                              |
| <span data-ttu-id="fa59a-119">WPDNSE \_ PROPSHEET \_ STORAGE \_ GENERAL</span><span class="sxs-lookup"><span data-stu-id="fa59a-119">WPDNSE\_PROPSHEET\_STORAGE\_GENERAL</span></span>    | <span data-ttu-id="fa59a-120">Corrisponde alla scheda Generale per un oggetto di archiviazione presente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa59a-120">Corresponds to the general tab for a storage object found on the device.</span></span>    |
| <span data-ttu-id="fa59a-121">CONTENUTO PROPSHEET WPDNSE \_ \_ \_ GENERALE</span><span class="sxs-lookup"><span data-stu-id="fa59a-121">WPDNSE\_PROPSHEET\_CONTENT\_GENERAL</span></span>    | <span data-ttu-id="fa59a-122">Corrisponde alla scheda Generale per l'oggetto contenuto presente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa59a-122">Corresponds to the general tab for content object found on the device.</span></span>      |
| <span data-ttu-id="fa59a-123">RIFERIMENTI AL CONTENUTO PROPSHEET WPDNSE \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fa59a-123">WPDNSE\_PROPSHEET\_CONTENT\_REFERENCES</span></span> | <span data-ttu-id="fa59a-124">Corrisponde alla scheda riferimenti per un oggetto contenuto trovato nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa59a-124">Corresponds to the references tab for a content object found on the device.</span></span> |
| <span data-ttu-id="fa59a-125">RISORSE DI CONTENUTO PROPSHEET WPDNSE \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fa59a-125">WPDNSE\_PROPSHEET\_CONTENT\_RESOURCES</span></span>  | <span data-ttu-id="fa59a-126">Corrisponde alla scheda resources per un oggetto contenuto presente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa59a-126">Corresponds to the resources tab for a content object found on the device.</span></span>  |
| <span data-ttu-id="fa59a-127">DETTAGLI DEL CONTENUTO DI PROPSHEET WPDNSE \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fa59a-127">WPDNSE\_PROPSHEET\_CONTENT\_DETAILS</span></span>    | <span data-ttu-id="fa59a-128">Corrisponde a una scheda dei dettagli per un oggetto contenuto trovato nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa59a-128">Corresponds to a details tab for a content object found on the device.</span></span>      |



 

<span data-ttu-id="fa59a-129">Nell'estensione della finestra delle proprietà di esempio, il metodo ReplacePage richiama due gestori di sostituzione: \_ ReplaceDeviceGeneral e \_ ReplaceContentReferences.</span><span class="sxs-lookup"><span data-stu-id="fa59a-129">In the sample property sheet extension, the ReplacePage method invokes two replacement handlers: \_ReplaceDeviceGeneral and \_ReplaceContentReferences.</span></span> <span data-ttu-id="fa59a-130">Questi gestori sostituiscono il dispositivo generale e il contenuto fa riferimento alle schede nelle finestre delle proprietà estendibile.</span><span class="sxs-lookup"><span data-stu-id="fa59a-130">These handlers replace the general device and the content references tabs in the extensible property sheets.</span></span>


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



<span data-ttu-id="fa59a-131">Poiché un utente può selezionare più dispositivi, un'applicazione dovrà salvare la matrice PIDL restituita da IShellExtInit::Initialize e quindi esaminare la parola alta del primo parametro in ReplacePage.</span><span class="sxs-lookup"><span data-stu-id="fa59a-131">Because it is possible for a user to select multiple devices, an application will need to save the PIDL array returned by IShellExtInit::Initialize and then examine the high word of the first parameter to ReplacePage.</span></span> <span data-ttu-id="fa59a-132">Il valore zero in questa parola alta corrisponde al primo elemento nella matrice PIDL, un valore pari a uno corrisponde al secondo elemento e così via.</span><span class="sxs-lookup"><span data-stu-id="fa59a-132">A value of zero in this high word corresponds to the first element in the PIDL array, a value of one corresponds to the second element, and so on.</span></span> <span data-ttu-id="fa59a-133">Nella funzione ReplacePage dell'applicazione di esempio questo valore di parola alto viene passato a entrambi i gestori di sostituzione.</span><span class="sxs-lookup"><span data-stu-id="fa59a-133">In the sample application's ReplacePage function, this high word value is passed to both replacement handlers.</span></span> <span data-ttu-id="fa59a-134">Questi gestori, a loro volta, usano questo valore per identificare un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="fa59a-134">These handlers, in turn, use this value to identify a particular device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa59a-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa59a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa59a-136">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="fa59a-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



