---
description: Abilita l'elaborazione video avanzata da parte del lettore di origine, tra cui conversione dello spazio colore, deinterlacciamento, ridimensionamento video e conversione della frequenza dei fotogrammi.
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: Attributo MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6978239c5c1c466c78a310b38b5d10bd41f9e004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525998"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a><span data-ttu-id="78009-103">MF \_ source \_ Reader \_ Abilita \_ l' \_ attributo Advanced video \_ Processing</span><span class="sxs-lookup"><span data-stu-id="78009-103">MF\_SOURCE\_READER\_ENABLE\_ADVANCED\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="78009-104">Abilita l'elaborazione video avanzata da parte del [lettore di origine](source-reader.md), tra cui conversione dello spazio colore, deinterlacciamento, ridimensionamento video e conversione della frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="78009-104">Enables advanced video processing by the [Source Reader](source-reader.md), including color space conversion, deinterlacing, video resizing, and frame-rate conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="78009-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="78009-105">Data type</span></span>

<span data-ttu-id="78009-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78009-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="78009-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="78009-107">Remarks</span></span>

<span data-ttu-id="78009-108">Se questo attributo è **true**, il lettore di origine può inserire un processore video nella pipeline di elaborazione, che consente i tipi di conversione di formato seguenti:</span><span class="sxs-lookup"><span data-stu-id="78009-108">If this attribute is **TRUE**, the Source Reader can insert a video processor into the processing pipeline, which enables the following types of format conversion:</span></span>

-   <span data-ttu-id="78009-109">Conversione dello spazio colore (YUV a RGB-32)</span><span class="sxs-lookup"><span data-stu-id="78009-109">Color space conversion (YUV to RGB-32)</span></span>
-   <span data-ttu-id="78009-110">Deinterlacciamento</span><span class="sxs-lookup"><span data-stu-id="78009-110">Deinterlacing</span></span>
-   <span data-ttu-id="78009-111">Ridimensionamento video</span><span class="sxs-lookup"><span data-stu-id="78009-111">Video resizing</span></span>
-   <span data-ttu-id="78009-112">Conversione della frequenza di frame</span><span class="sxs-lookup"><span data-stu-id="78009-112">Frame-rate conversion</span></span>

<span data-ttu-id="78009-113">Se questo attributo è **true**, è necessario che l'attributo [MF \_ ReadWrite \_ Disable \_ Converters](mf-readwrite-disable-converters.md) sia **impostato su false**.</span><span class="sxs-lookup"><span data-stu-id="78009-113">If this attribute is **TRUE**, the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute must be **FALSE**.</span></span>

<span data-ttu-id="78009-114">Il lettore di origine cerca i processori video registrati nella categoria **MFT \_ categoria \_ \_ processore video** , inclusi MFTS registrati per il processo locale.</span><span class="sxs-lookup"><span data-stu-id="78009-114">The Source Reader looks for video processors that are registered in the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category, including MFTs that are registered for the local process.</span></span> <span data-ttu-id="78009-115">Per ulteriori informazioni sulla registrazione locale di MFTs, vedere [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) . Il lettore di origine utilizza il processore transcodificatore video (XVP) se non viene trovato altro elaboratore video appropriato.</span><span class="sxs-lookup"><span data-stu-id="78009-115">(See [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) for more information about local registration of MFTs.) The Source Reader uses the Transcode Video Processor (XVP) if no other suitable video processor is found.</span></span>

<span data-ttu-id="78009-116">L'applicazione specifica il tipo di output desiderato chiamando [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="78009-116">The application specifies the desired output type by calling [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span> <span data-ttu-id="78009-117">Quando il lettore di origine configura il processore video, tenta di trovare la corrispondenza con gli attributi seguenti del tipo di output:</span><span class="sxs-lookup"><span data-stu-id="78009-117">When the Source Reader configures the video processor, it attempts to match the following attributes of the output type:</span></span>

-   <span data-ttu-id="78009-118">Frequenza fotogrammi[( \_ \_ \_ frequenza del frame MF mt](mf-mt-frame-rate-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="78009-118">Frame rate ([MF\_MT\_FRAME\_RATE](mf-mt-frame-rate-attribute.md))</span></span>
-   <span data-ttu-id="78009-119">Dimensioni frame ([ \_ dimensioni del \_ frame \_ MF mt](mf-mt-frame-size-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="78009-119">Frame size ([MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md))</span></span>
-   <span data-ttu-id="78009-120">Modalità interlacciata ([ \_ \_ \_ modalità di interpolazione MF mt](mf-mt-interlace-mode-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="78009-120">Interlace mode ([MF\_MT\_INTERLACE\_MODE](mf-mt-interlace-mode-attribute.md))</span></span>
-   <span data-ttu-id="78009-121">Proporzioni pixel (proporzioni del[ \_ pixel MF mt \_ \_ \_ ](mf-mt-pixel-aspect-ratio-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="78009-121">Pixel aspect ratio ([MF\_MT\_PIXEL\_ASPECT\_RATIO](mf-mt-pixel-aspect-ratio-attribute.md))</span></span>
-   <span data-ttu-id="78009-122">Sottotipo ([ \_ \_ sottotipo MF mt](mf-mt-subtype-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="78009-122">Subtype ([MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md))</span></span>

<span data-ttu-id="78009-123">Questo attributo è simile all'attributo [di \_ \_ \_ \_ \_ elaborazione video dell'abilitazione del lettore di origine MF](mf-source-reader-enable-video-processing.md) , ma offre i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="78009-123">This attribute is similar to the [MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING](mf-source-reader-enable-video-processing.md) attribute, but offers the following advantages:</span></span>

-   <span data-ttu-id="78009-124">È supportata un'ampia gamma di conversioni di formato.</span><span class="sxs-lookup"><span data-stu-id="78009-124">A greater range of format conversions is supported.</span></span>
-   <span data-ttu-id="78009-125">Le applicazioni possono registrare i propri convertitori.</span><span class="sxs-lookup"><span data-stu-id="78009-125">Applications can register their own converters.</span></span>
-   <span data-ttu-id="78009-126">Alcune conversioni possono essere eseguite nell'hardware usando la GPU.</span><span class="sxs-lookup"><span data-stu-id="78009-126">Some conversions can be performed in hardware using the GPU.</span></span>

## <a name="requirements"></a><span data-ttu-id="78009-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78009-127">Requirements</span></span>



| <span data-ttu-id="78009-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="78009-128">Requirement</span></span> | <span data-ttu-id="78009-129">Valore</span><span class="sxs-lookup"><span data-stu-id="78009-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="78009-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78009-130">Minimum supported client</span></span><br/> | <span data-ttu-id="78009-131">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="78009-131">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="78009-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78009-132">Minimum supported server</span></span><br/> | <span data-ttu-id="78009-133">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="78009-133">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="78009-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78009-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="78009-135"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="78009-135"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78009-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78009-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78009-137">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="78009-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="78009-138">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="78009-138">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="78009-139">Attributi lettore di origine</span><span class="sxs-lookup"><span data-stu-id="78009-139">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




