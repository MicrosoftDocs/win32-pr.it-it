---
title: Struttura DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX (wmdrmsdk. h)
description: La \_ \_ \_ \_ struttura ad esempio ID protezione output video DRM \_ include una matrice di \_ strutture di protezione dell'output video DRM \_ \_ .
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- Formato di Windows Media per la struttura DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e7cc5ec0b4b14d88deb317e62e3e1cd4f92b57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324049"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a><span data-ttu-id="b7c00-105">\_ \_ ID protezione output video DRM- \_ \_ \_ struttura ex</span><span class="sxs-lookup"><span data-stu-id="b7c00-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="b7c00-106">La struttura ad **\_ \_ \_ \_ \_ esempio ID protezione output video DRM** include una matrice di strutture di **\_ \_ \_ protezione dell'output video DRM** .</span><span class="sxs-lookup"><span data-stu-id="b7c00-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7c00-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7c00-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="b7c00-108">Members</span><span class="sxs-lookup"><span data-stu-id="b7c00-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b7c00-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="b7c00-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="b7c00-110">Numero di versione.</span><span class="sxs-lookup"><span data-stu-id="b7c00-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="b7c00-111">**Centri di**</span><span class="sxs-lookup"><span data-stu-id="b7c00-111">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="b7c00-112">Numero di elementi nella matrice a cui fa riferimento **rgVop**.</span><span class="sxs-lookup"><span data-stu-id="b7c00-112">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="b7c00-113">**rgVop**</span><span class="sxs-lookup"><span data-stu-id="b7c00-113">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="b7c00-114">Indirizzo di una matrice di **strutture \_ \_ \_ \_ ex protezione output video DRM** .</span><span class="sxs-lookup"><span data-stu-id="b7c00-114">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="b7c00-115">**DRM \_ La \_ protezione dell'output \_ \_ video** è un tipo definito [**come \_ \_ protezione dell' \_ output DRM**](drm-output-protection-ex.md), ad esempio.</span><span class="sxs-lookup"><span data-stu-id="b7c00-115">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7c00-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7c00-116">Remarks</span></span>

<span data-ttu-id="b7c00-117">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="b7c00-117">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7c00-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7c00-118">Requirements</span></span>



| <span data-ttu-id="b7c00-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7c00-119">Requirement</span></span> | <span data-ttu-id="b7c00-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b7c00-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c00-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7c00-121">Header</span></span><br/> | <dl> <span data-ttu-id="b7c00-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7c00-122"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7c00-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7c00-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c00-124">**\_ \_ \_ ID protezione output audio \_ DRM \_ es.**</span><span class="sxs-lookup"><span data-stu-id="b7c00-124">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="b7c00-125">**\_ID di \_ protezione dell'output del video DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7c00-125">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="b7c00-126">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="b7c00-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





