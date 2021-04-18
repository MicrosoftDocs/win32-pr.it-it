---
title: Struttura DRM_VIDEO_OUTPUT_PROTECTION_IDS (wmdrmsdk. h)
description: La \_ \_ \_ struttura degli ID di protezione dell'output del video DRM \_ include una matrice di \_ strutture di protezione dell'output video DRM \_ \_ .
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- Formato di Windows Media per la struttura DRM_VIDEO_OUTPUT_PROTECTION_IDS
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51af3ccebec52ab6f6863aeb376ed27f8c8e2467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324450"
---
# <a name="drm_video_output_protection_ids-structure"></a><span data-ttu-id="3251a-105">\_Struttura degli \_ ID di protezione dell'output del video DRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="3251a-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="3251a-106">La struttura degli **ID di protezione dell' \_ output del video \_ \_ \_ DRM** include una matrice di strutture di **\_ \_ \_ protezione dell'output video DRM** .</span><span class="sxs-lookup"><span data-stu-id="3251a-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="3251a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3251a-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="3251a-108">Members</span><span class="sxs-lookup"><span data-stu-id="3251a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3251a-109">**Centri di**</span><span class="sxs-lookup"><span data-stu-id="3251a-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="3251a-110">Numero di elementi nella matrice a cui fa riferimento **rgVop**.</span><span class="sxs-lookup"><span data-stu-id="3251a-110">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="3251a-111">**rgVop**</span><span class="sxs-lookup"><span data-stu-id="3251a-111">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="3251a-112">Indirizzo di una matrice di strutture di **\_ \_ \_ protezione dell'output video DRM** .</span><span class="sxs-lookup"><span data-stu-id="3251a-112">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="3251a-113">**DRM \_ La \_ \_ protezione dell'output video** è un tipo definito come [**\_ \_ protezione dell'output DRM**](drm-output-protection.md).</span><span class="sxs-lookup"><span data-stu-id="3251a-113">**DRM\_VIDEO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3251a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3251a-114">Remarks</span></span>

<span data-ttu-id="3251a-115">Questa struttura viene utilizzata come membro della struttura [**DRM \_ Play \_ OPL**](drmdrm-play-opl.md) .</span><span class="sxs-lookup"><span data-stu-id="3251a-115">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3251a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3251a-116">Requirements</span></span>



| <span data-ttu-id="3251a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3251a-117">Requirement</span></span> | <span data-ttu-id="3251a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3251a-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3251a-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3251a-119">Header</span></span><br/> | <dl> <span data-ttu-id="3251a-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3251a-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3251a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3251a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3251a-122">**\_ID di \_ protezione dell'output audio \_ DRM \_**</span><span class="sxs-lookup"><span data-stu-id="3251a-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="3251a-123">**\_ \_ \_ ID protezione output video \_ DRM \_ es.**</span><span class="sxs-lookup"><span data-stu-id="3251a-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="3251a-124">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="3251a-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





