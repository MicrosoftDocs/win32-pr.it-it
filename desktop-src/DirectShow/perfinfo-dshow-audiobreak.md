---
description: La \_ struttura PERFINFO dshow \_ AUDIOBREAK contiene i dati per un evento di traccia di tipo GUID \_ AUDIOBREAK. Il filtro renderer DirectSound registra questo evento quando si verifica un'interruzioni nel flusso audio.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: Struttura PERFINFO_DSHOW_AUDIOBREAK (Perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AUDIOBREAK
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 599befea67b28acbedffd5c98ebce84aadf70838
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332267"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a><span data-ttu-id="eec5f-103">\_Struttura PERFINFO dshow \_ AUDIOBREAK</span><span class="sxs-lookup"><span data-stu-id="eec5f-103">PERFINFO\_DSHOW\_AUDIOBREAK structure</span></span>

<span data-ttu-id="eec5f-104">La `PERFINFO_DSHOW_AUDIOBREAK` struttura contiene dati per un evento di traccia di tipo GUID \_ AUDIOBREAK.</span><span class="sxs-lookup"><span data-stu-id="eec5f-104">The `PERFINFO_DSHOW_AUDIOBREAK` structure contains data for a trace event of type GUID\_AUDIOBREAK.</span></span>

<span data-ttu-id="eec5f-105">Il filtro [renderer DirectSound](directsound-renderer-filter.md) registra questo evento quando si verifica un'interruzioni nel flusso audio.</span><span class="sxs-lookup"><span data-stu-id="eec5f-105">The [DirectSound Renderer](directsound-renderer-filter.md) filter logs this event when there is a break in the audio stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec5f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eec5f-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a><span data-ttu-id="eec5f-107">Members</span><span class="sxs-lookup"><span data-stu-id="eec5f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="eec5f-108">**cycleCounter**</span><span class="sxs-lookup"><span data-stu-id="eec5f-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="eec5f-109">Numero di cicli di clock più recenti (istruzione RDTSC).</span><span class="sxs-lookup"><span data-stu-id="eec5f-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="eec5f-110">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="eec5f-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="eec5f-111">Posizione di scrittura corrente nel buffer DirectSound.</span><span class="sxs-lookup"><span data-stu-id="eec5f-111">Current write position in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="eec5f-112">**sampleTime**</span><span class="sxs-lookup"><span data-stu-id="eec5f-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="eec5f-113">Inizio dell'interruzioni audio nel buffer DirectSound.</span><span class="sxs-lookup"><span data-stu-id="eec5f-113">Start of the audio break in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="eec5f-114">**sampleDuration**</span><span class="sxs-lookup"><span data-stu-id="eec5f-114">**sampleDuration**</span></span>
</dt> <dd>

<span data-ttu-id="eec5f-115">Durata dell'intervallo, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="eec5f-115">Duration of the break, in milliseconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eec5f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="eec5f-116">Remarks</span></span>

<span data-ttu-id="eec5f-117">Per abilitare questo evento, è necessario impostare il \_ flag di bit AUDIOBREAK nel parametro *EnableFlag* quando si chiama **EnableTrace**.</span><span class="sxs-lookup"><span data-stu-id="eec5f-117">To enable this event, you must set the AUDIOBREAK\_BIT flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="eec5f-118">Questo flag è definito nel file di intestazione Dxmperf. h, incluso nelle classi base di DirectShow.</span><span class="sxs-lookup"><span data-stu-id="eec5f-118">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="eec5f-119">Per registrare questo evento da un filtro DirectShow, usare la **macro \_ AUDIOBREAK di PERFLOG** , definita in Dxmperf. h.</span><span class="sxs-lookup"><span data-stu-id="eec5f-119">To log this event from a DirectShow filter, use the **PERFLOG\_AUDIOBREAK** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="eec5f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eec5f-120">Requirements</span></span>



| <span data-ttu-id="eec5f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="eec5f-121">Requirement</span></span> | <span data-ttu-id="eec5f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="eec5f-122">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eec5f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eec5f-123">Header</span></span><br/> | <dl> <span data-ttu-id="eec5f-124"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="eec5f-124"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eec5f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eec5f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec5f-126">Strutture DirectShow</span><span class="sxs-lookup"><span data-stu-id="eec5f-126">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="eec5f-127">Traccia eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="eec5f-127">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="eec5f-128">GUID dell'evento di traccia</span><span class="sxs-lookup"><span data-stu-id="eec5f-128">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




