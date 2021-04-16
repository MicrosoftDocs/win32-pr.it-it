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
# <a name="supporting-device-side-content"></a>Supporto del contenuto lato dispositivo

Poiché il contenuto lato dispositivo non è accessibile tramite il file system in Windows Vista, è necessario usare l'API shell di Windows o l'API WPD per recuperare i dati per gli oggetti dispositivo. Questa è la differenza principale tra un normale gestore della finestra delle proprietà e un gestore della finestra delle proprietà WPD. Il codice di esempio seguente illustra il recupero del contenuto sul lato dispositivo tramite l'API shell di Windows.

Il primo passaggio è l'inizializzazione dell'elenco di identificatori di elemento o di PIDL. (Questo elenco contiene l'identificatore univoco per l'oggetto dispositivo specificato).


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



La funzione di inizializzazione chiama la \_ funzione ExaminePIDLArray, che recupera le proprietà per l'oggetto identificato da un PIDL nella matrice PIDL.


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



Oltre all'inizializzazione e all'elaborazione dell'elenco degli identificatori di elemento, l'applicazione dovrà implementare il metodo IShellPropSheetExt:: ReplacePage e inserire i gestori di sostituzione appropriati. La shell di Windows chiama questo metodo ogni volta che sta per visualizzare una finestra delle proprietà sostituibile, permettendo all'applicazione di richiamare un gestore di sostituzione corrispondente. La parola bassa del primo parametro per il metodo ReplacePage è un identificatore della finestra delle proprietà specificata che Windows sta per visualizzare. I valori passati nella parola bassa del primo parametro corrispondono ai valori definiti nel file WpdShellExtension. h. Questi valori e le relative descrizioni vengono visualizzati nella tabella seguente.



| Valore                                  | Descrizione                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| WPDNSE \_ PROPSHEET \_ dispositivo \_ generale     | Corrisponde alla scheda generale del dispositivo.                              |
| WPDNSE \_ PROPSHEET \_ storage \_ generale    | Corrisponde alla scheda generale per un oggetto di archiviazione trovato nel dispositivo.    |
| WPDNSE \_ PROPSHEET \_ contenuto \_ generale    | Corrisponde alla scheda generale per l'oggetto contenuto trovato nel dispositivo.      |
| \_riferimenti al \_ contenuto \_ PROPSHEET di WPDNSE | Corrisponde alla scheda riferimenti per un oggetto contenuto trovato nel dispositivo. |
| \_risorse di \_ contenuto \_ PROPSHEET di WPDNSE  | Corrisponde alla scheda risorse per un oggetto contenuto trovato nel dispositivo.  |
| dettagli del contenuto di WPDNSE \_ PROPSHEET \_ \_    | Corrisponde a una scheda Dettagli per un oggetto contenuto trovato nel dispositivo.      |



 

Nell'estensione della finestra delle proprietà di esempio, il metodo ReplacePage richiama due gestori di sostituzione: \_ ReplaceDeviceGeneral e \_ ReplaceContentReferences. Questi gestori sostituiscono le schede Generale del dispositivo e riferimenti al contenuto nelle finestre delle proprietà estendibili.


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



Poiché è possibile che un utente selezioni più dispositivi, un'applicazione dovrà salvare la matrice PIDL restituita da IShellExtInit:: Initialize, quindi esaminare la parola alta del primo parametro su ReplacePage. Un valore pari a zero in questa parola alta corrisponde al primo elemento nella matrice PIDL, un valore di uno corrisponde al secondo elemento e così via. Nella funzione ReplacePage dell'applicazione di esempio, questo valore di parola alta viene passato a entrambi i gestori di sostituzione. Questi gestori, a loro volta, usano questo valore per identificare un dispositivo specifico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 



