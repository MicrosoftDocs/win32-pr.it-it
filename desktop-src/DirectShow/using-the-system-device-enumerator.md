---
description: Uso di System Device Enumerator
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Uso di System Device Enumerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f8f66cb64e9f7bb51d6b0716b9fa23cf531435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564174"
---
# <a name="using-the-system-device-enumerator"></a>Uso di System Device Enumerator

L'enumeratore di dispositivo System fornisce un modo uniforme per enumerare, per categoria, i filtri registrati nel sistema di un utente. Inoltre, distingue tra i singoli dispositivi hardware, anche se lo stesso filtro li supporta. Questa operazione è particolarmente utile per i dispositivi che usano il Windows Driver Model (WDM) e il filtro KSProxy. Ad esempio, l'utente potrebbe avere diversi dispositivi di acquisizione video WDM, tutti supportati dallo stesso filtro. L'enumeratore di dispositivi di sistema li considera come istanze di dispositivo separate.

L'enumeratore di dispositivi di sistema funziona creando un enumeratore per una categoria specifica, ad esempio l'acquisizione audio o la compressione video. L'enumeratore Category restituisce un moniker univoco per ogni dispositivo nella categoria. L'enumeratore Category include automaticamente eventuali dispositivi Plug and Play rilevanti nella categoria. Per un elenco di categorie, vedere [filtrare le categorie](filter-categories.md).

Per usare l'enumeratore di dispositivo di sistema, eseguire le operazioni seguenti:

1.  Creare l'enumeratore di dispositivo di sistema chiamando **CoCreateInstance**. L'identificatore di classe (CLSID) è CLSID \_ SystemDeviceEnum.
2.  Ottenere un enumeratore Category chiamando [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con il CLSID della categoria desiderata. Questo metodo restituisce un puntatore all'interfaccia **IEnumMoniker** . Se la categoria è vuota (o non esiste), il metodo restituisce \_ false anziché un codice di errore. In caso affermativo, il puntatore **IEnumMoniker** restituito è **null** e la dereferenziazione provocherà un'eccezione. Pertanto, testare in modo esplicito for S \_ OK quando si chiama **CreateClassEnumerator**, invece di chiamare la normale macro **succeeded** .
3.  Usare il metodo **IEnumMoniker:: Next** per enumerare ogni moniker. Questo metodo restituisce un puntatore a interfaccia **IMoniker** . Quando il metodo **successivo** raggiunge la fine dell'enumerazione, restituisce anche s \_ false, quindi controlla di nuovo la presenza di s \_ OK.
4.  Per recuperare il nome descrittivo del dispositivo (ad esempio, per visualizzarlo nell'interfaccia utente), chiamare il metodo **IMoniker:: BindToStorage** .
5.  Per creare e inizializzare il filtro DirectShow che gestisce il dispositivo, chiamare **IMoniker:: BindToObject** nel moniker. Chiamare [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il filtro al grafo.

La figura seguente illustra questo processo.

![Enumerazione dei dispositivi](images/sysdevenum.png)

Nell'esempio seguente viene illustrato come enumerare i compressioni video installati nel sistema dell'utente. Per brevità, nell'esempio viene eseguito il controllo minimo degli errori.


```C++
// Create the System Device Enumerator.
HRESULT hr;
ICreateDevEnum *pSysDevEnum = NULL;
hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, CLSCTX_INPROC_SERVER,
    IID_ICreateDevEnum, (void **)&pSysDevEnum);
if (FAILED(hr))
{
    return hr;
}

// Obtain a class enumerator for the video compressor category.
IEnumMoniker *pEnumCat = NULL;
hr = pSysDevEnum->CreateClassEnumerator(CLSID_VideoCompressorCategory, &pEnumCat, 0);

if (hr == S_OK) 
{
    // Enumerate the monikers.
    IMoniker *pMoniker = NULL;
    ULONG cFetched;
    while(pEnumCat->Next(1, &pMoniker, &cFetched) == S_OK)
    {
        IPropertyBag *pPropBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pPropBag);
        if (SUCCEEDED(hr))
        {
            // To retrieve the filter's friendly name, do the following:
            VARIANT varName;
            VariantInit(&varName);
            hr = pPropBag->Read(L"FriendlyName", &varName, 0);
            if (SUCCEEDED(hr))
            {
                // Display the name in your UI somehow.
            }
            VariantClear(&varName);

            // To create an instance of the filter, do the following:
            IBaseFilter *pFilter;
            hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter,
                (void**)&pFilter);
            // Now add the filter to the graph. 
            //Remember to release pFilter later.
            pPropBag->Release();
        }
        pMoniker->Release();
    }
    pEnumCat->Release();
}
pSysDevEnum->Release();
```



**Moniker del dispositivo**

Per i moniker del dispositivo, è possibile passare il moniker al metodo [**IFilterGraph2:: AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) per creare un filtro di acquisizione per il dispositivo. Per un esempio di codice, vedere la documentazione relativa a tale metodo.

Il metodo **IMoniker:: GetDisplayName** restituisce il nome visualizzato del moniker. Sebbene il nome visualizzato sia leggibile, in genere non viene visualizzato a un utente finale. Ottenere invece il nome descrittivo dall'elenco delle proprietà, come descritto in precedenza.

Il metodo **IMoniker::P arsedisplayname** o la funzione **MkParseDisplayName** può essere usato per creare un moniker di dispositivo predefinito per una categoria di filtro specificata. Usare un nome visualizzato con il formato `@device:*:{category-clsid}` , dove `category-clsid` è la rappresentazione di stringa del GUID di categoria. Il moniker predefinito è il primo moniker restituito dall'enumeratore del dispositivo per tale categoria.

 

 



