---
title: Struttura WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX (wmdrmsdk. h)
description: La \_ \_ struttura ex restrizioni video WMDRM analoghe \_ \_ include informazioni estese su una restrizione per la riproduzione di contenuto come video analogico.
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- Formato di Windows Media per la struttura WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59c9ca5f58cf2adadeb5a6a0618457472cde976c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326609"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a><span data-ttu-id="818df-105">WMDRM \_ la \_ \_ struttura ex restrizione del video analogico \_</span><span class="sxs-lookup"><span data-stu-id="818df-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX structure</span></span>

<span data-ttu-id="818df-106">La **struttura \_ \_ \_ \_ ex restrizioni video WMDRM analoghe** include informazioni estese su una restrizione per la riproduzione di contenuto come video analogico.</span><span class="sxs-lookup"><span data-stu-id="818df-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX** structure holds extended information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="818df-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="818df-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="818df-108">Members</span><span class="sxs-lookup"><span data-stu-id="818df-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="818df-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="818df-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="818df-110">Numero di versione.</span><span class="sxs-lookup"><span data-stu-id="818df-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="818df-111">**guidRestrictionID**</span><span class="sxs-lookup"><span data-stu-id="818df-111">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="818df-112">ID restrizione.</span><span class="sxs-lookup"><span data-stu-id="818df-112">Restriction ID.</span></span>

</dd> <dt>

<span data-ttu-id="818df-113">**cbRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="818df-113">**cbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="818df-114">Dimensioni in byte dei dati di restrizione.</span><span class="sxs-lookup"><span data-stu-id="818df-114">Size of restriction data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="818df-115">**pbRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="818df-115">**pbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="818df-116">Dati di restrizione.</span><span class="sxs-lookup"><span data-stu-id="818df-116">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="818df-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="818df-117">Remarks</span></span>

<span data-ttu-id="818df-118">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="818df-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="818df-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="818df-119">Requirements</span></span>



| <span data-ttu-id="818df-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="818df-120">Requirement</span></span> | <span data-ttu-id="818df-121">Valore</span><span class="sxs-lookup"><span data-stu-id="818df-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="818df-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="818df-122">Header</span></span><br/> | <dl> <span data-ttu-id="818df-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="818df-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="818df-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="818df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="818df-125">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="818df-125">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="818df-126">**\_restrizioni video analogiche WMDRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="818df-126">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**</span></span>](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





