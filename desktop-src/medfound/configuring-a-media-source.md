---
description: Configurazione di un'origine multimediale
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Configurazione di un'origine multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e6737d643db2ee473214586cd7ded4f9596133dac5f4fb177df4d7b6b19757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880592"
---
# <a name="configuring-a-media-source"></a>Configurazione di un'origine multimediale

Quando si usa il [sistema di risoluzione dell'origine](source-resolver.md) per creare un'origine multimediale, è possibile specificare un archivio delle proprietà che contiene le proprietà di configurazione. Queste proprietà verranno usate per inizializzare l'origine multimediale. Il set di proprietà supportate dipende dall'implementazione dell'origine multimediale. Non tutte le origini multimediali definiscono le proprietà di configurazione.

Nella tabella seguente sono elencate le proprietà di configurazione per le origini multimediali fornite in Media Foundation. Le origini multimediali di terze parti possono definire proprietà personalizzate.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Origine multimediale</th>
<th>Proprietà</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Origine di rete</td>
<td>Vedere <a href="network-source-features.md">Funzionalità dell'origine di rete</a>.</td>
</tr>
<tr class="even">
<td>Origine multimediale ASF</td>
<td><ul>
<li><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></li>
<li><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></li>
<li><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></li>
<li><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></li>
</ul></td>
</tr>
</tbody>
</table>



 

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



Il resolver di origine passa il **puntatore IPropertyStore** direttamente al gestore dello schema o al gestore del flusso di byte che crea l'origine. Il sistema di risoluzione di origine non tenta di convalidare le proprietà.

In genere, queste proprietà vengono usate per le impostazioni avanzate. Se non si fornisce un archivio delle proprietà, l'origine dei supporti dovrebbe comunque funzionare correttamente con le impostazioni predefinite.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resolver di origine](source-resolver.md)
</dt> </dl>

 

 



