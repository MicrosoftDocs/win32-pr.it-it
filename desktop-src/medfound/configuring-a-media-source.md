---
description: Configurazione di un'origine multimediale
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Configurazione di un'origine multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 809d215cf282dba1e65c21316fafda47684a2151
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481707"
---
# <a name="configuring-a-media-source"></a>Configurazione di un'origine multimediale

Quando si usa il [sistema di risoluzione dell'origine](source-resolver.md) per creare un'origine multimediale, è possibile specificare un archivio delle proprietà che contiene le proprietà di configurazione. Queste proprietà verranno usate per inizializzare l'origine multimediale. Il set di proprietà supportate dipende dall'implementazione dell'origine multimediale. Non tutte le origini multimediali definiscono le proprietà di configurazione.

Nella tabella seguente sono elencate le proprietà di configurazione per le origini multimediali fornite in Media Foundation. Le origini multimediali di terze parti possono definire proprietà personalizzate.




| Origine multimediale | Proprietà | 
|--------------|------------|
| Origine di rete | Vedere <a href="network-source-features.md">Funzionalità dell'origine di rete</a>. | 
| Origine multimediale ASF | <ul><li><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></li><li><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></li><li><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></li><li><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></li></ul> | 




 

Per configurare un'origine, seguire questa procedura.

1.  Chiamare **PSCreateMemoryPropertyStore** per creare un nuovo archivio delle proprietà. Questa funzione restituisce un **puntatore IPropertyStore.**
2.  Chiamare **IPropertyStore::SetValue** per impostare una o più proprietà di configurazione.
3.  Chiamare una delle funzioni di creazione del resolver di origine, ad esempio [**IMFSourceResolver::CreateObjectFromURL,**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)e passare il puntatore **IPropertyStore** nel *parametro pProps.*


```C++
// Creates a media source from a URL.

HRESULT CreateMediaSource(
    PCWSTR pszURL, 
    IPropertyStore *pConfig,    // Optional, can be NULL
    IMFMediaSource **ppSource
    )
{
    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        DbgLog(L"CreateObjectFromURL");

        hr = pSourceResolver->CreateObjectFromURL(
            pszURL,                     
            MF_RESOLUTION_MEDIASOURCE,  // Create a media source.
            pConfig,                    // Configuration properties.
            &ObjectType,                // Receives the object type. 
            &pSource            
            );

        DbgLog(L"CreateObjectFromURL - FINISHED");

    }

    if (SUCCEEDED(hr))
    {
        hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));
    }

    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



Il sistema di risoluzione di origine passa il **puntatore IPropertyStore** direttamente al gestore dello schema o al gestore del flusso di byte che crea l'origine. Il sistema di risoluzione di origine non tenta di convalidare le proprietà.

In genere, queste proprietà vengono usate per le impostazioni avanzate. Se non si fornisce un archivio delle proprietà, l'origine dei supporti dovrebbe comunque funzionare correttamente con le impostazioni predefinite.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resolver di origine](source-resolver.md)
</dt> </dl>

 

 



