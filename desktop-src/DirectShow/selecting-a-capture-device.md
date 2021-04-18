---
description: Selezione di un dispositivo di acquisizione
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Selezione di un dispositivo di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b599728c6bd2d98b89285b6008923aa4fb2a3aef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303908"
---
# <a name="selecting-a-capture-device"></a>Selezione di un dispositivo di acquisizione

Per selezionare un dispositivo di acquisizione audio o video, usare l' [enumeratore](system-device-enumerator.md)del dispositivo di sistema, descritto nell'argomento [uso di System Device Enumerator](using-the-system-device-enumerator.md). L'enumeratore del dispositivo di sistema restituisce una raccolta di moniker di dispositivo, selezionati per categoria del dispositivo. Un *moniker* è un oggetto com che contiene informazioni su un altro oggetto. I moniker consentono all'applicazione di ottenere informazioni su un oggetto senza creare effettivamente l'oggetto. Successivamente, l'applicazione può utilizzare il moniker per creare l'oggetto. Per ulteriori informazioni sui moniker, vedere la documentazione relativa a [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).

Per usare l'enumeratore di dispositivo di sistema, seguire questa procedura.

1.  Chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un'istanza dell'enumeratore di dispositivo di sistema.
2.  Chiamare [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) e specificare la categoria del dispositivo come GUID. Per i dispositivi di acquisizione, le seguenti categorie sono rilevanti. 

    | GUID categoria                       | Descrizione           |
    |-------------------------------------|-----------------------|
    | **\_AUDIOINPUTDEVICECATEGORY CLSID** | Dispositivi di acquisizione audio |
    | **\_VIDEOINPUTDEVICECATEGORY CLSID** | Dispositivi di acquisizione video |

    

     

    Se una videocamera ha un microfono integrato, viene visualizzata in entrambe le categorie. Tuttavia, la fotocamera e il microfono vengono considerati dispositivi distinti dal sistema, ai fini dell'enumerazione, della creazione del dispositivo e del flusso di dati.

3.  Il metodo [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) restituisce un puntatore all'interfaccia [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) . Per enumerare i moniker, chiamare [**IEnumMoniker:: Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).

Il codice seguente crea un enumeratore per una categoria di dispositivi specificata.


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



L'interfaccia [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) enumera un elenco di interfacce [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) , ognuna delle quali rappresenta un moniker di dispositivo. L'applicazione può leggere le proprietà dal moniker oppure usare il moniker per creare un filtro di acquisizione DirectShow per il dispositivo. Le proprietà del moniker vengono restituite come valori **Variant** . Le proprietà seguenti sono supportate dai moniker del dispositivo.



| Proprietà       | Descrizione                                                               | Tipo VARIANT |
|----------------|---------------------------------------------------------------------------|--------------|
| FriendlyName | Nome del dispositivo.                                                   | **\_BSTR VT** |
| Descrizione  | Descrizione del modello.                                              | **\_BSTR VT** |
| DevicePath   | Stringa univoca che identifica il dispositivo. (Solo per dispositivi di acquisizione video). | **\_BSTR VT** |
| "WaveInID"     | Identificatore di un dispositivo di acquisizione audio. (Solo dispositivi di acquisizione audio.) | **VT \_ I4**   |



 

Le proprietà "FriendlyName" e "Description" sono adatte per la visualizzazione in un'interfaccia utente.

-   La proprietà "FriendlyName" è disponibile per ogni dispositivo. Contiene un nome leggibile per il dispositivo.
-   La proprietà "Description" è disponibile solo per i dispositivi DV e D-VHS/MPEG. Per ulteriori informazioni, vedere [driver Msdv](msdv-driver.md) e [driver MSTape](mstape-driver.md). Se disponibile, contiene una descrizione del dispositivo più specifica della proprietà "FriendlyName". In genere include il nome del fornitore.
-   La proprietà "DevicePath" non è una stringa leggibile, ma è sicuramente univoca per ogni dispositivo di acquisizione video nel sistema. È possibile usare questa proprietà per distinguere tra due o più istanze dello stesso modello di dispositivo.
-   Se è presente la proprietà "WaveInID", significa che il filtro di acquisizione DirectShow usa le API [audio della forma d'onda](../multimedia/waveform-audio.md) internamente per comunicare con il dispositivo. Il valore della proprietà "WaveInID" corrisponde all'identificatore usato dalle funzioni **WaveIn \** _, ad esempio [_ *waveInOpen* *](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).

Per leggere le proprietà dal moniker, seguire questa procedura.

1.  Chiamare [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) per ottenere un puntatore all'interfaccia [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) .
2.  Chiamare **IPropertyBag:: Read** per leggere la proprietà.

Nell'esempio di codice riportato di seguito viene illustrato come enumerare un elenco di moniker di dispositivo e recuperare le proprietà.


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



Per creare un filtro di acquisizione DirectShow per il dispositivo, chiamare il metodo [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) per ottenere un puntatore [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) . Quindi, chiamare [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il filtro al grafo del filtro:


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione audio](audio-capture.md)
</dt> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 
