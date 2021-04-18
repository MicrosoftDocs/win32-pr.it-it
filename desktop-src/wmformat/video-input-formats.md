---
title: Formati di input video
description: Formati di input video
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- Windows Media Format SDK, formati di input video
- ASF (Advanced Systems Format), formati di input video
- ASF (Advanced Systems Format), formati di input video
- formati di input video
- Windows Media Format SDK, formati video
- ASF (Advanced Systems Format), formati video
- ASF (Advanced Systems Format), formati video
- formati video
- Windows Media Video 9 codec, formati di input video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299525"
---
# <a name="video-input-formats"></a><span data-ttu-id="ae16b-112">Formati di input video</span><span class="sxs-lookup"><span data-stu-id="ae16b-112">Video Input Formats</span></span>

<span data-ttu-id="ae16b-113">Il writer accetta i formati video seguenti come input da comprimere usando il codec Windows Media Video 9:</span><span class="sxs-lookup"><span data-stu-id="ae16b-113">The writer accepts the following video formats as input to be compressed using the Windows Media Video 9 codec:</span></span>

-   <span data-ttu-id="ae16b-114">\_IYUV WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ae16b-114">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="ae16b-115">\_I420 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ae16b-115">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="ae16b-116">\_YV12 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ae16b-116">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="ae16b-117">\_YUY2 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ae16b-117">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="ae16b-118">\_UYVY WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ae16b-118">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="ae16b-119">\_YVYU WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ae16b-119">WMMEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="ae16b-120">\_YVU9 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ae16b-120">WMMEDIASUBTYPE\_YVU9</span></span>
-   <span data-ttu-id="ae16b-121">\_Rgb32 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ae16b-121">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="ae16b-122">\_RGB24 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ae16b-122">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="ae16b-123">\_RGB565 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ae16b-123">WMMEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="ae16b-124">\_RGB555 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ae16b-124">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="ae16b-125">\_RGB8 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="ae16b-125">WMMEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="ae16b-126">Usare sempre [**IWMWriter:: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) e [**IWMWriter:: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) per enumerare i formati di input disponibili e ottenere l'oggetto proprietà supporto di input per il formato desiderato.</span><span class="sxs-lookup"><span data-stu-id="ae16b-126">You should always use [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) and [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) to enumerate the available input formats and to obtain the input media properties object for the desired format.</span></span> <span data-ttu-id="ae16b-127">È necessario modificare gli oggetti proprietà del supporto di input video per riflettere le dimensioni del frame e la frequenza dei fotogrammi del supporto di input.</span><span class="sxs-lookup"><span data-stu-id="ae16b-127">Video input media properties objects must be changed to reflect the frame size and frame rate of your input media.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae16b-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ae16b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae16b-129">**Identificatori del tipo di supporto**</span><span class="sxs-lookup"><span data-stu-id="ae16b-129">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="ae16b-130">**Tipi di supporto**</span><span class="sxs-lookup"><span data-stu-id="ae16b-130">**Media Types**</span></span>](media-types.md)
</dt> </dl>

 

 




