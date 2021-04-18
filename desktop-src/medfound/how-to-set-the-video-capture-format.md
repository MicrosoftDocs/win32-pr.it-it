---
description: Un dispositivo di acquisizione video potrebbe supportare diversi formati di acquisizione. I formati generalmente variano in base al tipo di compressione, allo spazio colore (YUV o RGB), alle dimensioni del frame o alla frequenza dei fotogrammi.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Come impostare il formato di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27cb9c20cbf989ab5db3564733dc96860c7bcb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310841"
---
# <a name="how-to-set-the-video-capture-format"></a><span data-ttu-id="17aef-104">Come impostare il formato di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="17aef-104">How to Set the Video Capture Format</span></span>

<span data-ttu-id="17aef-105">Un dispositivo di acquisizione video potrebbe supportare diversi formati di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="17aef-105">A video capture device might support several capture formats.</span></span> <span data-ttu-id="17aef-106">I formati generalmente variano in base al tipo di compressione, allo spazio colore (YUV o RGB), alle dimensioni del frame o alla frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="17aef-106">Formats typically differ by compression type, color space (YUV or RGB), frame size, or frame rate.</span></span>

<span data-ttu-id="17aef-107">L'elenco dei formati supportati è contenuto nel *descrittore della presentazione*.</span><span class="sxs-lookup"><span data-stu-id="17aef-107">The list of supported formats is contained in the *presentation descriptor*.</span></span> <span data-ttu-id="17aef-108">Per ulteriori informazioni, vedere [descrittori di presentazione](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="17aef-108">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="17aef-109">Per enumerare i formati supportati:</span><span class="sxs-lookup"><span data-stu-id="17aef-109">To enumerate the supported formats:</span></span>

