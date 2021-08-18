---
description: Scelta di un filtro di compressione
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Scelta di un filtro di compressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf964aa3647086efe569263e5fb36b4e0db60ebfad73c9d2fe9dcb14f3bcf125
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999221"
---
# <a name="choosing-a-compression-filter"></a>Scelta di un filtro di compressione

Diversi tipi di componenti software possono eseguire la compressione video o audio, ad esempio:

-   Filtri DirectShow nativi
-   Codec di Gestione compressione video
-   Codec di Gestione compressione audio
-   Oggetti multimediali DirectX (DMO)

In DirectShow, i codec VCM vengono incapsulati dal filtro [AVI Codec](avi-compressor-filter.md)e i codec ACM vengono incapsulati dal filtro [wrapper ACM](acm-wrapper-filter.md). Gli oggetti DMO vengono incapsulati dal [DMO wrapper.](dmo-wrapper-filter.md) L'enumeratore del dispositivo di sistema offre un modo coerente per enumerare e creare uno di questi tipi di compresso, senza preoccuparsi del modello sottostante.

Per informazioni dettagliate sull'enumeratore del dispositivo di sistema, vedere [Uso dell'enumeratore dispositivo di sistema](using-the-system-device-enumerator.md). Brevemente, tutti DirectShow filtri vengono classificati in base alla categoria e ogni categoria è identificata da un GUID. Per i proiettori video, il GUID della categoria è CLSID \_ VideoCompressorCategory. Per i proiettori audio, si tratta di CLSID \_ AudioCompressorCategory. Per enumerare una determinata categoria, l'enumeratore del dispositivo di sistema crea un *oggetto enumeratore* che supporta [**l'interfaccia IEnumMoniker.**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) L'applicazione usa questa interfaccia per recuperare i moniker del dispositivo, in cui ogni moniker di dispositivo rappresenta un'istanza di un DirectShow filtro. È possibile usare il moniker per creare il filtro o per ottenere il nome descrittivo del dispositivo senza creare il filtro.

Per enumerare i compressi audio o video disponibili nel sistema dell'utente, eseguire le operazioni seguenti:

1.  Chiamare [**CoCreateInstance per**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) creare l'enumeratore del dispositivo di sistema, che ha un ID di classe di CLSID \_ SystemDeviceEnum.
2.  Chiamare [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con il GUID della categoria di filtro. Il metodo restituisce un puntatore a **interfaccia IEnumMoniker.**
3.  Usare il metodo IEnumMoniker::Next per enumerare i moniker del dispositivo. Questo metodo restituisce [**un'interfaccia IMoniker,**](/windows/desktop/api/objidl/nn-objidl-imoniker) che rappresenta il moniker.

Per ottenere il nome descrittivo da un moniker, eseguire le operazioni seguenti:

1.  Chiamare il **metodo IMoniker::BindToStorage.** Questo metodo restituisce un puntatore a **interfaccia IPropertyBag.**
2.  Usare il **metodo IPropertyBag::Read** per leggere la **proprietà FriendlyName.**

In genere, un'applicazione visualizza un elenco di compresse, in modo che l'utente possa sceglierne uno. Ad esempio, il codice seguente popola una casella di riepilogo con i nomi dei compressi video disponibili.


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



Per creare un'istanza di filtro dal moniker, chiamare il **metodo IMoniker::BindToObject.** Il metodo restituisce un [**puntatore IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



Per i codec VCM, ogni moniker rappresenta un codec specifico, anche se tutti i codec sono incapsulati dallo stesso filtro di compressione AVI. La **chiamata a BindToObject** crea un'istanza di questo filtro, inizializzata per tale codec. Per questo motivo, non è possibile chiamare **CoCreateInstance** direttamente sul filtro di compressione AVI. È necessario passare attraverso l'enumeratore del dispositivo di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricompressione di un file AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 
