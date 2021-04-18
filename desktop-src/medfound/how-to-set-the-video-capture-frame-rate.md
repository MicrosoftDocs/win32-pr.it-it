---
description: Un dispositivo di acquisizione video potrebbe supportare un intervallo di frequenza dei fotogrammi.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Come impostare la frequenza dei fotogrammi di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e105965f5449cb7f4cab59f49410ecfb40221c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308755"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a><span data-ttu-id="2748e-103">Come impostare la frequenza dei fotogrammi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="2748e-103">How to Set the Video Capture Frame Rate</span></span>

<span data-ttu-id="2748e-104">Un dispositivo di acquisizione video potrebbe supportare un intervallo di frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="2748e-104">A video capture device might support a range of frame rates.</span></span> <span data-ttu-id="2748e-105">Se queste informazioni sono disponibili, le frequenze dei fotogrammi minime e massime vengono archiviate come attributi di tipo multimediale:</span><span class="sxs-lookup"><span data-stu-id="2748e-105">If this information is available, the minimum and maximum frame rates are stored as media type attributes:</span></span>



| <span data-ttu-id="2748e-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="2748e-106">Attribute</span></span>                                                         | <span data-ttu-id="2748e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2748e-107">Description</span></span>         |
|-------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="2748e-108">\_intervallo di \_ frequenza frame MF mt \_ \_ \_ Max</span><span class="sxs-lookup"><span data-stu-id="2748e-108">MF\_MT\_FRAME\_RATE\_RANGE\_MAX</span></span>](mf-mt-frame-rate-range-max.md) | <span data-ttu-id="2748e-109">Frequenza massima di fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="2748e-109">Maximum frame rate.</span></span> |
| [<span data-ttu-id="2748e-110">\_intervallo di \_ \_ frequenza frame \_ MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="2748e-110">MF\_MT\_FRAME\_RATE\_RANGE\_MIN</span></span>](mf-mt-frame-rate-range-min.md) | <span data-ttu-id="2748e-111">Frequenza minima del fotogramma.</span><span class="sxs-lookup"><span data-stu-id="2748e-111">Minimum frame rate.</span></span> |



 

<span data-ttu-id="2748e-112">L'intervallo può variare a seconda del formato di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="2748e-112">The range can vary depending on the capture format.</span></span> <span data-ttu-id="2748e-113">Ad esempio, in dimensioni di frame più grandi, la frequenza massima dei frame potrebbe essere ridotta.</span><span class="sxs-lookup"><span data-stu-id="2748e-113">For example, at larger frame sizes, the maximum frame rate might be reduced.</span></span>

<span data-ttu-id="2748e-114">Per impostare la frequenza dei fotogrammi:</span><span class="sxs-lookup"><span data-stu-id="2748e-114">To set the frame rate:</span></span>

1.  <span data-ttu-id="2748e-115">Creare l'origine multimediale per il dispositivo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="2748e-115">Create the media source for the capture device.</span></span> <span data-ttu-id="2748e-116">Vedere [enumerazione dei dispositivi di acquisizione video](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="2748e-116">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="2748e-117">Chiamare [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) sull'origine del supporto per ottenere il descrittore della presentazione.</span><span class="sxs-lookup"><span data-stu-id="2748e-117">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="2748e-118">Chiamare [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) per ottenere il descrittore del flusso per il flusso video.</span><span class="sxs-lookup"><span data-stu-id="2748e-118">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="2748e-119">Chiamare [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) sul descrittore del flusso.</span><span class="sxs-lookup"><span data-stu-id="2748e-119">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="2748e-120">Enumerare i formati di acquisizione, come descritto in [come impostare il formato di acquisizione video](how-to-set-the-video-capture-format.md).</span><span class="sxs-lookup"><span data-stu-id="2748e-120">Enumerate the capture formats, as described in [How to Set the Video Capture Format](how-to-set-the-video-capture-format.md).</span></span>
6.  <span data-ttu-id="2748e-121">Selezionare il formato di output desiderato nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="2748e-121">Select the desired output format from the list.</span></span>
7.  <span data-ttu-id="2748e-122">Eseguire una query sul tipo di supporto per gli attributi [MF \_ mt \_ frame \_ rate \_ \_ Max](mf-mt-frame-rate-range-max.md) e [MF \_ mt \_ frame \_ rate \_ Range \_ min](mf-mt-frame-rate-range-min.md) .</span><span class="sxs-lookup"><span data-stu-id="2748e-122">Query the media type for the [MF\_MT\_FRAME\_RATE\_RANGE\_MAX](mf-mt-frame-rate-range-max.md) and [MF\_MT\_FRAME\_RATE\_RANGE\_MIN](mf-mt-frame-rate-range-min.md) attributes.</span></span> <span data-ttu-id="2748e-123">Questi valori forniscono la gamma di frequenze dei frame supportate.</span><span class="sxs-lookup"><span data-stu-id="2748e-123">This values give the range of supported frame rates.</span></span> <span data-ttu-id="2748e-124">Il dispositivo potrebbe supportare altre frequenze dei fotogrammi all'interno di questo intervallo.</span><span class="sxs-lookup"><span data-stu-id="2748e-124">The device might support other frame rates within this range.</span></span>
8.  <span data-ttu-id="2748e-125">Impostare l'attributo [**MF \_ mt \_ frame**](mf-mt-frame-rate-attribute.md) sul tipo di supporto per specificare la frequenza dei fotogrammi desiderata.</span><span class="sxs-lookup"><span data-stu-id="2748e-125">Set the [**MF\_MT\_FRAME**](mf-mt-frame-rate-attribute.md) attribute on the media type to specify the desired frame rate.</span></span>
9.  <span data-ttu-id="2748e-126">Chiamare [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) con il tipo di supporto modificato.</span><span class="sxs-lookup"><span data-stu-id="2748e-126">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) with the modified media type.</span></span>

<span data-ttu-id="2748e-127">Nell'esempio seguente viene impostata la frequenza dei fotogrammi uguale alla frequenza massima di frame supportata dal dispositivo:</span><span class="sxs-lookup"><span data-stu-id="2748e-127">The following example sets the frame rate equal to the maximum frame rate that the device supports:</span></span>


```C++
HRESULT SetMaxFrameRate(IMFMediaSource *pSource, DWORD dwTypeIndex)
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
    hr = pPD->GetStreamDescriptorByIndex(dwTypeIndex, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetCurrentMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the maximum frame rate for the selected capture format.

    // Note: To get the minimum frame rate, use the 
    // MF_MT_FRAME_RATE_RANGE_MIN attribute instead.

    PROPVARIANT var;
    if (SUCCEEDED(pType->GetItem(MF_MT_FRAME_RATE_RANGE_MAX, &var)))
    {
        hr = pType->SetItem(MF_MT_FRAME_RATE, var);

        PropVariantClear(&var);

        if (FAILED(hr))
        {
            goto done;
        }

        hr = pHandler->SetCurrentMediaType(pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2748e-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2748e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2748e-129">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="2748e-129">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



