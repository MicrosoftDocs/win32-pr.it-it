---
title: Struttura DRM_AUDIO_OUTPUT_PROTECTION_IDS (wmdrmsdk. h)
description: La \_ struttura degli \_ ID di protezione dell'output audio DRM \_ \_ contiene un elenco di identificatori di protezione dell'output audio.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- Formato di Windows Media per la struttura DRM_AUDIO_OUTPUT_PROTECTION_IDS
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332283"
---
# <a name="drm_audio_output_protection_ids-structure"></a><span data-ttu-id="1ab40-105">\_Struttura degli \_ \_ ID di protezione dell'output audio DRM \_</span><span class="sxs-lookup"><span data-stu-id="1ab40-105">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="1ab40-106">La struttura degli **\_ ID di \_ \_ protezione \_ dell'output audio DRM** contiene un elenco di identificatori di protezione dell'output audio.</span><span class="sxs-lookup"><span data-stu-id="1ab40-106">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** structure contains a list of audio output protection identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab40-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ab40-107">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="1ab40-108">Members</span><span class="sxs-lookup"><span data-stu-id="1ab40-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1ab40-109">**Centri di**</span><span class="sxs-lookup"><span data-stu-id="1ab40-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="1ab40-110">Numero di voci nella matrice **rgAop** .</span><span class="sxs-lookup"><span data-stu-id="1ab40-110">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="1ab40-111">**rgAop**</span><span class="sxs-lookup"><span data-stu-id="1ab40-111">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="1ab40-112">Matrice di strutture di **\_ \_ \_ protezione dell'output audio DRM** .</span><span class="sxs-lookup"><span data-stu-id="1ab40-112">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="1ab40-113">**DRM \_ La \_ \_ protezione dell'output audio** è un tipo definito come [**\_ \_ protezione dell'output DRM**](drm-output-protection.md).</span><span class="sxs-lookup"><span data-stu-id="1ab40-113">**DRM\_AUDIO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ab40-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ab40-114">Remarks</span></span>

<span data-ttu-id="1ab40-115">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="1ab40-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ab40-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ab40-116">Requirements</span></span>



| <span data-ttu-id="1ab40-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ab40-117">Requirement</span></span> | <span data-ttu-id="1ab40-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1ab40-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab40-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ab40-119">Header</span></span><br/> | <dl> <span data-ttu-id="1ab40-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ab40-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ab40-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ab40-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab40-122">**\_ \_ \_ ID protezione output audio \_ DRM \_ es.**</span><span class="sxs-lookup"><span data-stu-id="1ab40-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="1ab40-123">**\_ID di \_ protezione dell'output del video DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1ab40-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="1ab40-124">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="1ab40-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





