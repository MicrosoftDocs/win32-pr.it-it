---
title: Struttura WMDRM_OUTPUT_PROTECTION_LEVELS (wmdrmsdk. h)
description: La \_ struttura dei \_ livelli di protezione dell'output \_ di WMDRM contiene i livelli di protezione dell'output (OPLs) richiesti da una licenza per eseguire varie azioni.
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- Formato di Windows Media per la struttura WMDRM_OUTPUT_PROTECTION_LEVELS
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d720a8aef42178da188b71a1635d97031b138397
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326598"
---
# <a name="wmdrm_output_protection_levels-structure"></a><span data-ttu-id="20713-105">\_Struttura del \_ livello di protezione dell'output WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="20713-105">WMDRM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="20713-106">La struttura dei livelli di protezione dell'output di WMDRM contiene i livelli di protezione dell'output (OPLs) richiesti da una licenza per eseguire varie azioni. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="20713-106">The **WMDRM\_OUTPUT\_PROTECTION\_LEVELS** structure contains the output protections levels (OPLs) required by a license to perform various actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="20713-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20713-107">Syntax</span></span>


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
} ;
```



## <a name="members"></a><span data-ttu-id="20713-108">Members</span><span class="sxs-lookup"><span data-stu-id="20713-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="20713-109">**wCompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="20713-109">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="20713-110">Numero minimo di OPL necessari per la ricezione di video digitali compressi.</span><span class="sxs-lookup"><span data-stu-id="20713-110">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="20713-111">**wUncompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="20713-111">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="20713-112">Numero minimo di OPL necessari per la ricezione di video digitali non compressi.</span><span class="sxs-lookup"><span data-stu-id="20713-112">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="20713-113">**wAnalogVideo**</span><span class="sxs-lookup"><span data-stu-id="20713-113">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="20713-114">Numero minimo di OPL necessari per la ricezione di video analogici.</span><span class="sxs-lookup"><span data-stu-id="20713-114">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="20713-115">**wCompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="20713-115">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="20713-116">OPL minime necessarie per ricevere audio digitale compresso.</span><span class="sxs-lookup"><span data-stu-id="20713-116">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="20713-117">**wUncompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="20713-117">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="20713-118">OPL minime necessarie per ricevere audio digitale non compresso.</span><span class="sxs-lookup"><span data-stu-id="20713-118">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="20713-119">**wMinimumCopyProtectionLevel**</span><span class="sxs-lookup"><span data-stu-id="20713-119">**wMinimumCopyProtectionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="20713-120">OPL minimo necessario per copiare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="20713-120">Minimum OPL required to copy the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20713-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="20713-121">Remarks</span></span>

<span data-ttu-id="20713-122">Questa struttura viene utilizzata dal metodo [**IWMDRMLicense:: GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) .</span><span class="sxs-lookup"><span data-stu-id="20713-122">This structure is used by the [**IWMDRMLicense::GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="20713-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20713-123">Requirements</span></span>



| <span data-ttu-id="20713-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="20713-124">Requirement</span></span> | <span data-ttu-id="20713-125">Valore</span><span class="sxs-lookup"><span data-stu-id="20713-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20713-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20713-126">Header</span></span><br/> | <dl> <span data-ttu-id="20713-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="20713-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20713-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20713-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20713-129">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="20713-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





