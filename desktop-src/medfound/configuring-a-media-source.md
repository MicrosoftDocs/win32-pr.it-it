---
description: Configurazione di un'origine multimediale
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Configurazione di un'origine multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea741e3c04282af445fbea7be07854bf517ec44f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320758"
---
# <a name="configuring-a-media-source"></a><span data-ttu-id="30f1f-103">Configurazione di un'origine multimediale</span><span class="sxs-lookup"><span data-stu-id="30f1f-103">Configuring a Media Source</span></span>

<span data-ttu-id="30f1f-104">Quando si usa il [resolver di origine](source-resolver.md) per creare un'origine multimediale, è possibile specificare un archivio di proprietà che contiene le proprietà di configurazione.</span><span class="sxs-lookup"><span data-stu-id="30f1f-104">When you use the [Source Resolver](source-resolver.md) to create a media source, you can specify a property store that contains configuration properties.</span></span> <span data-ttu-id="30f1f-105">Queste proprietà verranno usate per inizializzare l'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="30f1f-105">These properties will be used to initialize the media source.</span></span> <span data-ttu-id="30f1f-106">Il set di proprietà supportate dipende dall'implementazione dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="30f1f-106">The set of supported properties depends on the implementation of the media source.</span></span> <span data-ttu-id="30f1f-107">Non tutte le origini supporti definiscono le proprietà di configurazione.</span><span class="sxs-lookup"><span data-stu-id="30f1f-107">Not every media source defines configuration properties.</span></span>

<span data-ttu-id="30f1f-108">Nella tabella seguente sono elencate le proprietà di configurazione per le origini multimediali disponibili in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="30f1f-108">The following table lists the configuration properties for the media sources that are provided in Media Foundation.</span></span> <span data-ttu-id="30f1f-109">Le origini multimediali di terze parti possono definire proprietà personalizzate.</span><span class="sxs-lookup"><span data-stu-id="30f1f-109">Third-party media sources can define their own custom properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="30f1f-110">Origine supporto</span><span class="sxs-lookup"><span data-stu-id="30f1f-110">Media source</span></span></th>
<th><span data-ttu-id="30f1f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="30f1f-111">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="30f1f-112">Origine rete</span><span class="sxs-lookup"><span data-stu-id="30f1f-112">Network source</span></span></td>
<td><span data-ttu-id="30f1f-113">Vedere <a href="network-source-features.md">funzionalità dell'origine di rete</a>.</span><span class="sxs-lookup"><span data-stu-id="30f1f-113">See <a href="network-source-features.md">Network Source Features</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="30f1f-114">Origine supporto ASF</span><span class="sxs-lookup"><span data-stu-id="30f1f-114">ASF media source</span></span></td>
<td><ul>
<li><span data-ttu-id="30f1f-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span><span class="sxs-lookup"><span data-stu-id="30f1f-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span></span></li>
<li><span data-ttu-id="30f1f-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span><span class="sxs-lookup"><span data-stu-id="30f1f-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span></span></li>
<li><span data-ttu-id="30f1f-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span><span class="sxs-lookup"><span data-stu-id="30f1f-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span></span></li>
<li><span data-ttu-id="30f1f-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span><span class="sxs-lookup"><span data-stu-id="30f1f-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="30f1f-119">Per configurare un'origine, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="30f1f-119">To configure a source, perform the following steps.</span></span>

1.  <span data-ttu-id="30f1f-120">Chiamare **PSCreateMemoryPropertyStore** per creare un nuovo archivio delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="30f1f-120">Call **PSCreateMemoryPropertyStore** to create a new property store.</span></span> <span data-ttu-id="30f1f-121">Questa funzione restituisce un puntatore **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="30f1f-121">This function returns an **IPropertyStore** pointer.</span></span>
2.  <span data-ttu-id="30f1f-122">Chiamare **IPropertyStore:: SetValue** per impostare una o più proprietà di configurazione.</span><span class="sxs-lookup"><span data-stu-id="30f1f-122">Call **IPropertyStore::SetValue** to set one or more configuration properties.</span></span>
3.  <span data-ttu-id="30f1f-123">Chiamare una delle funzioni di creazione del resolver di origine, ad esempio [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), e passare il puntatore **IPropertyStore** nel parametro *pProps* .</span><span class="sxs-lookup"><span data-stu-id="30f1f-123">Call one of the source resolver's creation functions, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), and pass the **IPropertyStore** pointer in the *pProps* parameter.</span></span>


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



<span data-ttu-id="30f1f-124">Il resolver di origine passa il puntatore **IPropertyStore** direttamente al gestore dello schema o al gestore del flusso di byte che crea l'origine.</span><span class="sxs-lookup"><span data-stu-id="30f1f-124">The source resolver passes the **IPropertyStore** pointer directly to the scheme handler or byte-stream handler that creates the source.</span></span> <span data-ttu-id="30f1f-125">Il resolver di origine non esegue alcun tentativo di convalida delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="30f1f-125">The source resolver makes no attempt to validate the properties.</span></span>

<span data-ttu-id="30f1f-126">In genere, queste proprietà vengono usate per le impostazioni avanzate.</span><span class="sxs-lookup"><span data-stu-id="30f1f-126">Generally, these properties are used for advanced settings.</span></span> <span data-ttu-id="30f1f-127">Se non si fornisce un archivio delle proprietà, l'origine multimediale dovrebbe continuare a funzionare correttamente con le impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="30f1f-127">If you don't provide a property store, the media source should still function correctly with default settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30f1f-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="30f1f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30f1f-129">Resolver di origine</span><span class="sxs-lookup"><span data-stu-id="30f1f-129">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



