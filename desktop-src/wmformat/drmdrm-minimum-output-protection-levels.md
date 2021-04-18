---
title: Struttura DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS (wmdrmsdk. h)
description: La \_ struttura dei livelli di protezione dell'output minimo DRM \_ \_ \_ include i livelli minimi di protezione dell'output (OPLs) per la riproduzione di diversi tipi di contenuto. Un dispositivo deve supportare il OPL minimo per un tipo di dati per ricevere il tipo di dati dal lettore.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- Formato di Windows Media per la struttura DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060fdda4cd1c3cc665e396a72d46ac05e721abe4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324454"
---
# <a name="drm_minimum_output_protection_levels-structure"></a><span data-ttu-id="8349c-106">\_Struttura del \_ \_ livello di protezione dell'output minimo DRM \_</span><span class="sxs-lookup"><span data-stu-id="8349c-106">DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="8349c-107">La struttura dei **\_ livelli di \_ \_ protezione \_ dell'output minimo DRM** include i livelli minimi di protezione dell'output (OPLs) per la riproduzione di diversi tipi di contenuto.</span><span class="sxs-lookup"><span data-stu-id="8349c-107">The **DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS** structure holds the minimum output protection levels (OPLs) for playback of various types of content.</span></span> <span data-ttu-id="8349c-108">Un dispositivo deve supportare il OPL minimo per un tipo di dati per ricevere il tipo di dati dal lettore.</span><span class="sxs-lookup"><span data-stu-id="8349c-108">A device must support the minimum OPL for a type of data to receive that type of data from the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="8349c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8349c-109">Syntax</span></span>


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a><span data-ttu-id="8349c-110">Members</span><span class="sxs-lookup"><span data-stu-id="8349c-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="8349c-111">**wCompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="8349c-111">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="8349c-112">Numero minimo di OPL necessari per la ricezione di video digitali compressi.</span><span class="sxs-lookup"><span data-stu-id="8349c-112">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="8349c-113">**wUncompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="8349c-113">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="8349c-114">Numero minimo di OPL necessari per la ricezione di video digitali non compressi.</span><span class="sxs-lookup"><span data-stu-id="8349c-114">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="8349c-115">**wAnalogVideo**</span><span class="sxs-lookup"><span data-stu-id="8349c-115">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="8349c-116">Numero minimo di OPL necessari per la ricezione di video analogici.</span><span class="sxs-lookup"><span data-stu-id="8349c-116">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="8349c-117">**wCompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="8349c-117">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="8349c-118">OPL minime necessarie per ricevere audio digitale compresso.</span><span class="sxs-lookup"><span data-stu-id="8349c-118">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="8349c-119">**wUncompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="8349c-119">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="8349c-120">OPL minime necessarie per ricevere audio digitale non compresso.</span><span class="sxs-lookup"><span data-stu-id="8349c-120">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8349c-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="8349c-121">Remarks</span></span>

<span data-ttu-id="8349c-122">Questa struttura viene utilizzata come membro della struttura [**DRM \_ Play \_ OPL**](drmdrm-play-opl.md) .</span><span class="sxs-lookup"><span data-stu-id="8349c-122">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8349c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8349c-123">Requirements</span></span>



| <span data-ttu-id="8349c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8349c-124">Requirement</span></span> | <span data-ttu-id="8349c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8349c-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8349c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8349c-126">Header</span></span><br/> | <dl> <span data-ttu-id="8349c-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8349c-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8349c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8349c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8349c-129">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="8349c-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





