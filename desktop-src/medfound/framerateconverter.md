---
description: Modifica la frequenza dei fotogrammi di un flusso video.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Convertitore frequenza frame DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6197c29e9e753db6f327aa8b2797ba04131448d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749231"
---
# <a name="frame-rate-converter-dsp"></a><span data-ttu-id="023e3-103">Convertitore frequenza frame DSP</span><span class="sxs-lookup"><span data-stu-id="023e3-103">Frame Rate Converter DSP</span></span>

<span data-ttu-id="023e3-104">Modifica la frequenza dei fotogrammi di un flusso video.</span><span class="sxs-lookup"><span data-stu-id="023e3-104">Changes the frame rate of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="023e3-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="023e3-105">CLSID</span></span>

<span data-ttu-id="023e3-106">\_CFRAMERATECONVERTDMO CLSID</span><span class="sxs-lookup"><span data-stu-id="023e3-106">CLSID\_CFrameRateConvertDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="023e3-107">Interfacce</span><span class="sxs-lookup"><span data-stu-id="023e3-107">Interfaces</span></span>

-   <span data-ttu-id="023e3-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="023e3-108">**IMediaObject**</span></span>
-   <span data-ttu-id="023e3-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="023e3-109">**IMFTransform**</span></span>
-   <span data-ttu-id="023e3-110">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="023e3-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="023e3-111">Formati</span><span class="sxs-lookup"><span data-stu-id="023e3-111">Formats</span></span>

-   <span data-ttu-id="023e3-112">ARGB 32</span><span class="sxs-lookup"><span data-stu-id="023e3-112">ARGB 32</span></span>
-   <span data-ttu-id="023e3-113">RGB 24</span><span class="sxs-lookup"><span data-stu-id="023e3-113">RGB 24</span></span>
-   <span data-ttu-id="023e3-114">RGB 32</span><span class="sxs-lookup"><span data-stu-id="023e3-114">RGB 32</span></span>
-   <span data-ttu-id="023e3-115">RGB 555</span><span class="sxs-lookup"><span data-stu-id="023e3-115">RGB 555</span></span>
-   <span data-ttu-id="023e3-116">RGB 565</span><span class="sxs-lookup"><span data-stu-id="023e3-116">RGB 565</span></span>
-   <span data-ttu-id="023e3-117">AYUV</span><span class="sxs-lookup"><span data-stu-id="023e3-117">AYUV</span></span>
-   <span data-ttu-id="023e3-118">IYUV</span><span class="sxs-lookup"><span data-stu-id="023e3-118">IYUV</span></span>
-   <span data-ttu-id="023e3-119">UYVY</span><span class="sxs-lookup"><span data-stu-id="023e3-119">UYVY</span></span>
-   <span data-ttu-id="023e3-120">Y211</span><span class="sxs-lookup"><span data-stu-id="023e3-120">Y211</span></span>
-   <span data-ttu-id="023e3-121">Y411</span><span class="sxs-lookup"><span data-stu-id="023e3-121">Y411</span></span>
-   <span data-ttu-id="023e3-122">Y41P</span><span class="sxs-lookup"><span data-stu-id="023e3-122">Y41P</span></span>
-   <span data-ttu-id="023e3-123">YUY2</span><span class="sxs-lookup"><span data-stu-id="023e3-123">YUY2</span></span>
-   <span data-ttu-id="023e3-124">YUYV</span><span class="sxs-lookup"><span data-stu-id="023e3-124">YUYV</span></span>
-   <span data-ttu-id="023e3-125">YV12</span><span class="sxs-lookup"><span data-stu-id="023e3-125">YV12</span></span>
-   <span data-ttu-id="023e3-126">YVYU</span><span class="sxs-lookup"><span data-stu-id="023e3-126">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="023e3-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="023e3-127">Properties</span></span>

-   [<span data-ttu-id="023e3-128">MFPKEY \_ conv \_ INPUTFRAMERATE</span><span class="sxs-lookup"><span data-stu-id="023e3-128">MFPKEY\_CONV\_INPUTFRAMERATE</span></span>](mfpkey-conv-inputframerate.md)
-   [<span data-ttu-id="023e3-129">MFPKEY \_ conv \_ OUTPUTFRAMERATE</span><span class="sxs-lookup"><span data-stu-id="023e3-129">MFPKEY\_CONV\_OUTPUTFRAMERATE</span></span>](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a><span data-ttu-id="023e3-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="023e3-130">Remarks</span></span>

<span data-ttu-id="023e3-131">Questo DSP modifica la frequenza dei fotogrammi ripetendo o eliminando i frame.</span><span class="sxs-lookup"><span data-stu-id="023e3-131">This DSP changes the frame rate by repeating or dropping frames.</span></span>

<span data-ttu-id="023e3-132">Per impostazione predefinita, il DSP ottiene le frequenze dei fotogrammi dai tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="023e3-132">By default, the DSP gets the frame rates from the media types.</span></span> <span data-ttu-id="023e3-133">Facoltativamente, è possibile specificare le frequenze dei fotogrammi impostando \_ le \_ Proprietà MFPKEY CONV INPUTFRAMERATE e MFPKEY \_ conv \_ OUTPUTFRAMERATE.</span><span class="sxs-lookup"><span data-stu-id="023e3-133">Optionally, you can specify the frame rates by setting the MFPKEY\_CONV\_INPUTFRAMERATE and MFPKEY\_CONV\_OUTPUTFRAMERATE properties.</span></span> <span data-ttu-id="023e3-134">Questi valori eseguono l'override della frequenza dei fotogrammi specificata nel tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="023e3-134">These values override the frame rate given in the media type.</span></span> <span data-ttu-id="023e3-135">Tuttavia, se si usa questo DSP all'interno della pipeline di Media Foundation, è consigliabile non impostare queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="023e3-135">However, if you are using this DSP within the Media Foundation pipeline, you should not set these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="023e3-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="023e3-136">Requirements</span></span>



| <span data-ttu-id="023e3-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="023e3-137">Requirement</span></span> | <span data-ttu-id="023e3-138">Valore</span><span class="sxs-lookup"><span data-stu-id="023e3-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="023e3-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="023e3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="023e3-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="023e3-140">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="023e3-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="023e3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="023e3-142">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="023e3-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="023e3-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="023e3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="023e3-144"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="023e3-144"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="023e3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="023e3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="023e3-146"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="023e3-146"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="023e3-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="023e3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="023e3-148">Processori di segnale digitale</span><span class="sxs-lookup"><span data-stu-id="023e3-148">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




