---
description: Creazione Kernel-Mode filtri
ms.assetid: cbc86a5d-c53a-44a0-aa81-5c41527a8f67
title: Creazione Kernel-Mode filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473565046c462e8992350c3662360e4c22b3b5b75e10f0e79e1399885355056e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953940"
---
# <a name="creating-kernel-mode-filters"></a>Creazione Kernel-Mode filtri

Alcuni filtri in modalità kernel non possono essere creati tramite **CoCreateInstance** e pertanto non dispongono di CLSID. Questi filtri includono [il convertitore Tee/Sink-to-Sink,](tee-sink-to-sink-converter.md)il filtro [CC Decoder](cc-decoder-filter.md) e il filtro [codec WST.](wst-codec-filter.md) Per creare uno di questi filtri, usare [l'oggetto System Device Enumerator](system-device-enumerator.md) e cercare in base al nome del filtro.

1.  Creare l'enumeratore del dispositivo di sistema.
2.  Chiamare il [**metodo ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con il CLSID della categoria di filtro per il filtro. Questo metodo crea un enumeratore per la categoria di filtri. Un *enumeratore* è semplicemente un oggetto che restituisce un elenco di altri oggetti usando un'interfaccia COM definita. L'enumeratore **restituisce puntatori IMoniker,** che rappresentano i filtri in tale categoria.
3.  Per ogni moniker, chiamare **IMoniker::BindToStorage** per ottenere **un'interfaccia IPropertyBag.**
4.  Chiamare **IPropertyBag::Read** per ottenere il nome del filtro.
5.  Se il nome corrisponde, chiamare **IMoniker::BindToObject** per creare il filtro.

Il codice seguente illustra una funzione che esegue questi passaggi:


```C++
HRESULT CreateKernelFilter(
    const GUID &guidCategory,  // Filter category.
    LPCOLESTR szName,          // The name of the filter.
    IBaseFilter **ppFilter     // Receives a pointer to the filter.
)
{
    HRESULT hr;
    ICreateDevEnum *pDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    if (!szName || !ppFilter) 
    {
        return E_POINTER;
    }

    // Create the system device enumerator.
    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC,
        IID_ICreateDevEnum, (void**)&pDevEnum);
    if (FAILED(hr))
    {
        return hr;
    }

    // Create a class enumerator for the specified category.
    hr = pDevEnum->CreateClassEnumerator(guidCategory, &pEnum, 0);
    pDevEnum->Release();
    if (hr != S_OK) // S_FALSE means the category is empty.
    {
        return E_FAIL;
    }

    // Enumerate devices within this category.
    bool bFound = false;
    IMoniker *pMoniker;
    while (!bFound && (S_OK == pEnum->Next(1, &pMoniker, 0)))
    {
        IPropertyBag *pBag = NULL;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, (void **)&pBag);
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        // Check the friendly name.
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(L"FriendlyName", &var, NULL);
        if (SUCCEEDED(hr) && (lstrcmpiW(var.bstrVal, szName) == 0))
        {
            // This is the right filter.
            hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter,
                (void**)ppFilter);
            bFound = true;
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnum->Release();
    return (bFound ? hr : E_FAIL);
}
```



L'esempio di codice seguente usa questa funzione per creare il filtro CC Decoder e aggiungerlo al grafico dei filtri:


```C++
IBaseFilter *pCC = NULL;
hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
    OLESTR("CC Decoder"), &pCC);
if (SUCCEEDED(hr))
{
    hr = pGraph->AddFilter(pCC, L"CC Decoder");
    pCC->Release();
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti di acquisizione avanzata](advanced-capture-topics.md)
</dt> <dt>

[Uso dell'enumeratore del dispositivo di sistema](using-the-system-device-enumerator.md)
</dt> </dl>

 

 



