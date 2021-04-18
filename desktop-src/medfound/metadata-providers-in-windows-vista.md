---
description: In Windows Vista Microsoft Media Foundation espone i metadati tramite l'interfaccia IMFMetadata.
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: Provider di metadati in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1726e04058a7b15e387fca4f3faa94fce7c91c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307990"
---
# <a name="metadata-providers-in-windows-vista"></a><span data-ttu-id="816dc-103">Provider di metadati in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="816dc-103">Metadata Providers in Windows Vista</span></span>

<span data-ttu-id="816dc-104">In Windows Vista Microsoft Media Foundation espone i metadati tramite l'interfaccia [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="816dc-104">In Windows Vista, Microsoft Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="816dc-105">Lettura dei metadati</span><span class="sxs-lookup"><span data-stu-id="816dc-105">Reading Metadata</span></span>

<span data-ttu-id="816dc-106">Per leggere i metadati da un'origine multimediale, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="816dc-106">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="816dc-107">Ottenere un puntatore all'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="816dc-107">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="816dc-108">Per ottenere un puntatore **IMFMediaSource** è possibile usare l'interfaccia [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .</span><span class="sxs-lookup"><span data-stu-id="816dc-108">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="816dc-109">Chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) per ottenere il descrittore di presentazione dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="816dc-109">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="816dc-110">Chiamare [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) sull'origine multimediale per ottenere un puntatore all'interfaccia [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) .</span><span class="sxs-lookup"><span data-stu-id="816dc-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span> <span data-ttu-id="816dc-111">Nel parametro *guidService* di **MFGetService** specificare il valore **MF \_ Metadata \_ provider \_ Service**.</span><span class="sxs-lookup"><span data-stu-id="816dc-111">In the *guidService* parameter of **MFGetService**, specify the value **MF\_METADATA\_PROVIDER\_SERVICE**.</span></span> <span data-ttu-id="816dc-112">Se l'origine non supporta l'interfaccia **IMFMetadataProvider** , **MFGetService** restituisce il **\_ servizio MF E non \_ supportato \_**.</span><span class="sxs-lookup"><span data-stu-id="816dc-112">If the source does not support the **IMFMetadataProvider** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
4.  <span data-ttu-id="816dc-113">Chiamare [**IMFMetadataProvider:: GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) e passare un puntatore al descrittore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="816dc-113">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) and pass in a pointer to the presentation descriptor.</span></span> <span data-ttu-id="816dc-114">Questo metodo restituisce un puntatore all'interfaccia [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="816dc-114">This method returns a pointer to the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>
    -   <span data-ttu-id="816dc-115">Per ottenere prima i metadati a livello di flusso, chiamare [**IMFStreamDescriptor:: GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) per ottenere l'identificatore del flusso.</span><span class="sxs-lookup"><span data-stu-id="816dc-115">To get stream-level metadata first call [**IMFStreamDescriptor::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) to get the stream identifier.</span></span> <span data-ttu-id="816dc-116">Passare quindi l'identificatore del flusso nel parametro *dwStreamIdentifier* di [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).</span><span class="sxs-lookup"><span data-stu-id="816dc-116">Then pass the stream identifier in the *dwStreamIdentifier* parameter of [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).</span></span>
    -   <span data-ttu-id="816dc-117">Per ottenere i metadati a livello di presentazione, impostare *dwStreamIdentifier* su zero.</span><span class="sxs-lookup"><span data-stu-id="816dc-117">To get presentation-level metadata, set *dwStreamIdentifier* to zero.</span></span>
5.  <span data-ttu-id="816dc-118">\[Chiamata facoltativa \] [**IMFMetadata:: GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) per ottenere un elenco delle lingue in cui sono disponibili i metadati.</span><span class="sxs-lookup"><span data-stu-id="816dc-118">\[Optional\] Call [**IMFMetadata::GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) to get a list of the languages in which metadata is available.</span></span> <span data-ttu-id="816dc-119">Le lingue vengono identificate usando i tag di linguaggio conformi a RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="816dc-119">Languages are identified using RFC 1766-compliant language tags.</span></span>
6.  <span data-ttu-id="816dc-120">\[\]Per selezionare la lingua, chiamare [**IMFMetadata:: tolanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) .</span><span class="sxs-lookup"><span data-stu-id="816dc-120">\[Optional\] Call [**IMFMetadata::SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) to select the language.</span></span>
7.  <span data-ttu-id="816dc-121">\[Chiamata facoltativa \] [**IMFMetadata:: GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) per ottenere un elenco dei nomi di tutte le proprietà dei metadati per il flusso o la presentazione.</span><span class="sxs-lookup"><span data-stu-id="816dc-121">\[Optional\] Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to get a list of the names of all the metadata properties for this stream or presentation.</span></span>
8.  <span data-ttu-id="816dc-122">Chiamare [**IMFMetadata:: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) per ottenere un valore specifico della proprietà dei metadati, passando il nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="816dc-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get a specific metadata property value, passing in the name of the property.</span></span>

<span data-ttu-id="816dc-123">Il codice seguente illustra i passaggi da 2 a 4:</span><span class="sxs-lookup"><span data-stu-id="816dc-123">The following code shows steps 2–4:</span></span>


```C++
HRESULT GetMetadata(
    IMFMediaSource *pSource, IMFMetadata **ppMetadata, DWORD dwStream = 0)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFMetadataProvider *pProvider = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFGetService(
        pSource, MF_METADATA_PROVIDER_SERVICE, IID_PPV_ARGS(&pProvider));

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProvider->GetMFMetadata(pPD, dwStream, 0, ppMetadata);

done:
    SafeRelease(&pPD);
    SafeRelease(&pProvider);
    return hr;
}
```



<span data-ttu-id="816dc-124">Il codice seguente illustra i passaggi da 7 a 8.</span><span class="sxs-lookup"><span data-stu-id="816dc-124">The following code shows steps 7–8.</span></span> <span data-ttu-id="816dc-125">Si supponga che `DisplayProperty` sia una funzione che visualizza un valore **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="816dc-125">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


```C++
HRESULT DisplayMetadata(IMFMetadata *pMetadata)
{
    PROPVARIANT varNames;
    HRESULT hr = pMetadata->GetAllPropertyNames(&varNames);
    if (FAILED(hr))
    {
        return hr;
    }

    for (ULONG i = 0; i < varNames.calpwstr.cElems; i++)
    {
        wprintf(L"%s\n", varNames.calpwstr.pElems[i]);

        PROPVARIANT varValue;
        hr = pMetadata->GetProperty( varNames.calpwstr.pElems[i], &varValue );
        if (SUCCEEDED(hr))
        {
            DisplayProperty(varValue);
            PropVariantClear(&varValue);
        }
    }

    PropVariantClear(&varNames);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="816dc-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="816dc-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="816dc-127">Metadati del supporto</span><span class="sxs-lookup"><span data-stu-id="816dc-127">Media Metadata</span></span>](media-metadata.md)
</dt> <dt>

[<span data-ttu-id="816dc-128">Provider di metadati della shell</span><span class="sxs-lookup"><span data-stu-id="816dc-128">Shell Metadata Providers</span></span>](shell-metadata-providers.md)
</dt> </dl>

 

 



