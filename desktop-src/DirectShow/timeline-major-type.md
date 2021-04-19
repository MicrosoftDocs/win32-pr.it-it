---
description: L' \_ enumerazione del \_ tipo principale della sequenza temporale specifica il tipo principale di un oggetto.
ms.assetid: 1a5fde83-2a0a-4bcf-bffe-340a9d914885
title: Enumerazione TIMELINE_MAJOR_TYPE (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TIMELINE_MAJOR_TYPE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 25c3e829aa73d1da78c110ffd148fb0ebaaebdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325470"
---
# <a name="timeline_major_type-enumeration"></a><span data-ttu-id="c6467-103">\_Enumerazione del tipo principale della sequenza temporale \_</span><span class="sxs-lookup"><span data-stu-id="c6467-103">TIMELINE\_MAJOR\_TYPE enumeration</span></span>

> [!Note]  
> <span data-ttu-id="c6467-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c6467-104">\[Deprecated.</span></span> <span data-ttu-id="c6467-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c6467-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c6467-106">L' `TIMELINE_MAJOR_TYPE` enumerazione specifica il tipo principale di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="c6467-106">The `TIMELINE_MAJOR_TYPE` enumeration specifies the major type of an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6467-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6467-107">Syntax</span></span>


```C++
typedef enum  { 
  TIMELINE_MAJOR_TYPE_COMPOSITE   = 1,
  TIMELINE_MAJOR_TYPE_TRACK       = 2,
  TIMELINE_MAJOR_TYPE_SOURCE      = 4,
  TIMELINE_MAJOR_TYPE_TRANSITION  = 8,
  TIMELINE_MAJOR_TYPE_EFFECT      = 16,
  TIMELINE_MAJOR_TYPE_GROUP       = 128
} TIMELINE_MAJOR_TYPE;
```



## <a name="constants"></a><span data-ttu-id="c6467-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="c6467-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c6467-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**\_tipo principale sequenza temporale \_ \_ composita**</span><span class="sxs-lookup"><span data-stu-id="c6467-109"><span id="TIMELINE_MAJOR_TYPE_COMPOSITE"></span><span id="timeline_major_type_composite"></span>**TIMELINE\_MAJOR\_TYPE\_COMPOSITE**</span></span>
</dt> <dd>

<span data-ttu-id="c6467-110">Oggetto composito.</span><span class="sxs-lookup"><span data-stu-id="c6467-110">Composite object.</span></span> <span data-ttu-id="c6467-111">Include una o più tracce.</span><span class="sxs-lookup"><span data-stu-id="c6467-111">Holds one or more tracks.</span></span>

</dd> <dt>

<span data-ttu-id="c6467-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**\_traccia del \_ tipo \_ principale della sequenza temporale**</span><span class="sxs-lookup"><span data-stu-id="c6467-112"><span id="TIMELINE_MAJOR_TYPE_TRACK"></span><span id="timeline_major_type_track"></span>**TIMELINE\_MAJOR\_TYPE\_TRACK**</span></span>
</dt> <dd>

<span data-ttu-id="c6467-113">Oggetto Track.</span><span class="sxs-lookup"><span data-stu-id="c6467-113">Track object.</span></span> <span data-ttu-id="c6467-114">Include una o più origini.</span><span class="sxs-lookup"><span data-stu-id="c6467-114">Holds one or more sources.</span></span>

</dd> <dt>

<span data-ttu-id="c6467-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**\_ \_ origine tipo principale sequenza temporale \_**</span><span class="sxs-lookup"><span data-stu-id="c6467-115"><span id="TIMELINE_MAJOR_TYPE_SOURCE"></span><span id="timeline_major_type_source"></span>**TIMELINE\_MAJOR\_TYPE\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="c6467-116">Oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="c6467-116">Source object.</span></span> <span data-ttu-id="c6467-117">Contiene un riferimento a un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c6467-117">Contains a reference to a media source.</span></span>

</dd> <dt>

<span data-ttu-id="c6467-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**\_transizione di \_ tipo \_ principale della sequenza temporale**</span><span class="sxs-lookup"><span data-stu-id="c6467-118"><span id="TIMELINE_MAJOR_TYPE_TRANSITION"></span><span id="timeline_major_type_transition"></span>**TIMELINE\_MAJOR\_TYPE\_TRANSITION**</span></span>
</dt> <dd>

<span data-ttu-id="c6467-119">Oggetto di transizione.</span><span class="sxs-lookup"><span data-stu-id="c6467-119">Transition object.</span></span> <span data-ttu-id="c6467-120">Definisce una transizione tra compositi, tracce o origini.</span><span class="sxs-lookup"><span data-stu-id="c6467-120">Defines a transition between composites, tracks, or sources.</span></span>

</dd> <dt>

<span data-ttu-id="c6467-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**\_effetto del \_ tipo \_ principale della sequenza temporale**</span><span class="sxs-lookup"><span data-stu-id="c6467-121"><span id="TIMELINE_MAJOR_TYPE_EFFECT"></span><span id="timeline_major_type_effect"></span>**TIMELINE\_MAJOR\_TYPE\_EFFECT**</span></span>
</dt> <dd>

<span data-ttu-id="c6467-122">Oggetto effetto.</span><span class="sxs-lookup"><span data-stu-id="c6467-122">Effect object.</span></span> <span data-ttu-id="c6467-123">Definisce un effetto a input singolo da applicare a un oggetto composito, di traccia o di origine.</span><span class="sxs-lookup"><span data-stu-id="c6467-123">Defines a single-input effect to be applied to a composite, track, or source object.</span></span>

</dd> <dt>

<span data-ttu-id="c6467-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**\_gruppo di \_ tipi \_ principali della sequenza temporale**</span><span class="sxs-lookup"><span data-stu-id="c6467-124"><span id="TIMELINE_MAJOR_TYPE_GROUP"></span><span id="timeline_major_type_group"></span>**TIMELINE\_MAJOR\_TYPE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="c6467-125">Oggetto gruppo.</span><span class="sxs-lookup"><span data-stu-id="c6467-125">Group object.</span></span> <span data-ttu-id="c6467-126">Contiene una o più tracce di un determinato tipo.</span><span class="sxs-lookup"><span data-stu-id="c6467-126">Contains one or more tracks of a given type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6467-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6467-127">Requirements</span></span>



| <span data-ttu-id="c6467-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6467-128">Requirement</span></span> | <span data-ttu-id="c6467-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c6467-129">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c6467-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6467-130">Header</span></span><br/> | <dl> <span data-ttu-id="c6467-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6467-131"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6467-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6467-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6467-133">**IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="c6467-133">**IAMTimeline**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="c6467-134">**IAMTimelineComp::GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="c6467-134">**IAMTimelineComp::GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)
</dt> <dt>

[<span data-ttu-id="c6467-135">**IAMTimelineObj::GetTimelineType**</span><span class="sxs-lookup"><span data-stu-id="c6467-135">**IAMTimelineObj::GetTimelineType**</span></span>](iamtimelineobj-gettimelinetype.md)
</dt> </dl>

 

 




