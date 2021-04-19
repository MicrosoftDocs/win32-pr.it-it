---
title: Struttura DRM_PLAY_OPL (wmdrmsdk. h)
description: La \_ struttura OPL di riproduzione DRM \_ include informazioni sui livelli di protezione dell'output (OPLs) specificati in una licenza per le azioni di riproduzione.
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- Formato di Windows Media per la struttura DRM_PLAY_OPL
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a40d8fe4e8b3c820f9d7bcb405b5c0806040182
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333625"
---
# <a name="drm_play_opl-structure"></a><span data-ttu-id="c475e-105">\_Struttura OPL della riproduzione DRM \_</span><span class="sxs-lookup"><span data-stu-id="c475e-105">DRM\_PLAY\_OPL structure</span></span>

<span data-ttu-id="c475e-106">La **struttura \_ \_ OPL di riproduzione DRM** include informazioni sui livelli di protezione dell'output (OPLs) specificati in una licenza per le azioni di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c475e-106">The **DRM\_PLAY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c475e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c475e-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="c475e-108">Members</span><span class="sxs-lookup"><span data-stu-id="c475e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c475e-109">**minOPL**</span><span class="sxs-lookup"><span data-stu-id="c475e-109">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="c475e-110">[**DRM \_ Struttura \_ dei \_ \_ livelli di protezione dell'output minima**](drmdrm-minimum-output-protection-levels.md) che contiene il OPL minimo richiesto per riprodurre contenuto in formati diversi.</span><span class="sxs-lookup"><span data-stu-id="c475e-110">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="c475e-111">**oplIdReserved**</span><span class="sxs-lookup"><span data-stu-id="c475e-111">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="c475e-112">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="c475e-112">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="c475e-113">**vopi**</span><span class="sxs-lookup"><span data-stu-id="c475e-113">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="c475e-114">[**DRM \_ Struttura \_ degli \_ \_ ID di protezione dell'output video**](drmdrm-video-output-protection-ids.md) contenente gli identificatori di protezione dell'output video che si applicano alla riproduzione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="c475e-114">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c475e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c475e-115">Requirements</span></span>



| <span data-ttu-id="c475e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c475e-116">Requirement</span></span> | <span data-ttu-id="c475e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c475e-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c475e-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c475e-118">Header</span></span><br/> | <dl> <span data-ttu-id="c475e-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c475e-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c475e-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c475e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c475e-121">**\_copia DRM \_ OPL**</span><span class="sxs-lookup"><span data-stu-id="c475e-121">**DRM\_COPY\_OPL**</span></span>](drmdrm-copy-opl.md)
</dt> <dt>

[<span data-ttu-id="c475e-122">**DRM \_ Play \_ OPL \_ ex**</span><span class="sxs-lookup"><span data-stu-id="c475e-122">**DRM\_PLAY\_OPL\_EX**</span></span>](drm-play-opl-ex.md)
</dt> <dt>

[<span data-ttu-id="c475e-123">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="c475e-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





