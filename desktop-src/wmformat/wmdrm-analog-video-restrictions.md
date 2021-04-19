---
title: Struttura WMDRM_ANALOG_VIDEO_RESTRICTIONS (wmdrmsdk. h)
description: La \_ struttura di restrizioni video analoghe di WMDRM \_ \_ include informazioni su una restrizione per la riproduzione di contenuto come video analogico.
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- Formato di Windows Media per la struttura WMDRM_ANALOG_VIDEO_RESTRICTIONS
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3d6b8fe957468baebb6da06f45ba7b37756413c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326608"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a><span data-ttu-id="1436a-105">\_Struttura di \_ restrizioni video ANALOGIche WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="1436a-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS structure</span></span>

<span data-ttu-id="1436a-106">La struttura di **\_ \_ \_ restrizioni video analoghe di WMDRM** include informazioni su una restrizione per la riproduzione di contenuto come video analogico.</span><span class="sxs-lookup"><span data-stu-id="1436a-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS** structure holds information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="1436a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1436a-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="1436a-108">Members</span><span class="sxs-lookup"><span data-stu-id="1436a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1436a-109">**guidRestrictionID**</span><span class="sxs-lookup"><span data-stu-id="1436a-109">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="1436a-110">Identificatore di restrizione.</span><span class="sxs-lookup"><span data-stu-id="1436a-110">Restriction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1436a-111">**dwRestrictionData**</span><span class="sxs-lookup"><span data-stu-id="1436a-111">**dwRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="1436a-112">Dati di restrizione.</span><span class="sxs-lookup"><span data-stu-id="1436a-112">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1436a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1436a-113">Remarks</span></span>

<span data-ttu-id="1436a-114">Questa struttura viene ricevuta quando si chiama [**IWMDRMLicense:: GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).</span><span class="sxs-lookup"><span data-stu-id="1436a-114">This structure is received when you call [**IWMDRMLicense::GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1436a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1436a-115">Requirements</span></span>



| <span data-ttu-id="1436a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1436a-116">Requirement</span></span> | <span data-ttu-id="1436a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1436a-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1436a-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1436a-118">Header</span></span><br/> | <dl> <span data-ttu-id="1436a-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1436a-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1436a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1436a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1436a-121">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="1436a-121">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="1436a-122">**\_ \_ restrizioni video ANALOGIche WMDRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1436a-122">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX**</span></span>](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





