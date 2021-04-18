---
title: Struttura DRM_PLAY_OPL_EX (wmdrmsdk. h)
description: La \_ struttura ex di DRM Play \_ OPL \_ include informazioni sui livelli di protezione dell'output (OPLs) specificati in una licenza per le azioni di riproduzione.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- Formato di Windows Media per la struttura DRM_PLAY_OPL_EX
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edf85ee664b33df9c63c390a870401b100327f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329052"
---
# <a name="drm_play_opl_ex-structure"></a><span data-ttu-id="7e9d9-105">\_ \_ Struttura ex OPL di DRM Play \_</span><span class="sxs-lookup"><span data-stu-id="7e9d9-105">DRM\_PLAY\_OPL\_EX structure</span></span>

<span data-ttu-id="7e9d9-106">La struttura **ex di DRM \_ Play \_ OPL \_** include informazioni sui livelli di protezione dell'output (OPLs) specificati in una licenza per le azioni di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-106">The **DRM\_PLAY\_OPL\_EX** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e9d9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e9d9-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="7e9d9-108">Members</span><span class="sxs-lookup"><span data-stu-id="7e9d9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7e9d9-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="7e9d9-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7e9d9-110">Numero di versione.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="7e9d9-111">**minOPL**</span><span class="sxs-lookup"><span data-stu-id="7e9d9-111">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="7e9d9-112">[**DRM \_ Struttura \_ dei \_ \_ livelli di protezione dell'output minima**](drmdrm-minimum-output-protection-levels.md) che contiene il OPL minimo richiesto per riprodurre contenuto in formati diversi.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-112">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="7e9d9-113">**oplIdReserved**</span><span class="sxs-lookup"><span data-stu-id="7e9d9-113">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="7e9d9-114">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="7e9d9-115">**vopi**</span><span class="sxs-lookup"><span data-stu-id="7e9d9-115">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="7e9d9-116">[**DRM \_ Struttura \_ degli \_ \_ ID di protezione dell'output video**](drmdrm-video-output-protection-ids.md) contenente gli identificatori di protezione dell'output video che si applicano alla riproduzione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-116">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e9d9-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7e9d9-117">Remarks</span></span>

<span data-ttu-id="7e9d9-118">Questa struttura è identica alla struttura **\_ \_ OPL di riproduzione DRM** , ad eccezione del fatto che include un numero di versione.</span><span class="sxs-lookup"><span data-stu-id="7e9d9-118">This structure is identical to the **DRM\_PLAY\_OPL** structure, except that it includes a version number.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e9d9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e9d9-119">Requirements</span></span>



| <span data-ttu-id="7e9d9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e9d9-120">Requirement</span></span> | <span data-ttu-id="7e9d9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7e9d9-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e9d9-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e9d9-122">Header</span></span><br/> | <dl> <span data-ttu-id="7e9d9-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e9d9-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e9d9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e9d9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e9d9-125">**\_riproduzione DRM \_ OPL**</span><span class="sxs-lookup"><span data-stu-id="7e9d9-125">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="7e9d9-126">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="7e9d9-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





