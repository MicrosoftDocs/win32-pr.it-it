---
description: Scelta di un filtro di compressione
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Scelta di un filtro di compressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64ebebf41c35ed6aed9ab47d853c03ba720a31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125511"
---
# <a name="choosing-a-compression-filter"></a>Scelta di un filtro di compressione

Diversi tipi di componenti software possono eseguire la compressione video o audio, ad esempio:

-   Filtri DirectShow nativi
-   Codec di Gestione compressione video (VCM)
-   Codec di Gestione compressione audio (ACM)
-   Oggetti multimediali DirectX (DMOs)

In DirectShow, i codec VCM sono inclusi nel [filtro del compressore AVI](avi-compressor-filter.md)e i codec ACM sono inclusi nel [filtro del wrapper ACM](acm-wrapper-filter.md). DMOs è incluso nel [filtro del wrapper DMO](dmo-wrapper-filter.md). System Device Enumerator fornisce un modo coerente per enumerare e creare uno di questi tipi di compensatori, senza preoccuparsi del modello sottostante.

Per informazioni dettagliate sull'enumeratore di dispositivo di sistema, vedere [using the System Device Enumerator](using-the-system-device-enumerator.md). In breve, tutti i filtri DirectShow sono classificati in base alla categoria e ogni categoria viene identificata da un GUID. Per i commediatori video, il GUID categoria è CLSID \_ VideoCompressorCategory. Per i commediatori audio, è CLSID \_ AudioCompressorCategory. Per enumerare una particolare categoria, l'enumeratore di dispositivo di sistema crea un oggetto *enumeratore* che supporta l'interfaccia [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) . L'applicazione usa questa interfaccia per recuperare i moniker del dispositivo, dove ogni moniker del dispositivo rappresenta un'istanza di un filtro DirectShow. È possibile usare il moniker per creare il filtro o per ottenere il nome descrittivo del dispositivo senza creare il filtro.

Per enumerare i compressori video o audio disponibili nel sistema dell'utente, eseguire le operazioni seguenti:

1.  Chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare l'enumeratore di dispositivo di sistema, che ha un ID di classe CLSID \_ SystemDeviceEnum.
2.  Chiamare [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con il GUID della categoria di filtro. Il metodo restituisce un puntatore di interfaccia **IEnumMoniker** .
3.  Usare il Metodo IEnumMoniker:: Next per enumerare i moniker del dispositivo. Questo metodo restituisce un'interfaccia [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) , che rappresenta il moniker.

Per ottenere il nome descrittivo da un moniker, procedere come segue:

1.  Chiamare il metodo **IMoniker:: BindToStorage** . Questo metodo restituisce un puntatore all'interfaccia **IPropertyBag** .
2.  Usare il metodo **IPropertyBag:: Read** per leggere la proprietà **FriendlyName** .

In genere, in un'applicazione viene visualizzato un elenco di compressatori, in modo che l'utente possa sceglierne uno. Il codice seguente, ad esempio, popola una casella di riepilogo con i nomi dei commediatori video disponibili.


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



Per creare un'istanza di filtro dal moniker, chiamare il metodo **IMoniker:: BindToObject** . Il metodo restituisce un puntatore [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .


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



Per i codec VCM, ogni moniker rappresenta un codec particolare, anche se tutti i codec sono racchiusi dallo stesso filtro di compressione AVI. La chiamata a **BindToObject** crea un'istanza di questo filtro, inizializzata per il codec. Per questo motivo, non è possibile chiamare **CoCreateInstance** direttamente nel filtro di compressione AVI. È necessario esaminare l'enumeratore di dispositivo di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricompressione di un file AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 
