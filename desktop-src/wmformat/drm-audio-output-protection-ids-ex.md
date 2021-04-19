---
title: Struttura DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX (wmdrmsdk. h)
description: La \_ \_ \_ \_ struttura ad esempio ID protezione output audio DRM \_ contiene un elenco di identificatori di protezione dell'output audio. Questa struttura estende gli \_ \_ \_ ID protezione dell'output audio DRM \_ aggiungendo un numero di versione.
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- Formato di Windows Media per la struttura DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb687b5600e75f845c2d980f73f3b8c2eeda970a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332288"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a><span data-ttu-id="d7ba9-106">\_ \_ ID protezione output audio DRM- \_ \_ \_ struttura ex</span><span class="sxs-lookup"><span data-stu-id="d7ba9-106">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="d7ba9-107">La struttura ad **\_ \_ \_ \_ \_ esempio ID protezione output audio DRM** contiene un elenco di identificatori di protezione dell'output audio.</span><span class="sxs-lookup"><span data-stu-id="d7ba9-107">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX** structure contains a list of audio output protection identifiers.</span></span> <span data-ttu-id="d7ba9-108">Questa struttura estende **gli \_ \_ \_ \_ ID protezione dell'output audio DRM** aggiungendo un numero di versione.</span><span class="sxs-lookup"><span data-stu-id="d7ba9-108">This structure extends **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ba9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7ba9-109">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION_EX *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="d7ba9-110">Members</span><span class="sxs-lookup"><span data-stu-id="d7ba9-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7ba9-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="d7ba9-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d7ba9-112">Numero di versione.</span><span class="sxs-lookup"><span data-stu-id="d7ba9-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="d7ba9-113">**Centri di**</span><span class="sxs-lookup"><span data-stu-id="d7ba9-113">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="d7ba9-114">Numero di voci nella matrice **rgAop** .</span><span class="sxs-lookup"><span data-stu-id="d7ba9-114">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="d7ba9-115">**rgAop**</span><span class="sxs-lookup"><span data-stu-id="d7ba9-115">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="d7ba9-116">Matrice di **strutture \_ \_ \_ \_ ex protezione output audio DRM** .</span><span class="sxs-lookup"><span data-stu-id="d7ba9-116">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="d7ba9-117">**DRM \_ La \_ Protezione output audio \_ \_ ex** è un tipo definito [**come \_ protezione dell'output \_ \_ DRM**](drm-output-protection-ex.md), ad esempio.</span><span class="sxs-lookup"><span data-stu-id="d7ba9-117">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7ba9-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7ba9-118">Remarks</span></span>

<span data-ttu-id="d7ba9-119">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="d7ba9-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7ba9-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7ba9-120">Requirements</span></span>



| <span data-ttu-id="d7ba9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7ba9-121">Requirement</span></span> | <span data-ttu-id="d7ba9-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d7ba9-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ba9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7ba9-123">Header</span></span><br/> | <dl> <span data-ttu-id="d7ba9-124"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ba9-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7ba9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7ba9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ba9-126">**\_ID di \_ protezione dell'output audio \_ DRM \_**</span><span class="sxs-lookup"><span data-stu-id="d7ba9-126">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="d7ba9-127">**\_ \_ \_ ID protezione output video \_ DRM \_ es.**</span><span class="sxs-lookup"><span data-stu-id="d7ba9-127">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="d7ba9-128">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="d7ba9-128">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





