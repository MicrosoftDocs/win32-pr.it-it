---
description: La \_ struttura di caps di configurazione del flusso video TAPI \_ \_ \_ è contenuta nella \_ struttura di caps di configurazione del flusso TAPI \_ \_ quando il membro CapsType è impostato sul membro VideoCap dell'Unione StreamConfigCapsType.
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: Struttura TAPI_VIDEO_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525a35cb7c7332aa4e80fe8d5e2436e75e2d5c08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331775"
---
# <a name="tapi_video_stream_config_caps-structure"></a><span data-ttu-id="a1b89-103">\_ \_ \_ Struttura Caps di configurazione del flusso video TAPI \_</span><span class="sxs-lookup"><span data-stu-id="a1b89-103">TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="a1b89-104">\[ Questa struttura non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a1b89-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a1b89-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a1b89-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a1b89-106">La struttura di **Caps di \_ \_ \_ configurazione \_ del flusso video TAPI** è contenuta nella struttura di caps di  [**\_ \_ configurazione \_ del flusso TAPI**](tapi-stream-config-caps.md) quando il membro CapsType è impostato sul membro **VideoCap** dell'Unione [**StreamConfigCapsType**](streamconfigcapstype.md) .</span><span class="sxs-lookup"><span data-stu-id="a1b89-106">The **TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **VideoCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b89-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1b89-107">Syntax</span></span>


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="a1b89-108">Members</span><span class="sxs-lookup"><span data-stu-id="a1b89-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1b89-109">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a1b89-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-110">Descrizione intuitiva del tipo di configurazione del flusso audio da visualizzare agli utenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a1b89-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-111">**VideoStandard**</span><span class="sxs-lookup"><span data-stu-id="a1b89-111">**VideoStandard**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-112">Viene usato il video standard.</span><span class="sxs-lookup"><span data-stu-id="a1b89-112">Video standard being used.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-113">**InputSize**</span><span class="sxs-lookup"><span data-stu-id="a1b89-113">**InputSize**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-114">Dimensioni di input del frame.</span><span class="sxs-lookup"><span data-stu-id="a1b89-114">Input size of frame.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-115">**MinCroppingSize**</span><span class="sxs-lookup"><span data-stu-id="a1b89-115">**MinCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-116">Dimensioni minime di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="a1b89-116">Minimum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-117">**MaxCroppingSize**</span><span class="sxs-lookup"><span data-stu-id="a1b89-117">**MaxCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-118">Dimensioni massime di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="a1b89-118">Maximum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-119">**CropGranularityX**</span><span class="sxs-lookup"><span data-stu-id="a1b89-119">**CropGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-120">Granularità del ritaglio consentito lungo l'asse x.</span><span class="sxs-lookup"><span data-stu-id="a1b89-120">Granularity of cropping allowed along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-121">**CropGranularityY**</span><span class="sxs-lookup"><span data-stu-id="a1b89-121">**CropGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-122">Granularità del ritaglio consentito lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="a1b89-122">Granularity of cropping allowed along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-123">**CropAlignX**</span><span class="sxs-lookup"><span data-stu-id="a1b89-123">**CropAlignX**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-124">Allineamento del ritaglio di asse x.</span><span class="sxs-lookup"><span data-stu-id="a1b89-124">Alignment of x-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-125">**CropAlignY**</span><span class="sxs-lookup"><span data-stu-id="a1b89-125">**CropAlignY**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-126">Allineamento del ritaglio dell'asse y.</span><span class="sxs-lookup"><span data-stu-id="a1b89-126">Alignment of y-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-127">**MinOutputSize**</span><span class="sxs-lookup"><span data-stu-id="a1b89-127">**MinOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-128">Dimensioni minime risultanti della finestra video.</span><span class="sxs-lookup"><span data-stu-id="a1b89-128">Minimum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-129">**MaxOutputSize**</span><span class="sxs-lookup"><span data-stu-id="a1b89-129">**MaxOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-130">Dimensione massima risultante della finestra video.</span><span class="sxs-lookup"><span data-stu-id="a1b89-130">Maximum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-131">**OutputGranularityX**</span><span class="sxs-lookup"><span data-stu-id="a1b89-131">**OutputGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-132">Granularità delle dimensioni di output lungo l'asse x.</span><span class="sxs-lookup"><span data-stu-id="a1b89-132">Granularity of output size along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-133">**OutputGranularityY**</span><span class="sxs-lookup"><span data-stu-id="a1b89-133">**OutputGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-134">Granularità delle dimensioni di output lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="a1b89-134">Granularity of output size along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-135">**StretchTapsX**</span><span class="sxs-lookup"><span data-stu-id="a1b89-135">**StretchTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-136">Estendi lungo l'asse x.</span><span class="sxs-lookup"><span data-stu-id="a1b89-136">Stretch along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-137">**StretchTapsY**</span><span class="sxs-lookup"><span data-stu-id="a1b89-137">**StretchTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-138">Estendi lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="a1b89-138">Stretch along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-139">**ShrinkTapsX**</span><span class="sxs-lookup"><span data-stu-id="a1b89-139">**ShrinkTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-140">Compatta lungo l'asse x.</span><span class="sxs-lookup"><span data-stu-id="a1b89-140">Shrink along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-141">**ShrinkTapsY**</span><span class="sxs-lookup"><span data-stu-id="a1b89-141">**ShrinkTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-142">Compatta lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="a1b89-142">Shrink along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-143">**MinFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="a1b89-143">**MinFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-144">Intervallo minimo del fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="a1b89-144">Minimum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-145">**MaxFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="a1b89-145">**MaxFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-146">Intervallo massimo di fotogrammi video.</span><span class="sxs-lookup"><span data-stu-id="a1b89-146">Maximum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-147">**MinBitsPerSecond**</span><span class="sxs-lookup"><span data-stu-id="a1b89-147">**MinBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-148">Bit minimi al secondo.</span><span class="sxs-lookup"><span data-stu-id="a1b89-148">Minimum bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="a1b89-149">**MaxBitsPerSecond**</span><span class="sxs-lookup"><span data-stu-id="a1b89-149">**MaxBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="a1b89-150">Numero massimo di bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="a1b89-150">Maximum bits per second.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1b89-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1b89-151">Requirements</span></span>



| <span data-ttu-id="a1b89-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1b89-152">Requirement</span></span> | <span data-ttu-id="a1b89-153">Valore</span><span class="sxs-lookup"><span data-stu-id="a1b89-153">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b89-154">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="a1b89-154">TAPI version</span></span><br/> | <span data-ttu-id="a1b89-155">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="a1b89-155">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="a1b89-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1b89-156">Header</span></span><br/>       | <dl> <span data-ttu-id="a1b89-157"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1b89-157"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1b89-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1b89-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b89-159">**\_ \_ tappi configurazione flusso TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="a1b89-159">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




