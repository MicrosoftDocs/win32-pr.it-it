---
description: La \_ struttura dei \_ tappi di configurazione del flusso audio TAPI \_ \_ è contenuta nella \_ struttura dei limiti di configurazione del flusso TAPI \_ \_ quando il membro CapsType è impostato sul membro AudioCap dell'Unione StreamConfigCapsType.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: Struttura TAPI_AUDIO_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327488"
---
# <a name="tapi_audio_stream_config_caps-structure"></a><span data-ttu-id="7e959-103">\_Struttura di \_ \_ Caps di configurazione del flusso audio TAPI \_</span><span class="sxs-lookup"><span data-stu-id="7e959-103">TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="7e959-104">\[ Questa struttura non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7e959-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7e959-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="7e959-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7e959-106">La struttura dei **\_ \_ \_ \_ tappi di configurazione del flusso audio TAPI** è contenuta nella struttura dei [**\_ \_ \_ limiti di configurazione del flusso TAPI**](tapi-stream-config-caps.md) quando il membro **CapsType** è impostato sul membro **AudioCap** dell'Unione [**StreamConfigCapsType**](streamconfigcapstype.md) .</span><span class="sxs-lookup"><span data-stu-id="7e959-106">The **TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **AudioCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e959-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e959-107">Syntax</span></span>


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="7e959-108">Members</span><span class="sxs-lookup"><span data-stu-id="7e959-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7e959-109">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7e959-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7e959-110">Descrizione intuitiva del tipo di configurazione del flusso audio da visualizzare agli utenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e959-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="7e959-111">**MinimumChannels**</span><span class="sxs-lookup"><span data-stu-id="7e959-111">**MinimumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="7e959-112">Numero minimo di canali associati al flusso.</span><span class="sxs-lookup"><span data-stu-id="7e959-112">The minimum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="7e959-113">**MaximumChannels**</span><span class="sxs-lookup"><span data-stu-id="7e959-113">**MaximumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="7e959-114">Numero massimo di canali associati al flusso.</span><span class="sxs-lookup"><span data-stu-id="7e959-114">The maximum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="7e959-115">**ChannelsGranularity**</span><span class="sxs-lookup"><span data-stu-id="7e959-115">**ChannelsGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="7e959-116">Granularità del numero di canali.</span><span class="sxs-lookup"><span data-stu-id="7e959-116">The granularity of the channel count.</span></span>

</dd> <dt>

<span data-ttu-id="7e959-117">**MinimumBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="7e959-117">**MinimumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="7e959-118">Numero minimo di bit per campione.</span><span class="sxs-lookup"><span data-stu-id="7e959-118">The minimum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="7e959-119">**MaximumBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="7e959-119">**MaximumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="7e959-120">Numero massimo di bit per campione.</span><span class="sxs-lookup"><span data-stu-id="7e959-120">The maximum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="7e959-121">**BitsPerSampleGranularity**</span><span class="sxs-lookup"><span data-stu-id="7e959-121">**BitsPerSampleGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="7e959-122">Granularità dei bit per i valori di esempio.</span><span class="sxs-lookup"><span data-stu-id="7e959-122">The granularity of the bits per sample values.</span></span>

</dd> <dt>

<span data-ttu-id="7e959-123">**MinimumSampleFrequency**</span><span class="sxs-lookup"><span data-stu-id="7e959-123">**MinimumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="7e959-124">Frequenza di campionamento minima.</span><span class="sxs-lookup"><span data-stu-id="7e959-124">The minimum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="7e959-125">**MaximumSampleFrequency**</span><span class="sxs-lookup"><span data-stu-id="7e959-125">**MaximumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="7e959-126">Frequenza massima di campionamento.</span><span class="sxs-lookup"><span data-stu-id="7e959-126">The maximum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="7e959-127">**SampleFrequencyGranularity**</span><span class="sxs-lookup"><span data-stu-id="7e959-127">**SampleFrequencyGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="7e959-128">Granularità dei valori della frequenza di campionamento.</span><span class="sxs-lookup"><span data-stu-id="7e959-128">The granularity of the sampling frequency values.</span></span>

</dd> <dt>

<span data-ttu-id="7e959-129">**MinimumAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="7e959-129">**MinimumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="7e959-130">Media minima di byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="7e959-130">The minimum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="7e959-131">**MaximumAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="7e959-131">**MaximumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="7e959-132">Numero massimo di byte media al secondo.</span><span class="sxs-lookup"><span data-stu-id="7e959-132">The maximum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="7e959-133">**AvgBytesPerSecGranularity**</span><span class="sxs-lookup"><span data-stu-id="7e959-133">**AvgBytesPerSecGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="7e959-134">Granularità dei valori di byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="7e959-134">The granularity of the bytes per second values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e959-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e959-135">Requirements</span></span>



| <span data-ttu-id="7e959-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e959-136">Requirement</span></span> | <span data-ttu-id="7e959-137">Valore</span><span class="sxs-lookup"><span data-stu-id="7e959-137">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e959-138">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7e959-138">TAPI version</span></span><br/> | <span data-ttu-id="7e959-139">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="7e959-139">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="7e959-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e959-140">Header</span></span><br/>       | <dl> <span data-ttu-id="7e959-141"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e959-141"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e959-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e959-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e959-143">**\_ \_ tappi configurazione flusso TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="7e959-143">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




