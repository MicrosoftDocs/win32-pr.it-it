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
# <a name="shell-metadata-providers"></a><span data-ttu-id="180a8-103">Provider di metadati della shell</span><span class="sxs-lookup"><span data-stu-id="180a8-103">Shell Metadata Providers</span></span>

<span data-ttu-id="180a8-104">A partire da Windows 7, Microsoft Media Foundation espone i metadati tramite l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="180a8-104">Starting in Windows 7, Microsoft Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span>

<span data-ttu-id="180a8-105">I metadati ottenuti utilizzando il processo definito in questo argomento devono essere utilizzati solo per l'accesso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="180a8-105">Metadata obtained using the process defined in this topic should only be used for read-only access.</span></span> <span data-ttu-id="180a8-106">La scrittura di dati tramite questo processo non è supportata.</span><span class="sxs-lookup"><span data-stu-id="180a8-106">Writing data using this process is not supported.</span></span> <span data-ttu-id="180a8-107">È possibile creare un oggetto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a scopo di scrittura usando un identificatore di classe (CLSID) ottenuto da [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).</span><span class="sxs-lookup"><span data-stu-id="180a8-107">You can create an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object for writing purposes using a class identifier (CLSID) obtained from [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="180a8-108">Lettura dei metadati</span><span class="sxs-lookup"><span data-stu-id="180a8-108">Reading Metadata</span></span>

<span data-ttu-id="180a8-109">Per leggere i metadati da un'origine multimediale, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="180a8-109">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="180a8-110">Ottenere un puntatore all'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="180a8-110">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="180a8-111">Per ottenere un puntatore **IMFMediaSource** è possibile usare l'interfaccia [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .</span><span class="sxs-lookup"><span data-stu-id="180a8-111">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="180a8-112">Chiamare [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) sull'origine multimediale per ottenere un puntatore all'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="180a8-112">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span> <span data-ttu-id="180a8-113">Nel parametro *guidService* di **MFGetService** specificare il valore del **gestore di \_ proprietà \_ del \_ servizio MF**.</span><span class="sxs-lookup"><span data-stu-id="180a8-113">In the *guidService* parameter of **MFGetService**, specify the value **MF\_PROPERTY\_HANDLER\_SERVICE**.</span></span> <span data-ttu-id="180a8-114">Se l'origine non supporta l'interfaccia **IPropertyStore** , **MFGetService** restituisce il **\_ servizio MF E non \_ supportato \_**.</span><span class="sxs-lookup"><span data-stu-id="180a8-114">If the source does not support the **IPropertyStore** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
3.  <span data-ttu-id="180a8-115">Chiamare i metodi [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per enumerare le proprietà dei metadati.</span><span class="sxs-lookup"><span data-stu-id="180a8-115">Call [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods to enumerate the metadata properties.</span></span>

<span data-ttu-id="180a8-116">Nel codice seguente vengono illustrati questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="180a8-116">The following code shows these steps.</span></span> <span data-ttu-id="180a8-117">Si supponga che `DisplayProperty` sia una funzione che visualizza un valore **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="180a8-117">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


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



<span data-ttu-id="180a8-118">Per un elenco di chiavi di proprietà dei metadati, vedere [proprietà dei metadati per i file multimediali](metadata-properties-for-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="180a8-118">For a list of metadata property keys, see [Metadata Properties for Media Files](metadata-properties-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="180a8-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="180a8-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="180a8-120">Metadati del supporto</span><span class="sxs-lookup"><span data-stu-id="180a8-120">Media Metadata</span></span>](media-metadata.md)
</dt> </dl>

 

 
