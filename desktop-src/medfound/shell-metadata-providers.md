---
description: A partire Windows 7, Microsoft Media Foundation i metadati tramite l'interfaccia IPropertyStore.
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Provider di metadati della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31960ed41743a86b62b63555236d2876166a14b098f0692f3d6cb22b051e338e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713361"
---
# <a name="shell-metadata-providers"></a>Provider di metadati della shell

A partire Windows 7, Microsoft Media Foundation i metadati tramite [**l'interfaccia IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

I metadati ottenuti usando il processo definito in questo argomento devono essere usati solo per l'accesso in sola lettura. La scrittura di dati tramite questo processo non è supportata. È possibile creare un [**oggetto IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a scopo di scrittura usando un identificatore di classe (CLSID) ottenuto da [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).

## <a name="reading-metadata"></a>Lettura di metadati

Per leggere i metadati da un'origine multimediale, seguire questa procedura:

1.  Ottenere un puntatore [**all'interfaccia IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine multimediale. È possibile usare [**l'interfaccia IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) per ottenere un **puntatore IMFMediaSource.**
2.  Chiamare [**MFGetService nell'origine**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) multimediale per ottenere un puntatore [**all'interfaccia IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore) Nel parametro *guidService* di **MFGetService** specificare il valore **MF \_ PROPERTY HANDLER \_ \_ SERVICE**. Se l'origine non supporta **l'interfaccia IPropertyStore,** **MFGetService** restituisce **MF \_ E \_ UNSUPPORTED \_ SERVICE**.
3.  Chiamare [**i metodi IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per enumerare le proprietà dei metadati.

Il codice seguente illustra questi passaggi. Si supponga `DisplayProperty` che sia una funzione che visualizza un valore **PROPVARIANT.**


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



Per un elenco delle chiavi delle proprietà dei metadati, vedere [Proprietà dei metadati per i file multimediali.](metadata-properties-for-media-files.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Metadati multimediali](media-metadata.md)
</dt> </dl>

 

 
