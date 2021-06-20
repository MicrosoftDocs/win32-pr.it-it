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
# <a name="supporting-device-side-content"></a>Supporto del contenuto sul lato dispositivo

Poiché il contenuto sul lato dispositivo non è accessibile tramite il file system in Windows Vista, è necessario usare l'API Shell di Windows o l'API WPD per recuperare i dati per gli oggetti dispositivo. Questa è la differenza principale tra un normale gestore della finestra delle proprietà e un gestore della finestra delle proprietà WPD. Il codice di esempio seguente illustra il recupero di contenuto sul lato dispositivo usando l'API Shell di Windows.

Il primo passaggio è l'inizializzazione dell'elenco di identificatori di elemento o PIDL. Questo elenco contiene l'identificatore univoco per l'oggetto dispositivo specificato.


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



La funzione di inizializzazione chiama la funzione ExaminePIDLArray, che recupera le proprietà per l'oggetto identificato da \_ un PIDL nella matrice PIDL.


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



Oltre all'inizializzazione e all'elaborazione dell'elenco di identificatori di elemento, l'applicazione dovrà implementare il metodo IShellPropSheetExt::ReplacePage e inserire i gestori di sostituzione appropriati. La shell di Windows chiama questo metodo ogni volta che sta per visualizzare una finestra delle proprietà sostituibile, offrendo all'applicazione la possibilità di richiamare un gestore di sostituzione corrispondente. La parola bassa del primo parametro del metodo ReplacePage è un identificatore per la finestra delle proprietà specificata che Windows sta per visualizzare. I valori passati nella parola bassa del primo parametro corrispondono ai valori definiti nel file WpdShellExtension.h. Questi valori e le relative descrizioni vengono visualizzati nella tabella seguente.



| Valore                                  | Descrizione                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| WPDNSE \_ PROPSHEET \_ DEVICE \_ GENERAL     | Corrisponde alla scheda Generale per il dispositivo.                              |
| WPDNSE \_ PROPSHEET \_ STORAGE \_ GENERAL    | Corrisponde alla scheda Generale per un oggetto di archiviazione presente nel dispositivo.    |
| CONTENUTO PROPSHEET WPDNSE \_ \_ \_ GENERALE    | Corrisponde alla scheda Generale per l'oggetto contenuto presente nel dispositivo.      |
| RIFERIMENTI AL CONTENUTO PROPSHEET WPDNSE \_ \_ \_ | Corrisponde alla scheda riferimenti per un oggetto contenuto trovato nel dispositivo. |
| RISORSE DI CONTENUTO PROPSHEET WPDNSE \_ \_ \_  | Corrisponde alla scheda resources per un oggetto contenuto presente nel dispositivo.  |
| DETTAGLI DEL CONTENUTO DI PROPSHEET WPDNSE \_ \_ \_    | Corrisponde a una scheda dei dettagli per un oggetto contenuto trovato nel dispositivo.      |



 

Nell'estensione della finestra delle proprietà di esempio, il metodo ReplacePage richiama due gestori di sostituzione: \_ ReplaceDeviceGeneral e \_ ReplaceContentReferences. Questi gestori sostituiscono il dispositivo generale e il contenuto fa riferimento alle schede nelle finestre delle proprietà estendibile.


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



Poiché un utente può selezionare più dispositivi, un'applicazione dovrà salvare la matrice PIDL restituita da IShellExtInit::Initialize e quindi esaminare la parola alta del primo parametro in ReplacePage. Il valore zero in questa parola alta corrisponde al primo elemento nella matrice PIDL, un valore pari a uno corrisponde al secondo elemento e così via. Nella funzione ReplacePage dell'applicazione di esempio questo valore di parola alto viene passato a entrambi i gestori di sostituzione. Questi gestori, a loro volta, usano questo valore per identificare un dispositivo specifico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 



