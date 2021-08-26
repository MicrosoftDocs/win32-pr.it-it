---
description: Selezione di un dispositivo di acquisizione
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Selezione di un dispositivo di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5bf92692070c8a0191a91559481d5446bf3d4d894c8e7f6aafc2ed9e73a6667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904411"
---
# <a name="selecting-a-capture-device"></a>Selezione di un dispositivo di acquisizione

Per selezionare un dispositivo di acquisizione audio o video, usare [l'enumeratore](system-device-enumerator.md)dispositivo di sistema , descritto nell'argomento [Uso dell'enumeratore dispositivo di sistema](using-the-system-device-enumerator.md). L'enumeratore del dispositivo di sistema restituisce una raccolta di moniker del dispositivo, selezionati per categoria di dispositivi. Un *moniker è* un oggetto COM che contiene informazioni su un altro oggetto. I moniker consentono all'applicazione di ottenere informazioni su un oggetto senza creare effettivamente l'oggetto. Successivamente, l'applicazione può usare il moniker per creare l'oggetto . Per altre informazioni sui moniker, vedere la documentazione di [**IMoniker.**](/windows/win32/api/objidl/nn-objidl-imoniker)

Per usare l'enumeratore del dispositivo di sistema, seguire questa procedura.

1.  Chiamare [**CoCreateInstance per**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) creare un'istanza dell'enumeratore dispositivo di sistema.
2.  Chiamare [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) e specificare la categoria di dispositivi come GUID. Per i dispositivi di acquisizione, le categorie seguenti sono rilevanti. 

    | GUID della categoria                       | Descrizione           |
    |-------------------------------------|-----------------------|
    | **CLSID \_ AudioInputDeviceCategory** | Dispositivi di acquisizione audio |
    | **CLSID \_ VideoInputDeviceCategory** | Dispositivi di acquisizione video |

    

     

    Se una videocamera ha un microfono integrato, viene visualizzata in entrambe le categorie. Tuttavia, la fotocamera e il microfono vengono trattati come dispositivi separati dal sistema, ai fini dell'enumerazione, della creazione del dispositivo e dello streaming dei dati.

3.  Il [**metodo CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) restituisce un [**puntatore all'interfaccia IEnumMoniker.**](/windows/win32/api/objidl/nn-objidl-ienummoniker) Per enumerare i moniker, chiamare [**IEnumMoniker::Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).

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



[**L'interfaccia IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) enumera un elenco di interfacce [**IMoniker,**](/windows/win32/api/objidl/nn-objidl-imoniker) ognuna delle quali rappresenta un moniker di dispositivo. L'applicazione può leggere le proprietà dal moniker o usare il moniker per creare un filtro di acquisizione DirectShow per il dispositivo. Le proprietà del moniker vengono restituite **come valori VARIANT.** Le proprietà seguenti sono supportate dai moniker dei dispositivi.



| Proprietà       | Descrizione                                                               | Tipo VARIANT |
|----------------|---------------------------------------------------------------------------|--------------|
| "FriendlyName" | Nome del dispositivo.                                                   | **VT \_ BSTR** |
| "Descrizione"  | Descrizione del modello.                                              | **VT \_ BSTR** |
| "DevicePath"   | Stringa univoca che identifica il dispositivo. (Solo dispositivi di acquisizione video). | **VT \_ BSTR** |
| "WaveInID"     | Identificatore di un dispositivo di acquisizione audio. (Solo dispositivi di acquisizione audio). | **VT \_ I4**   |



 

Le proprietà "FriendlyName" e "Description" sono adatte per la visualizzazione in un'interfaccia utente.

-   La proprietà "FriendlyName" è disponibile per ogni dispositivo. Contiene un nome leggibile per il dispositivo.
-   La proprietà "Description" è disponibile solo per i dispositivi camcorder DV e D-VHS/MPEG. Per altre informazioni, vedere [Driver MSDV](msdv-driver.md) e [DRIVER MSTape](mstape-driver.md). Se disponibile, contiene una descrizione del dispositivo più specifica della proprietà "FriendlyName". In genere include il nome del fornitore.
-   La proprietà "DevicePath" non è una stringa leggibile dall'utente, ma è garantita che sia univoca per ogni dispositivo di acquisizione video nel sistema. È possibile usare questa proprietà per distinguere tra due o più istanze dello stesso modello di dispositivo.
-   Se la proprietà "WaveInID" è presente, significa che il filtro di acquisizione DirectShow usa internamente le API [Audio Waveform](../multimedia/waveform-audio.md) per comunicare con il dispositivo. Il valore della proprietà "WaveInID" corrisponde all'identificatore usato dalle funzioni **\* waveIn* _, ad esempio [_ *waveInOpen* *](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).

Per leggere le proprietà dal moniker, seguire questa procedura.

1.  Chiamare [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) per ottenere un puntatore [**all'interfaccia IPropertyBag.**](../com/ipropertybag-and-ipersistpropertybag.md)
2.  Chiamare **IPropertyBag::Read** per leggere la proprietà.

Nell'esempio di codice seguente viene illustrato come enumerare un elenco di moniker del dispositivo e ottenere le proprietà .


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



Per creare un DirectShow di acquisizione per il dispositivo, chiamare il metodo [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) per ottenere un [**puntatore IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) Chiamare quindi [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il filtro al grafico dei filtri:


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

 

 
