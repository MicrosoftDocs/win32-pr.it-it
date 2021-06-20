---
title: Supporto del contenuto sul lato dispositivo WPD (ContextMenu)
description: Informazioni su come usare l'API della shell di Windows o l'API WPD per ottenere i dati per gli oggetti dispositivo WPD, che non sono accessibili tramite il file system in Windows Vista.
ms.assetid: 47fb7f49-9026-43c1-be46-8a520c048862
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626c92633b1aa215c0e826a4b720de0375aa6048
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404284"
---
# <a name="supporting-wpd-device-side-content"></a><span data-ttu-id="d8c8e-103">Supporto del contenuto sul lato dispositivo WPD</span><span class="sxs-lookup"><span data-stu-id="d8c8e-103">Supporting WPD device-side content</span></span>

<span data-ttu-id="d8c8e-104">Poiché il contenuto sul lato dispositivo non è accessibile tramite il file system in Windows Vista, dovrai usare l'API shell di Windows o l'API WPD per recuperare i dati per gli oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8c8e-104">Because device-side content is not accessible through the file system in Windows Vista, you'll need to use either the Windows Shell API or the WPD API to retrieve data for device objects.</span></span> <span data-ttu-id="d8c8e-105">Questa è la differenza principale tra un gestore di menu di scelta rapida normale e un gestore del menu di scelta rapida WPD.</span><span class="sxs-lookup"><span data-stu-id="d8c8e-105">This is the primary difference between a normal context menu handler and a WPD context menu handler.</span></span> <span data-ttu-id="d8c8e-106">Il codice di esempio seguente illustra il recupero del contenuto sul lato dispositivo usando l'API della shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="d8c8e-106">The following sample code demonstrates the retrieval of device-side content using the Windows Shell API.</span></span>

<span data-ttu-id="d8c8e-107">Il primo passaggio è l'inizializzazione dell'elenco di identificatori di elemento o PIDL.</span><span class="sxs-lookup"><span data-stu-id="d8c8e-107">The first step is the initialization of the item identifier list or PIDL.</span></span> <span data-ttu-id="d8c8e-108">Questo elenco contiene l'identificatore univoco per l'oggetto dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="d8c8e-108">(This list contains the unique identifier for the given device object.)</span></span>


```C++
HRESULT CWPDContextMenu::_InitializePIDLArray(IDataObject *pDataObj)
{
    if (m_cfHIDA == 0)
    {
        m_cfHIDA = (CLIPFORMAT)RegisterClipboardFormat(CFSTR_SHELLIDLIST);
    }

    STGMEDIUM   medium;
    FORMATETC   fmte = {m_cfHIDA, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};

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
                m_pida = pida;
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



<span data-ttu-id="d8c8e-109">La funzione di inizializzazione chiama la funzione ExaminePIDLArray, che recupera le proprietà per l'oggetto identificato da \_ un PIDL nella matrice PIDL.</span><span class="sxs-lookup"><span data-stu-id="d8c8e-109">The initialization function calls the \_ExaminePIDLArray function, which retrieves the properties for object identified by a PIDL in the PIDL array.</span></span>


```C++
HRESULT CWPDContextMenu::_ExaminePIDLArray()
{
    CComPtr<IShellFolder2> spParentFolder;

    CComVariant  variant;

    LPITEMIDLIST pidl = NULL;
    HRESULT      hr = S_OK;
    UINT         index = 0;

    pidl = GetPIDL(m_pida, index);
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

        pidl = GetPIDL(m_pida, ++index);
    } while (pidl != NULL && index < m_pida->cidl);

Exit:
    UI_SAFE_ILFREE(pidl);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d8c8e-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8c8e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8c8e-111">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="d8c8e-111">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



