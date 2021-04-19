---
description: La \_ struttura PERFINFO dshow \_ AVREND contiene i dati per un evento di traccia di tipo GUID \_ VIDEOREND. VMR registra questo evento immediatamente prima di eseguire il rendering di un frame.
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: Struttura PERFINFO_DSHOW_AVREND (Perfstruct. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AVREND
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: ee2d944d086f9c1a4ea7944f023321dfbc06d547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332263"
---
# <a name="perfinfo_dshow_avrend-structure"></a><span data-ttu-id="74892-103">\_Struttura PERFINFO dshow \_ AVREND</span><span class="sxs-lookup"><span data-stu-id="74892-103">PERFINFO\_DSHOW\_AVREND structure</span></span>

<span data-ttu-id="74892-104">La `PERFINFO_DSHOW_AVREND` struttura contiene dati per un evento di traccia di tipo GUID \_ VIDEOREND.</span><span class="sxs-lookup"><span data-stu-id="74892-104">The `PERFINFO_DSHOW_AVREND` structure contains data for a trace event of type GUID\_VIDEOREND.</span></span>

<span data-ttu-id="74892-105">VMR registra questo evento immediatamente prima di eseguire il rendering di un frame.</span><span class="sxs-lookup"><span data-stu-id="74892-105">The VMR logs this event immediately before rendering a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="74892-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74892-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a><span data-ttu-id="74892-107">Members</span><span class="sxs-lookup"><span data-stu-id="74892-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="74892-108">**cycleCounter**</span><span class="sxs-lookup"><span data-stu-id="74892-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="74892-109">Numero di cicli di clock più recenti (istruzione RDTSC).</span><span class="sxs-lookup"><span data-stu-id="74892-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="74892-110">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="74892-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="74892-111">Ora di riferimento corrente, restituita dal metodo [**IReferenceClock:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .</span><span class="sxs-lookup"><span data-stu-id="74892-111">Current reference time, as returned by the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

</dd> <dt>

<span data-ttu-id="74892-112">**sampleTime**</span><span class="sxs-lookup"><span data-stu-id="74892-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="74892-113">Ora di inizio dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="74892-113">Start time of the sample.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74892-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="74892-114">Remarks</span></span>

<span data-ttu-id="74892-115">Per abilitare questo evento, è necessario impostare il \_ flag DXMPERF VIDEOREND nel parametro *EnableFlag* quando si chiama **EnableTrace**.</span><span class="sxs-lookup"><span data-stu-id="74892-115">To enable this event, you must set the DXMPERF\_VIDEOREND flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="74892-116">Questo flag è definito nel file di intestazione Dxmperf. h, incluso nelle classi base di DirectShow.</span><span class="sxs-lookup"><span data-stu-id="74892-116">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="74892-117">Per registrare questo evento da un filtro DirectShow, usare la **macro \_ VIDEOREND di PERFLOG** , definita in Dxmperf. h.</span><span class="sxs-lookup"><span data-stu-id="74892-117">To log this event from a DirectShow filter, use the **PERFLOG\_VIDEOREND** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="74892-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74892-118">Requirements</span></span>



| <span data-ttu-id="74892-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="74892-119">Requirement</span></span> | <span data-ttu-id="74892-120">Valore</span><span class="sxs-lookup"><span data-stu-id="74892-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74892-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74892-121">Header</span></span><br/> | <dl> <span data-ttu-id="74892-122"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="74892-122"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74892-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74892-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74892-124">Strutture DirectShow</span><span class="sxs-lookup"><span data-stu-id="74892-124">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="74892-125">Traccia eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="74892-125">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="74892-126">GUID dell'evento di traccia</span><span class="sxs-lookup"><span data-stu-id="74892-126">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




