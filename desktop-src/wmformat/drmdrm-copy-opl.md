---
title: Struttura DRM_COPY_OPL (wmdrmsdk. h)
description: La \_ \_ struttura OPL copia DRM include informazioni sui livelli di protezione dell'output (OPLs) specificati in una licenza per le azioni di copia.
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- Formato di Windows Media per la struttura DRM_COPY_OPL
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_COPY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28655e220588bb704567de033e1117dd569d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330884"
---
# <a name="drm_copy_opl-structure"></a><span data-ttu-id="8a56d-105">\_ \_ Struttura OPL copia DRM</span><span class="sxs-lookup"><span data-stu-id="8a56d-105">DRM\_COPY\_OPL structure</span></span>

<span data-ttu-id="8a56d-106">La **struttura \_ \_ OPL copia DRM** include informazioni sui livelli di protezione dell'output (OPLs) specificati in una licenza per le azioni di copia.</span><span class="sxs-lookup"><span data-stu-id="8a56d-106">The **DRM\_COPY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for copy actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a56d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a56d-107">Syntax</span></span>


```C++
typedef struct DRM_COPY_OPL {
  WORD               wMinimumCopyLevel;
  DRM_OPL_OUTPUT_IDS oplIdIncludes;
  DRM_OPL_OUTPUT_IDS oplIdExcludes;
} ;
```



## <a name="members"></a><span data-ttu-id="8a56d-108">Members</span><span class="sxs-lookup"><span data-stu-id="8a56d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a56d-109">**wMinimumCopyLevel**</span><span class="sxs-lookup"><span data-stu-id="8a56d-109">**wMinimumCopyLevel**</span></span>
</dt> <dd>

<span data-ttu-id="8a56d-110">OPL minimo per le azioni di copia.</span><span class="sxs-lookup"><span data-stu-id="8a56d-110">Minimum OPL for copy actions.</span></span>

</dd> <dt>

<span data-ttu-id="8a56d-111">**oplIdIncludes**</span><span class="sxs-lookup"><span data-stu-id="8a56d-111">**oplIdIncludes**</span></span>
</dt> <dd>

<span data-ttu-id="8a56d-112">[**DRM \_ Struttura \_ di \_ ID output OPL**](drmdrm-opl-output-ids.md) contenente gli identificatori delle tecnologie da consentire.</span><span class="sxs-lookup"><span data-stu-id="8a56d-112">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the identifiers of technologies to allow.</span></span> <span data-ttu-id="8a56d-113">Questo membro viene utilizzato per le tecnologie di output a cui sono assegnati OPLs inferiori al livello di copia minimo, ma in cui è possibile copiare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="8a56d-113">This member is used for output technologies that are assigned OPLs lower than the minimum copy level, but to which the content may be copied.</span></span>

</dd> <dt>

<span data-ttu-id="8a56d-114">**oplIdExcludes**</span><span class="sxs-lookup"><span data-stu-id="8a56d-114">**oplIdExcludes**</span></span>
</dt> <dd>

<span data-ttu-id="8a56d-115">[**DRM \_ OPL \_ \_ ID output**](drmdrm-opl-output-ids.md) struttura contenente gli identificatori di output delle tecnologie da limitare.</span><span class="sxs-lookup"><span data-stu-id="8a56d-115">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the output identifiers of technologies to restrict.</span></span> <span data-ttu-id="8a56d-116">Questo membro viene utilizzato per le tecnologie di output a cui sono assegnati OPLs che superano il livello di copia minimo, ma che l'emittente della licenza non concede i diritti per la copia in.</span><span class="sxs-lookup"><span data-stu-id="8a56d-116">This member is used for output technologies that are assigned OPLs that exceed the minimum copy level, but that the license issuer does not grant rights for copying to.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a56d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a56d-117">Requirements</span></span>



| <span data-ttu-id="8a56d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a56d-118">Requirement</span></span> | <span data-ttu-id="8a56d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8a56d-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a56d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a56d-120">Header</span></span><br/> | <dl> <span data-ttu-id="8a56d-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a56d-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a56d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a56d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a56d-123">**\_riproduzione DRM \_ OPL**</span><span class="sxs-lookup"><span data-stu-id="8a56d-123">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="8a56d-124">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="8a56d-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





