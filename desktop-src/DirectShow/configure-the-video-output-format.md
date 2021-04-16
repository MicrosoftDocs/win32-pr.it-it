---
description: Configurare il formato di output del video
ms.assetid: 1969072e-575e-49b4-88db-4c7e7a5a1c37
title: Configurare il formato di output del video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09ac64d7f43e6c39377277544867491a93a6f3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550487"
---
# <a name="configure-the-video-output-format"></a><span data-ttu-id="e7452-103">Configurare il formato di output del video</span><span class="sxs-lookup"><span data-stu-id="e7452-103">Configure the Video Output Format</span></span>

> [!Note]  
> <span data-ttu-id="e7452-104">La funzionalità descritta in questo argomento è deprecata.</span><span class="sxs-lookup"><span data-stu-id="e7452-104">The functionality described in this topic is deprecated.</span></span> <span data-ttu-id="e7452-105">Per configurare il formato di output di un dispositivo di acquisizione, un'applicazione deve usare la struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) restituita da [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) nel parametro *PMT* .</span><span class="sxs-lookup"><span data-stu-id="e7452-105">To configure a capture device's output format, an application should use the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure returned by [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) in the *pmt* parameter.</span></span>

 

<span data-ttu-id="e7452-106">Un dispositivo di acquisizione può supportare un intervallo di formati di output.</span><span class="sxs-lookup"><span data-stu-id="e7452-106">A capture device can support a range of output formats.</span></span> <span data-ttu-id="e7452-107">Ad esempio, un dispositivo potrebbe supportare RGB a 16 bit, RGB a 32 bit e YUYV.</span><span class="sxs-lookup"><span data-stu-id="e7452-107">For example, a device might support 16-bit RGB, 32-bit RGB, and YUYV.</span></span> <span data-ttu-id="e7452-108">All'interno di ognuno di questi formati, il dispositivo può supportare un intervallo di dimensioni dei frame.</span><span class="sxs-lookup"><span data-stu-id="e7452-108">Within each of these formats, the device can support a range of frame sizes.</span></span>

<span data-ttu-id="e7452-109">In un dispositivo WDM, l'interfaccia [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) viene utilizzata per segnalare i formati supportati dal dispositivo e per impostare il formato.</span><span class="sxs-lookup"><span data-stu-id="e7452-109">In a WDM device, the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface is used to report which formats the device supports, and to set the format.</span></span> <span data-ttu-id="e7452-110">Per i dispositivi VFW legacy, utilizzare la finestra di dialogo VFW formato video, come descritto in [visualizzare le finestre di dialogo di acquisizione VFW](display-vfw-capture-dialog-boxes.md). L'interfaccia **IAMStreamConfig** viene esposta nel pin di acquisizione del filtro di acquisizione, nel pin di anteprima o in entrambi.</span><span class="sxs-lookup"><span data-stu-id="e7452-110">(For legacy VFW devices, use the Video Format VFW dialog box, as described in [Display VFW Capture Dialog Boxes](display-vfw-capture-dialog-boxes.md).) The **IAMStreamConfig** interface is exposed on the capture filter's capture pin, preview pin, or both.</span></span> <span data-ttu-id="e7452-111">Usare il metodo [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) per ottenere il puntatore di interfaccia:</span><span class="sxs-lookup"><span data-stu-id="e7452-111">Use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to get the interface pointer:</span></span>


```C++
IAMStreamConfig *pConfig = NULL;
hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, // Preview pin.
    0,    // Any media type.
    pCap, // Pointer to the capture filter.
    IID_IAMStreamConfig, (void**)&pConfig);
```



<span data-ttu-id="e7452-112">Il dispositivo dispone di un elenco di tipi di supporto supportati.</span><span class="sxs-lookup"><span data-stu-id="e7452-112">The device has a list of media types that it supports.</span></span> <span data-ttu-id="e7452-113">Per ogni tipo di supporto, il dispositivo fornisce anche un set di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e7452-113">For each media type, the device also provides a set of capabilities.</span></span> <span data-ttu-id="e7452-114">Questi includono l'intervallo di dimensioni dei frame disponibili per tale formato, il modo in cui il dispositivo può allungare o compattare l'immagine e l'intervallo di frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="e7452-114">These include the range of frame sizes that are available for that format, how well the device can stretch or shrink the image, and the range of frame rates.</span></span>

