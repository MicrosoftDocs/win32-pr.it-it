---
description: L' \_ enumerazione DEXTERF Track \_ Search \_ flags specifica le condizioni di limite in una ricerca di un oggetto nella sequenza temporale.
ms.assetid: 9a66ea17-5c2c-41fd-8a7b-c9918b10c8c9
title: Enumerazione DEXTERF_TRACK_SEARCH_FLAGS (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTERF_TRACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 09923d6be01bdf4a213db645a34b038dda15d86f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330660"
---
# <a name="dexterf_track_search_flags-enumeration"></a><span data-ttu-id="5d174-103">\_ \_ Enumerazione flag di ricerca DEXTERF Track \_</span><span class="sxs-lookup"><span data-stu-id="5d174-103">DEXTERF\_TRACK\_SEARCH\_FLAGS enumeration</span></span>

> [!Note]  
> <span data-ttu-id="5d174-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5d174-104">\[Deprecated.</span></span> <span data-ttu-id="5d174-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5d174-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5d174-106">L' `DEXTERF_TRACK_SEARCH_FLAGS` enumerazione specifica le condizioni di limite in una ricerca di un oggetto nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="5d174-106">The `DEXTERF_TRACK_SEARCH_FLAGS` enumeration specifies the boundary conditions on a search for an object in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d174-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d174-107">Syntax</span></span>


```C++
typedef enum  { 
  DEXTERF_BOUNDING    = -1,
  DEXTERF_EXACTLY_AT  = 0,
  DEXTERF_FORWARDS    = 1
} DEXTERF_TRACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="5d174-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="5d174-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5d174-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**\_delimitatore DEXTERF**</span><span class="sxs-lookup"><span data-stu-id="5d174-109"><span id="DEXTERF_BOUNDING"></span><span id="dexterf_bounding"></span>**DEXTERF\_BOUNDING**</span></span>
</dt> <dd>

<span data-ttu-id="5d174-110">Cerca un oggetto che si estende sul tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="5d174-110">Search for an object that spans the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="5d174-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF \_ esattamente \_ alle**</span><span class="sxs-lookup"><span data-stu-id="5d174-111"><span id="DEXTERF_EXACTLY_AT"></span><span id="dexterf_exactly_at"></span>**DEXTERF\_EXACTLY\_AT**</span></span>
</dt> <dd>

<span data-ttu-id="5d174-112">Cercare un oggetto che si avvii esattamente all'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="5d174-112">Search for an object that starts exactly at the specified time.</span></span>

</dd> <dt>

<span data-ttu-id="5d174-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF \_ inoltri**</span><span class="sxs-lookup"><span data-stu-id="5d174-113"><span id="DEXTERF_FORWARDS"></span><span id="dexterf_forwards"></span>**DEXTERF\_FORWARDS**</span></span>
</dt> <dd>

<span data-ttu-id="5d174-114">Cercare un oggetto che inizia all'ora specificata o successiva.</span><span class="sxs-lookup"><span data-stu-id="5d174-114">Search for an object that starts at the specified time or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d174-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d174-115">Remarks</span></span>

<span data-ttu-id="5d174-116">Queste condizioni di limite sono riepilogate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5d174-116">These boundary conditions are summarized in the following table.</span></span>



| <span data-ttu-id="5d174-117">Valore di enumerazione</span><span class="sxs-lookup"><span data-stu-id="5d174-117">Enumeration value</span></span>    | <span data-ttu-id="5d174-118">Condizione limite</span><span class="sxs-lookup"><span data-stu-id="5d174-118">Boundary condition</span></span>                        |
|----------------------|-------------------------------------------|
| <span data-ttu-id="5d174-119">\_delimitatore DEXTERF</span><span class="sxs-lookup"><span data-stu-id="5d174-119">DEXTERF\_BOUNDING</span></span>    | <span data-ttu-id="5d174-120">Start <= TimeStop > Time</span><span class="sxs-lookup"><span data-stu-id="5d174-120">Start <= TimeStop > Time</span></span><br/> |
| <span data-ttu-id="5d174-121">DEXTERF \_ esattamente \_ alle</span><span class="sxs-lookup"><span data-stu-id="5d174-121">DEXTERF\_EXACTLY\_AT</span></span> | <span data-ttu-id="5d174-122">Inizio = = ora</span><span class="sxs-lookup"><span data-stu-id="5d174-122">Start == Time</span></span>                             |
| <span data-ttu-id="5d174-123">DEXTERF \_ inoltri</span><span class="sxs-lookup"><span data-stu-id="5d174-123">DEXTERF\_FORWARDS</span></span>    | <span data-ttu-id="5d174-124">Inizio >= ora</span><span class="sxs-lookup"><span data-stu-id="5d174-124">Start >= Time</span></span>                          |



 

-   <span data-ttu-id="5d174-125">Start: ora di inizio dell'oggetto recuperato.</span><span class="sxs-lookup"><span data-stu-id="5d174-125">Start: start time of the retrieved object.</span></span>
-   <span data-ttu-id="5d174-126">Stop: ora di arresto dell'oggetto recuperato.</span><span class="sxs-lookup"><span data-stu-id="5d174-126">Stop: stop time of the retrieved object.</span></span>
-   <span data-ttu-id="5d174-127">Ora: tempo di ricerca specificato.</span><span class="sxs-lookup"><span data-stu-id="5d174-127">Time: specified search time.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d174-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d174-128">Requirements</span></span>



| <span data-ttu-id="5d174-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d174-129">Requirement</span></span> | <span data-ttu-id="5d174-130">Valore</span><span class="sxs-lookup"><span data-stu-id="5d174-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d174-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d174-131">Header</span></span><br/> | <dl> <span data-ttu-id="5d174-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d174-132"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d174-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d174-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d174-134">**IAMTimelineTrack::GetSrcAtTime**</span><span class="sxs-lookup"><span data-stu-id="5d174-134">**IAMTimelineTrack::GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)
</dt> </dl>

 

 




