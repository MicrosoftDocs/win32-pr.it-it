---
description: A partire da Windows 7, Microsoft Media Foundation espone i metadati tramite l'interfaccia IPropertyStore.
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Provider di metadati della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35488e750531a5ee7bac7dc915990593ecee1d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308997"
---
# <a name="shell-metadata-providers"></a>Provider di metadati della shell

A partire da Windows 7, Microsoft Media Foundation espone i metadati tramite l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

I metadati ottenuti utilizzando il processo definito in questo argomento devono essere utilizzati solo per l'accesso in sola lettura. La scrittura di dati tramite questo processo non è supportata. È possibile creare un oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a scopo di scrittura usando un identificatore di classe (CLSID) ottenuto da [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).

## <a name="reading-metadata"></a>Lettura dei metadati

Per leggere i metadati da un'origine multimediale, seguire questa procedura:

1.  Ottenere un puntatore all'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine multimediale. Per ottenere un puntatore **IMFMediaSource** è possibile usare l'interfaccia [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .
2.  Chiamare [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) sull'origine multimediale per ottenere un puntatore all'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . Nel parametro *guidService* di **MFGetService** specificare il valore del **gestore di \_ proprietà \_ del \_ servizio MF**. Se l'origine non supporta l'interfaccia **IPropertyStore** , **MFGetService** restituisce il **\_ servizio MF E non \_ supportato \_**.
3.  Chiamare i metodi [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per enumerare le proprietà dei metadati.

Nel codice seguente vengono illustrati questi passaggi. Si supponga che `DisplayProperty` sia una funzione che visualizza un valore **PROPVARIANT** .


```C++
HRESULT EnumerateMetadata(IMFMediaSource *pSource)
{
    IPropertyStore *pProps = NULL;

    HRESULT hr = MFGetService(
        pSource, MF_PROPERTY_HANDLER_SERVICE, IID_PPV_ARGS(&pProps));

    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cProps;

    hr = pProps->GetCount(&cProps);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cProps; i++)
    {
        PROPERTYKEY key;
        hr = pProps->GetAt(i, &key);
        if (FAILED(hr))
        {
            goto done;
        }

        PROPVARIANT pv;

        hr = pProps->GetValue(key, &pv);
        if (FAILED(hr))
        {
            goto done;
        }

        DisplayProperty(key, pv);
        PropVariantClear(&pv);
    }

done:
    SafeRelease(&pProps);
    return hr;
}
```



Per un elenco di chiavi di proprietà dei metadati, vedere [proprietà dei metadati per i file multimediali](metadata-properties-for-media-files.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Metadati del supporto](media-metadata.md)
</dt> </dl>

 

 
