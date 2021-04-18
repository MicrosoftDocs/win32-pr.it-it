---
description: Enumerazione degli effetti e delle transizioni
ms.assetid: 364b7bfb-5d6e-4ca6-b0c8-7a0180c3f61a
title: Enumerazione degli effetti e delle transizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e533f36501ac8da6015cc31eea6c2c111bf6a208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303969"
---
# <a name="enumerating-effects-and-transitions"></a>Enumerazione degli effetti e delle transizioni

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

DirectShow fornisce un oggetto [enumeratore dispositivo di sistema](system-device-enumerator.md) per l'enumerazione dei dispositivi. È possibile usarlo per recuperare i moniker per gli effetti o le transizioni installate nel sistema dell'utente.

System Device Enumerator espone l'interfaccia [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) . Restituisce gli enumeratori di categoria per le categorie di dispositivi specificate. Un enumeratore Category, a sua volta, espone l'interfaccia [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) e restituisce moniker per ogni dispositivo nella categoria. Per una descrizione dettagliata dell'uso di **ICreateDevEnum**, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md). Di seguito è riportato un breve riepilogo, specifico per i servizi di modifica DirectShow.

Per enumerare gli effetti o le transizioni, seguire questa procedura.

1.  Creare un'istanza dell'enumeratore di dispositivo di sistema.
2.  Chiamare il metodo [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) per recuperare un enumeratore Category. Le categorie sono definite dagli identificatori di classe (CLSID). Usare CLSID \_ VideoEffects1Category per Effects o CLSID \_ VideoEffects2Category per le transizioni.
3.  Chiamare **IEnumMoniker:: Next** per recuperare ogni moniker nell'enumerazione.
4.  Per ogni moniker, chiamare **IMoniker:: BindToStorage** per recuperare il contenitore delle proprietà associato.

Il contenitore delle proprietà contiene il nome descrittivo e l'identificatore univoco globale (GUID) per l'effetto o la transizione. Un'applicazione può visualizzare un elenco di nomi descrittivi e quindi ottenere il GUID corrispondente.

Nell'esempio di codice seguente vengono illustrati questi passaggi.


```C++
ICreateDevEnum *pCreateDevEnum = NULL;
IEnumMoniker *pEnumMoniker = NULL;

// Create the System Device Enumerator.
HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
    CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, (void**)&pCreateDevEnum);
if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

// Create an enumerator for the video effects category.
hr = pCreateDevEnum->CreateClassEnumerator(
    CLSID_VideoEffects1Category,  // Video effects category. 
    &pEnumMoniker, 0);               

// Note: Use CLSID_VideoEffects2Category for video transitions.

if (hr == S_OK)  // S_FALSE means the category is empty.
{
    // Enumerate each video effect.
    IMoniker *pMoniker;
    while (S_OK == pEnumMoniker->Next(1, &pMoniker, NULL))
    {
        IPropertyBag *pBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pBag);
        if(FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(OLESTR("FriendlyName"), &var, NULL);
        if (SUCCEEDED(hr))
        {
            if ( ... )  // Check if var.bstrVal is the name you want.
            {
                VARIANT var2;
                GUID guid;
                var2.vt = VT_BSTR;
                pBag->Read(OLESTR("guid"), &var2, NULL);
                CLSIDFromString(var2.bstrVal, &guid);
                VariantClear(&var2);
                // GUID is now the CLSID for the effect.
            }
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnumMoniker->Release();
}
pCreateDevEnum->Release();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo degli effetti e delle transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
