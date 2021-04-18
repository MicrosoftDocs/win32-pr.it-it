---
description: La struttura di caps di configurazione del \_ flusso TAPI \_ \_ contiene informazioni sulla configurazione di flussi video o audio.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: Struttura TAPI_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379ca481d3bebaf8ceb11bfc2dbdab6642ca20b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328901"
---
# <a name="tapi_stream_config_caps-structure"></a><span data-ttu-id="b1312-103">\_Struttura di \_ Caps di configurazione del flusso TAPI \_</span><span class="sxs-lookup"><span data-stu-id="b1312-103">TAPI\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="b1312-104">\[ Questa struttura non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b1312-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b1312-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="b1312-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b1312-106">La struttura di **\_ \_ \_ Caps** di configurazione del flusso TAPI contiene informazioni sulla configurazione di flussi video o audio.</span><span class="sxs-lookup"><span data-stu-id="b1312-106">The **TAPI\_STREAM\_CONFIG\_CAPS** structure contains either video or audio stream configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1312-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1312-107">Syntax</span></span>


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="b1312-108">Members</span><span class="sxs-lookup"><span data-stu-id="b1312-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b1312-109">**CapsType**</span><span class="sxs-lookup"><span data-stu-id="b1312-109">**CapsType**</span></span>
</dt> <dd>

<span data-ttu-id="b1312-110">Definisce se il membro di Unione contiene informazioni video o audio.</span><span class="sxs-lookup"><span data-stu-id="b1312-110">Defines whether the union member contains video or audio information.</span></span>

</dd> <dt>

<span data-ttu-id="b1312-111">**VideoCap**</span><span class="sxs-lookup"><span data-stu-id="b1312-111">**VideoCap**</span></span>
</dt> <dd>

<span data-ttu-id="b1312-112">Struttura [**di \_ \_ Caps di \_ configurazione \_ del flusso video TAPI**](tapi-video-stream-config-caps.md) che contiene le funzionalità del flusso video.</span><span class="sxs-lookup"><span data-stu-id="b1312-112">A [**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**](tapi-video-stream-config-caps.md) structure containing the video stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="b1312-113">**AudioCap**</span><span class="sxs-lookup"><span data-stu-id="b1312-113">**AudioCap**</span></span>
</dt> <dd>

<span data-ttu-id="b1312-114">Struttura [**di \_ \_ Caps di \_ configurazione \_ del flusso audio TAPI**](tapi-audio-stream-config-caps.md) che contiene le funzionalità del flusso audio.</span><span class="sxs-lookup"><span data-stu-id="b1312-114">A [**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**](tapi-audio-stream-config-caps.md) structure containing the audio stream capabilities.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1312-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1312-115">Requirements</span></span>



| <span data-ttu-id="b1312-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1312-116">Requirement</span></span> | <span data-ttu-id="b1312-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b1312-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b1312-118">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="b1312-118">TAPI version</span></span><br/> | <span data-ttu-id="b1312-119">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="b1312-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="b1312-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1312-120">Header</span></span><br/>       | <dl> <span data-ttu-id="b1312-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1312-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1312-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1312-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1312-123">**ITFormatControl::GetStreamCaps**</span><span class="sxs-lookup"><span data-stu-id="b1312-123">**ITFormatControl::GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[<span data-ttu-id="b1312-124">**StreamConfigCapsType**</span><span class="sxs-lookup"><span data-stu-id="b1312-124">**StreamConfigCapsType**</span></span>](streamconfigcapstype.md)
</dt> <dt>

[<span data-ttu-id="b1312-125">**\_ \_ \_ tappi di configurazione \_ flusso video TAPI**</span><span class="sxs-lookup"><span data-stu-id="b1312-125">**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-video-stream-config-caps.md)
</dt> <dt>

[<span data-ttu-id="b1312-126">**\_ \_ \_ tappi di configurazione del flusso audio TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="b1312-126">**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