1.  <span data-ttu-id="17aef-110">Creare l'origine multimediale per il dispositivo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="17aef-110">Create the media source for the capture device.</span></span> <span data-ttu-id="17aef-111">Vedere [enumerazione dei dispositivi di acquisizione video](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="17aef-111">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="17aef-112">Chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sull'origine del supporto per ottenere il descrittore della presentazione.</span><span class="sxs-lookup"><span data-stu-id="17aef-112">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="17aef-113">Chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) per ottenere il descrittore del flusso per il flusso video.</span><span class="sxs-lookup"><span data-stu-id="17aef-113">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="17aef-114">Chiamare [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sul descrittore del flusso.</span><span class="sxs-lookup"><span data-stu-id="17aef-114">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="17aef-115">Chiamare [**IMFMediaTypeHandler:: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) per ottenere il numero di formati supportati.</span><span class="sxs-lookup"><span data-stu-id="17aef-115">Call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) to get the number of supported formats.</span></span>
6.  <span data-ttu-id="17aef-116">In un ciclo, chiamare [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) per ottenere ogni formato.</span><span class="sxs-lookup"><span data-stu-id="17aef-116">In a loop, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get each format.</span></span> <span data-ttu-id="17aef-117">Il formato è rappresentato da un *tipo di supporto*.</span><span class="sxs-lookup"><span data-stu-id="17aef-117">The format is represented by a *media type*.</span></span> <span data-ttu-id="17aef-118">Per ulteriori informazioni, vedere [tipi di supporti video](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="17aef-118">For more information, see [Video Media Types](video-media-types.md).</span></span>

<span data-ttu-id="17aef-119">Nell'esempio seguente vengono enumerati i formati di acquisizione per un dispositivo:</span><span class="sxs-lookup"><span data-stu-id="17aef-119">The following example enumerates the capture formats for a device:</span></span>


```C++
HRESULT EnumerateCaptureFormats(IMFMediaSource *pSource)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFStreamDescriptor *pSD = NULL;
    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pType = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL fSelected;
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cTypes = 0;
    hr = pHandler->GetMediaTypeCount(&cTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cTypes; i++)
    {
        hr = pHandler->GetMediaTypeByIndex(i, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        LogMediaType(pType);
        OutputDebugString(L"\n");

        SafeRelease(&pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="17aef-120">La `LogMediaType` funzione utilizzata in questo esempio è elencata nell'argomento [codice di debug del tipo di supporto](media-type-debugging-code.md).</span><span class="sxs-lookup"><span data-stu-id="17aef-120">The `LogMediaType` function used in this example is listed in the topic [Media Type Debugging Code](media-type-debugging-code.md).</span></span>

<span data-ttu-id="17aef-121">Per impostare il formato di acquisizione:</span><span class="sxs-lookup"><span data-stu-id="17aef-121">To set the capture format:</span></span>

1.  <span data-ttu-id="17aef-122">Ottenere un puntatore all'interfaccia [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) , come illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="17aef-122">Get a pointer to the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface, as shown in the previous example.</span></span>
2.  <span data-ttu-id="17aef-123">Chiamare [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) per ottenere il formato desiderato, specificato dall'indice.</span><span class="sxs-lookup"><span data-stu-id="17aef-123">Call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get the desired format, specified by index.</span></span>
3.  <span data-ttu-id="17aef-124">Chiamare [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) per impostare il formato.</span><span class="sxs-lookup"><span data-stu-id="17aef-124">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the format.</span></span>

<span data-ttu-id="17aef-125">Se non si imposta il formato di acquisizione, il dispositivo utilizzerà il formato predefinito.</span><span class="sxs-lookup"><span data-stu-id="17aef-125">If you do not set the capture format, the device will use its default format.</span></span>

<span data-ttu-id="17aef-126">Nell'esempio seguente viene impostato il formato di acquisizione:</span><span class="sxs-lookup"><span data-stu-id="17aef-126">The following example sets the capture format:</span></span>


```C++
HRESULT SetDeviceFormat(IMFMediaSource *pSource, DWORD dwFormatIndex)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFStreamDescriptor *pSD = NULL;
    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pType = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL fSelected;
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetMediaTypeByIndex(dwFormatIndex, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->SetCurrentMediaType(pType);

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



<span data-ttu-id="17aef-127">L'ordine in cui vengono restituiti i formati dipende dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="17aef-127">The order in which formats are returned depends on the device.</span></span> <span data-ttu-id="17aef-128">Vengono in genere raggruppati per primo in base al tipo di compressione o allo spazio dei colori; e quindi dalla dimensione minima del fotogramma alla dimensione massima del fotogramma all'interno di ogni gruppo.</span><span class="sxs-lookup"><span data-stu-id="17aef-128">Typically, they are grouped first by compression type or color space; and then from smallest frame size to largest frame size within each group.</span></span>

<span data-ttu-id="17aef-129">La frequenza dei fotogrammi viene gestita in modo leggermente diverso rispetto agli altri attributi di formato.</span><span class="sxs-lookup"><span data-stu-id="17aef-129">The frame rate is handled slightly differently than the other format attributes.</span></span> <span data-ttu-id="17aef-130">Per altre informazioni, vedere [How to set the video Capture frame rate](how-to-set-the-video-capture-frame-rate.md).</span><span class="sxs-lookup"><span data-stu-id="17aef-130">For more information, see [How to Set the Video Capture Frame Rate](how-to-set-the-video-capture-frame-rate.md).</span></span>

> [!Note]  
> <span data-ttu-id="17aef-131">In alcuni dispositivi, l'elenco di formato conterrà una voce duplicata per ogni formato.</span><span class="sxs-lookup"><span data-stu-id="17aef-131">In some devices, the format list will contain a duplicate entry for each format.</span></span> <span data-ttu-id="17aef-132">Se, ad esempio, il dispositivo supporta 15 formati di acquisizione distinti, l'elenco conterrà 30 voci.</span><span class="sxs-lookup"><span data-stu-id="17aef-132">For example, if the device supports 15 distinct capture formats, the list will contain 30 entries.</span></span> <span data-ttu-id="17aef-133">All'interno di ogni coppia uno dei tipi di supporto avrà l'attributo [**MF \_ mt \_ am \_ \_ tipo di formato**](mf-mt-am-format-type-attribute.md) uguale a **Format \_ videoinfo** e l'altro avrà il **tipo di \_ formato MF mt \_ \_ \_ am** uguale a **Format \_ VideoInfo2**.</span><span class="sxs-lookup"><span data-stu-id="17aef-133">Within each pair, one of the media types will have the attribute [**MF\_MT\_AM\_FORMAT\_TYPE**](mf-mt-am-format-type-attribute.md) equal to **FORMAT\_VideoInfo**, and the other will have **MF\_MT\_AM\_FORMAT\_TYPE** equal to **FORMAT\_VideoInfo2**.</span></span> <span data-ttu-id="17aef-134">Questi due valori vengono definiti nel file di intestazione UUIDs. h. Il secondo tipo può inoltre contenere informazioni sui colori aggiuntive ([informazioni sui colori estese](extended-color-information.md)) o visualizzare un valore diverso per l'interlacciamento ([**\_ \_ \_ modalità di interpolazione MF mt**](mf-mt-interlace-mode-attribute.md)).</span><span class="sxs-lookup"><span data-stu-id="17aef-134">(These two values are defined in the header file uuids.h.) The second type might also contain additional color information ([Extended Color Information](extended-color-information.md)) or show a different value for interlacing ([**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md)).</span></span> <span data-ttu-id="17aef-135">Questi tipi duplicati sono disponibili per supportare le applicazioni DirectShow precedenti.</span><span class="sxs-lookup"><span data-stu-id="17aef-135">These duplicate types exist to support older DirectShow applications.</span></span> <span data-ttu-id="17aef-136">In un'applicazione Media Foundation è consigliabile ignorare il **formato \_ videoinfo** ogni volta che viene elencato un tipo **\_ VideoInfo2 di formato** duplicato.</span><span class="sxs-lookup"><span data-stu-id="17aef-136">In a Media Foundation application, you should ignore the **FORMAT\_VideoInfo** type whenever a duplicate **FORMAT\_VideoInfo2** type is listed.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="17aef-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="17aef-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17aef-138">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="17aef-138">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



