---
title: Struttura DRM_OPL_OUTPUT_IDS (wmdrmsdk. h)
description: La \_ struttura degli \_ \_ ID di output di DRM OPL include un numero di identificatori di output OPL (output Protection Level).
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- Formato di Windows Media per la struttura DRM_OPL_OUTPUT_IDS
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802787c5e373c837d639e0225bf650d80c105970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330249"
---
# <a name="drm_opl_output_ids-structure"></a><span data-ttu-id="9912f-105">\_Struttura di \_ ID output OPL \_ DRM</span><span class="sxs-lookup"><span data-stu-id="9912f-105">DRM\_OPL\_OUTPUT\_IDS structure</span></span>

<span data-ttu-id="9912f-106">La struttura degli **\_ ID di \_ output \_ di DRM OPL** include un numero di identificatori di output OPL (output Protection Level).</span><span class="sxs-lookup"><span data-stu-id="9912f-106">The **DRM\_OPL\_OUTPUT\_IDS** structure holds a number of output protection level (OPL) output identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="9912f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9912f-107">Syntax</span></span>


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a><span data-ttu-id="9912f-108">Members</span><span class="sxs-lookup"><span data-stu-id="9912f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9912f-109">**CID**</span><span class="sxs-lookup"><span data-stu-id="9912f-109">**cIds**</span></span>
</dt> <dd>

<span data-ttu-id="9912f-110">Numero di identificatori nella matrice a cui fa riferimento **rgIds**.</span><span class="sxs-lookup"><span data-stu-id="9912f-110">Number of identifiers in the array referenced by **rgIds**.</span></span>

</dd> <dt>

<span data-ttu-id="9912f-111">**rgIds**</span><span class="sxs-lookup"><span data-stu-id="9912f-111">**rgIds**</span></span>
</dt> <dd>

<span data-ttu-id="9912f-112">Indirizzo di una matrice di GUID.</span><span class="sxs-lookup"><span data-stu-id="9912f-112">Address of an array of GUIDs.</span></span> <span data-ttu-id="9912f-113">Ogni membro della matrice contiene un identificatore di output OPL.</span><span class="sxs-lookup"><span data-stu-id="9912f-113">Each member of the array contains an OPL output identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9912f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9912f-114">Remarks</span></span>

<span data-ttu-id="9912f-115">Questa struttura viene utilizzata come membro delle strutture di [**\_ copia DRM \_ OPL**](drmdrm-copy-opl.md) e [**DRM \_ Play \_ OPL**](drmdrm-play-opl.md) per identificare i gruppi di identificatori di output.</span><span class="sxs-lookup"><span data-stu-id="9912f-115">This structure is used as a member of the [**DRM\_COPY\_OPL**](drmdrm-copy-opl.md) and [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structures to identify groups of output identifiers.</span></span>

## <a name="requirements"></a><span data-ttu-id="9912f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9912f-116">Requirements</span></span>



| <span data-ttu-id="9912f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9912f-117">Requirement</span></span> | <span data-ttu-id="9912f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9912f-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9912f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9912f-119">Header</span></span><br/> | <dl> <span data-ttu-id="9912f-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="9912f-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9912f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9912f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9912f-122">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="9912f-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





