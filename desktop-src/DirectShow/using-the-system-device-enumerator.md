---
description: Uso dell'enumeratore del dispositivo di sistema
ms.assetid: 70db139c-2c5b-4574-bec3-dfe758b16715
title: Uso dell'enumeratore del dispositivo di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7192a1ea85d807dd388b79eef455edf59c83d3c22ab3a4a330799b3491253bb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083536"
---
# <a name="using-the-system-device-enumerator"></a>Uso dell'enumeratore del dispositivo di sistema

L'enumeratore dispositivo di sistema fornisce un modo uniforme per enumerare, per categoria, i filtri registrati nel sistema di un utente. Inoltre, distingue tra singoli dispositivi hardware, anche se lo stesso filtro li supporta. Ciò è particolarmente utile per i dispositivi che usano Windows Driver Model (WDM) e il filtro KSProxy. Ad esempio, l'utente potrebbe avere diversi dispositivi di acquisizione video WDM, tutti supportati dallo stesso filtro. L'enumeratore del dispositivo di sistema li considera come istanze di dispositivo separate.

L'enumeratore dispositivo di sistema funziona creando un enumeratore per una categoria specifica, ad esempio l'acquisizione audio o la compressione video. L'enumeratore di categoria restituisce un moniker univoco per ogni dispositivo nella categoria. L'enumeratore di categoria include automaticamente Plug and Play dispositivi pertinenti nella categoria. Per un elenco di categorie, vedere [Filtrare le categorie](filter-categories.md).

Per usare l'enumeratore del dispositivo di sistema, eseguire le operazioni seguenti:

1.  Creare l'enumeratore del dispositivo di sistema chiamando **CoCreateInstance**. L'identificatore di classe (CLSID) è CLSID \_ SystemDeviceEnum.
2.  Ottenere un enumeratore di categoria chiamando [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con il CLSID della categoria desiderata. Questo metodo restituisce un puntatore a **interfaccia IEnumMoniker.** Se la categoria è vuota (o non esiste), il metodo restituisce S \_ FALSE anziché un codice di errore. In tal caso, il **puntatore IEnumMoniker** restituito è **NULL** e la sua dereferenziazione causerà un'eccezione. Pertanto, testare in modo esplicito S \_ OK quando si chiama **CreateClassEnumerator**, anziché chiamare la consueta macro **SUCCEEDED.**
3.  Usare il **metodo IEnumMoniker::Next** per enumerare ogni moniker. Questo metodo restituisce un puntatore a **interfaccia IMoniker.** Quando il **metodo Next** raggiunge la fine dell'enumerazione, restituisce anche S FALSE, quindi controllare di nuovo \_ S \_ OK.
4.  Per recuperare il nome descrittivo del dispositivo, ad esempio da visualizzare nell'interfaccia utente, chiamare il metodo **IMoniker::BindToStorage.**
5.  Per creare e inizializzare DirectShow filtro che gestisce il dispositivo, chiamare **IMoniker::BindToObject** nel moniker. Chiamare [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il filtro al grafo.

La figura seguente illustra questo processo.

![enumerazione di dispositivi](images/sysdevenum.png)

L'esempio seguente illustra come enumerare i video compressi installati nel sistema dell'utente. Per brevità, l'esempio esegue un controllo degli errori minimo.


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

Per i moniker del dispositivo, è possibile passare il moniker al metodo [**IFilterGraph2::AddSourceFilterForMoniker**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-addsourcefilterformoniker) per creare un filtro di acquisizione per il dispositivo. Per il codice di esempio, vedere la documentazione relativa a tale metodo.

Il **metodo IMoniker::GetDisplayName** restituisce il nome visualizzato del moniker. Anche se il nome visualizzato è leggibile, in genere non lo si visualizza a un utente finale. Ottenere invece il nome descrittivo dall'elenco delle proprietà, come descritto in precedenza.

È possibile usare il metodo **IMoniker::P arseDisplayName** o la funzione **MkParseDisplayName** per creare un moniker di dispositivo predefinito per una determinata categoria di filtri. Usare un nome visualizzato con il formato `@device:*:{category-clsid}` , dove è la `category-clsid` rappresentazione di stringa del GUID della categoria. Il moniker predefinito è il primo moniker restituito dall'enumeratore del dispositivo per la categoria.

 

 



