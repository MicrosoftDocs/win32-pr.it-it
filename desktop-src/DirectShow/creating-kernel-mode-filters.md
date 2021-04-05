---
description: Creazione di filtri Kernel-Mode
ms.assetid: cbc86a5d-c53a-44a0-aa81-5c41527a8f67
title: Creazione di filtri Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c915a08312e33f0e35245325fd8bce7e55e486c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125415"
---
# <a name="creating-kernel-mode-filters"></a>Creazione di filtri Kernel-Mode

Alcuni filtri in modalità kernel non possono essere creati tramite **CoCreateInstance** e pertanto non hanno CLSID. Questi filtri includono il [convertitore Tee/Sink-to-sink](tee-sink-to-sink-converter.md), il filtro del [decodificatore CC](cc-decoder-filter.md) e il filtro [codec WST](wst-codec-filter.md) . Per creare uno di questi filtri, utilizzare l'oggetto [enumeratore dispositivo di sistema](system-device-enumerator.md) e cercare in base al nome del filtro.

1.  Creare l'enumeratore di dispositivo di sistema.
2.  Chiamare il metodo [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con il CLSID della categoria Filter per tale filtro. Questo metodo crea un enumeratore per la categoria Filter. Un *enumeratore* è semplicemente un oggetto che restituisce un elenco di altri oggetti usando un'interfaccia com definita. L'enumeratore restituisce i puntatori **IMoniker** , che rappresentano i filtri in tale categoria.
3.  Per ogni moniker, chiamare **IMoniker:: BindToStorage** per ottenere un'interfaccia **IPropertyBag** .
4.  Chiamare **IPropertyBag:: Read** per ottenere il nome del filtro.
5.  Se il nome corrisponde, chiamare **IMoniker:: BindToObject** per creare il filtro.

Nel codice seguente viene illustrata una funzione che esegue questi passaggi:


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



Nell'esempio di codice seguente viene usata questa funzione per creare il filtro del decodificatore CC e aggiungerlo al grafico del filtro:


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

[Argomenti sull'acquisizione avanzata](advanced-capture-topics.md)
</dt> <dt>

[Uso di System Device Enumerator](using-the-system-device-enumerator.md)
</dt> </dl>

 

 