<span data-ttu-id="e7452-115">Per ottenere il numero di tipi di supporto, chiamare il metodo [**IAMStreamConfig:: GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="e7452-115">To get the number of media types, call the [**IAMStreamConfig::GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) method.</span></span> <span data-ttu-id="e7452-116">Il metodo restituisce due valori:</span><span class="sxs-lookup"><span data-stu-id="e7452-116">The method returns two values:</span></span>

-   <span data-ttu-id="e7452-117">Numero di tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="e7452-117">The number of media types.</span></span>
-   <span data-ttu-id="e7452-118">Dimensioni della struttura che contengono le informazioni sulle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e7452-118">The size of the structure that holds the capabilities information.</span></span>

<span data-ttu-id="e7452-119">Il valore delle dimensioni è necessario perché l'interfaccia [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) viene usata sia per audio che per video e può essere estesa ad altri tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="e7452-119">The size value is necessary because the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface is used for both audio and video (and could be extended to other media types).</span></span> <span data-ttu-id="e7452-120">Per i video, le funzionalità vengono descritte usando la struttura [**dei \_ \_ \_ tappi di configurazione del flusso video**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) , mentre l'audio usa la struttura dei [**\_ \_ \_ limiti di configurazione del flusso audio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="e7452-120">For video, the capabilities are described using the [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure, while audio uses the [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structure.</span></span>

<span data-ttu-id="e7452-121">Per enumerare i tipi di supporto, chiamare il metodo [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) con un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="e7452-121">To enumerate the media types, call the [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method with a zero-based index.</span></span> <span data-ttu-id="e7452-122">Il metodo **GetStreamCaps** restituisce un tipo di supporto e la struttura di capacità corrispondente:</span><span class="sxs-lookup"><span data-stu-id="e7452-122">The **GetStreamCaps** method returns a media type and the corresponding capability structure:</span></span>


```C++
int iCount = 0, iSize = 0;
hr = pConfig->GetNumberOfCapabilities(&iCount, &iSize);

// Check the size to make sure we pass in the correct structure.
if (iSize == sizeof(VIDEO_STREAM_CONFIG_CAPS))
{
    // Use the video capabilities structure.

    for (int iFormat = 0; iFormat < iCount; iFormat++)
    {
        VIDEO_STREAM_CONFIG_CAPS scc;
        AM_MEDIA_TYPE *pmtConfig;
        hr = pConfig->GetStreamCaps(iFormat, &pmtConfig, (BYTE*)&scc);
        if (SUCCEEDED(hr))
        {
            /* Examine the format, and possibly use it. */

            // Delete the media type when you are done.
            DeleteMediaType(pmtConfig);
        }
}
```



<span data-ttu-id="e7452-123">Si noti come vengono allocate le strutture per il metodo [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="e7452-123">Note how the structures are allocated for the [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="e7452-124">Il metodo alloca la struttura del tipo di supporto, mentre il chiamante alloca la struttura delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e7452-124">The method allocates the media type structure, whereas the caller allocates the capabilities structure.</span></span> <span data-ttu-id="e7452-125">Assegnare la struttura delle funzionalità a un puntatore di matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="e7452-125">Coerce the capabilities structure to a byte array pointer.</span></span> <span data-ttu-id="e7452-126">Al termine del tipo di supporto, eliminare la struttura del [**\_ \_ tipo**](/windows/win32/api/strmif/ns-strmif-am_media_type) di supporto am insieme al blocco di formato del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e7452-126">After you are done with the media type, delete the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, along with the media type's format block.</span></span>

<span data-ttu-id="e7452-127">È possibile configurare il dispositivo in modo che usi un formato restituito nel metodo [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="e7452-127">You can configure the device to use a format returned in the [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="e7452-128">È sufficiente chiamare [**IAMStreamConfig:: Seformatt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) con il tipo di supporto:</span><span class="sxs-lookup"><span data-stu-id="e7452-128">Simply call [**IAMStreamConfig::SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) with the media type:</span></span>


```C++
hr = pConfig->SetFormat(pmtConfig);
```



<span data-ttu-id="e7452-129">Se il PIN non è connesso, tenterà di usare questo formato quando si connette.</span><span class="sxs-lookup"><span data-stu-id="e7452-129">If the pin is not connected, it will attempt to use this format when it does connect.</span></span> <span data-ttu-id="e7452-130">Se il PIN è già connesso, tenta di riconnettersi usando il nuovo formato.</span><span class="sxs-lookup"><span data-stu-id="e7452-130">If the pin is already connected, it attempts to reconnect using the new format.</span></span> <span data-ttu-id="e7452-131">In entrambi i casi, è possibile che il filtro downstream rifiuterà il formato.</span><span class="sxs-lookup"><span data-stu-id="e7452-131">In either case, it is possible that the downstream filter will reject the format.</span></span>

<span data-ttu-id="e7452-132">È anche possibile modificare il tipo di supporto prima di passarlo al metodo [**Seformatt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) .</span><span class="sxs-lookup"><span data-stu-id="e7452-132">You can also modify the media type before passing it to the [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method.</span></span> <span data-ttu-id="e7452-133">Qui entra in gioco la struttura di [**\_ Caps di \_ configurazione \_ del flusso video**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="e7452-133">This is where the [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure comes in.</span></span> <span data-ttu-id="e7452-134">Vengono descritti tutti i modi validi per modificare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e7452-134">It describes all of the valid ways to change the media type.</span></span> <span data-ttu-id="e7452-135">Per usare queste informazioni, è necessario comprendere i dettagli del tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="e7452-135">To use this information, you must understand the details of that particular media type.</span></span>

<span data-ttu-id="e7452-136">Si supponga, ad esempio, che [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) restituisca un formato RGB a 24 bit, con una dimensione del frame di 320 x 240 pixel.</span><span class="sxs-lookup"><span data-stu-id="e7452-136">For example, suppose that [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) returns a 24-bit RGB format, with a frame size of 320 x 240 pixels.</span></span> <span data-ttu-id="e7452-137">È possibile ottenere queste informazioni esaminando il tipo principale, il sottotipo e il blocco di formato del tipo di supporto:</span><span class="sxs-lookup"><span data-stu-id="e7452-137">You can get this information by examining the major type, subtype, and format block of the media type:</span></span>


```C++
if ((pmtConfig.majortype == MEDIATYPE_Video) &&
    (pmtConfig.subtype == MEDIASUBTYPE_RGB24) &&
    (pmtConfig.formattype == FORMAT_VideoInfo) &&
    (pmtConfig.cbFormat >= sizeof (VIDEOINFOHEADER)) &&
    (pmtConfig.pbFormat != NULL))
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)pmtConfig.pbFormat;
    // pVih contains the detailed format information.
    LONG lWidth = pVih->bmiHeader.biWidth;
    LONG lHeight = pVih->bmiHeader.biHeight;
}
```



<span data-ttu-id="e7452-138">La struttura di [**\_ Caps di \_ configurazione \_ del flusso video**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) fornisce la larghezza e l'altezza minime e massime che possono essere usate per questo tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e7452-138">The [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure gives the minimum and maximum width and height that can be used for this media type.</span></span> <span data-ttu-id="e7452-139">Fornisce anche le dimensioni "Step", che definiscono gli incrementi in base ai quali è possibile modificare la larghezza o l'altezza.</span><span class="sxs-lookup"><span data-stu-id="e7452-139">It also gives you the "step" size, which defines the increments by which you can adjust the width or height.</span></span> <span data-ttu-id="e7452-140">Ad esempio, il dispositivo potrebbe restituire quanto segue:</span><span class="sxs-lookup"><span data-stu-id="e7452-140">For example, the device might return the following:</span></span>

-   <span data-ttu-id="e7452-141">MinOutputSize: 160 x 120</span><span class="sxs-lookup"><span data-stu-id="e7452-141">MinOutputSize: 160 x 120</span></span>
-   <span data-ttu-id="e7452-142">MaxOutputSize: 320 x 240</span><span class="sxs-lookup"><span data-stu-id="e7452-142">MaxOutputSize: 320 x 240</span></span>
-   <span data-ttu-id="e7452-143">OutputGranularityX: 8 pixel (dimensioni del passaggio orizzontale)</span><span class="sxs-lookup"><span data-stu-id="e7452-143">OutputGranularityX: 8 pixels (horizontal step size)</span></span>
-   <span data-ttu-id="e7452-144">OutputGranularityY: 8 pixel (dimensioni del passaggio verticale)</span><span class="sxs-lookup"><span data-stu-id="e7452-144">OutputGranularityY: 8 pixels (vertical step size)</span></span>

<span data-ttu-id="e7452-145">Dato questi numeri, è possibile impostare la larghezza su qualsiasi elemento nell'intervallo (160, 168, 176,... 304, 312, 320) e l'altezza di qualsiasi elemento compreso nell'intervallo (120, 128, 136,... 104, 112, 120).</span><span class="sxs-lookup"><span data-stu-id="e7452-145">Given these numbers, you could set the width to anything in the range (160, 168, 176, ... 304, 312, 320) and the height to anything in the range (120, 128, 136, ... 104, 112, 120).</span></span> <span data-ttu-id="e7452-146">La figura seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="e7452-146">The following diagram illustrates this process.</span></span>

![dimensioni del formato video](images/strmcap3.png)

<span data-ttu-id="e7452-148">Per impostare una nuova dimensione del fotogramma, modificare direttamente la struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) restituita in [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):</span><span class="sxs-lookup"><span data-stu-id="e7452-148">To set a new frame size, directly modify the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure returned in [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):</span></span>


```C++
pVih->bmiHeader.biWidth = 160;
pVih->bmiHeader.biHeight = 120;
pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader);
```



<span data-ttu-id="e7452-149">Passare quindi il tipo di supporto al metodo [**Seformatt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) , come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e7452-149">Then pass the media type to the [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method, as described previously.</span></span>

<span data-ttu-id="e7452-150">I membri di **MinFrameInterval** e **MaxFrameInterval** dei [**limiti di \_ \_ configurazione \_ del flusso video**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) sono la lunghezza minima e massima di ogni fotogramma video, che è possibile convertire in frequenza dei fotogrammi come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="e7452-150">The **MinFrameInterval** and **MaxFrameInterval** members of [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) are the minimum and maximum length of each video frame, which you can translate into frame rates as follows:</span></span>

`frames per second = 10,000,000 / frame duration`

<span data-ttu-id="e7452-151">Per richiedere una frequenza dei fotogrammi specifica, modificare il valore di **AvgTimePerFrame** nella struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) nel tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e7452-151">To request a particular frame rate, modify the value of **AvgTimePerFrame** in the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure in the media type.</span></span> <span data-ttu-id="e7452-152">Il dispositivo potrebbe non supportare ogni possibile valore tra il minimo e il massimo, quindi il driver utilizzerà il valore più vicino possibile.</span><span class="sxs-lookup"><span data-stu-id="e7452-152">The device may not support every possible value between the minimum and maximum, so the driver will use the closest value that it can.</span></span> <span data-ttu-id="e7452-153">Per visualizzare il valore effettivamente usato dal driver, chiamare [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) dopo la chiamata a [**seformatt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).</span><span class="sxs-lookup"><span data-stu-id="e7452-153">To see what value the driver actually used, call [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) after you call [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).</span></span>

<span data-ttu-id="e7452-154">Alcuni driver possono segnalare **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) per il valore di **MaxFrameInterval**, che in effetti significa che non esiste una durata massima.</span><span class="sxs-lookup"><span data-stu-id="e7452-154">Some drivers may report **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) for the value of **MaxFrameInterval**, which in effect means there is no maximum duration.</span></span> <span data-ttu-id="e7452-155">Tuttavia, potrebbe essere necessario applicare una frequenza minima dei fotogrammi nell'applicazione, ad esempio 1 fps.</span><span class="sxs-lookup"><span data-stu-id="e7452-155">However, you might want to enforce a minimum frame rate in your application, such as 1 fps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7452-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7452-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7452-157">Informazioni sui tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="e7452-157">About Media Types</span></span>](about-media-types.md)
</dt> <dt>

[<span data-ttu-id="e7452-158">Configurazione di un dispositivo di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="e7452-158">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



