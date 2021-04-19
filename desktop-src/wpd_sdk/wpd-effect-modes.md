---
description: Il \_ \_ tipo di enumerazione WPD Effect Modes descrive vari effetti visivi che possono essere applicati a un'immagine.
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: Enumerazione WPD_EFFECT_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7e29f89207a74d335fbe1c2561f8dcf9cec3e923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324205"
---
# <a name="wpd_effect_modes-enumeration"></a><span data-ttu-id="77639-103">\_Enumerazione WPD Effect \_ modes</span><span class="sxs-lookup"><span data-stu-id="77639-103">WPD\_EFFECT\_MODES enumeration</span></span>

<span data-ttu-id="77639-104">Il tipo di enumerazione **WPD \_ Effect \_ modes** descrive vari effetti visivi che possono essere applicati a un'immagine.</span><span class="sxs-lookup"><span data-stu-id="77639-104">The **WPD\_EFFECT\_MODES** enumeration type describes various visual effects that can be applied to an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="77639-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77639-105">Syntax</span></span>


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="77639-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="77639-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="77639-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**\_modalità effetto WPD non \_ \_ definita**</span><span class="sxs-lookup"><span data-stu-id="77639-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**WPD\_EFFECT\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="77639-108">Nessun effetto specificato.</span><span class="sxs-lookup"><span data-stu-id="77639-108">No effect has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="77639-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**\_ \_ colore modalità effetto \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="77639-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**WPD\_EFFECT\_MODE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="77639-110">L'immagine deve essere color.</span><span class="sxs-lookup"><span data-stu-id="77639-110">The image should be color.</span></span>

</dd> <dt>

<span data-ttu-id="77639-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**\_modalità effetto WPD in \_ \_ \_ \_ bianco e nero**</span><span class="sxs-lookup"><span data-stu-id="77639-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**WPD\_EFFECT\_MODE\_BLACK\_AND\_WHITE**</span></span>
</dt> <dd>

<span data-ttu-id="77639-112">L'immagine deve essere nera e bianca.</span><span class="sxs-lookup"><span data-stu-id="77639-112">The image should be black and white.</span></span>

</dd> <dt>

<span data-ttu-id="77639-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**\_ \_ seppia modalità effetto \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="77639-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**WPD\_EFFECT\_MODE\_SEPIA**</span></span>
</dt> <dd>

<span data-ttu-id="77639-114">L'immagine deve essere di seppia.</span><span class="sxs-lookup"><span data-stu-id="77639-114">The image should be sepia.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77639-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="77639-115">Remarks</span></span>

<span data-ttu-id="77639-116">Questa enumerazione viene utilizzata dalla proprietà [WPD \_ still \_ Image \_ Effect \_ mode](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="77639-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_EFFECT\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="77639-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77639-117">Requirements</span></span>



| <span data-ttu-id="77639-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="77639-118">Requirement</span></span> | <span data-ttu-id="77639-119">Valore</span><span class="sxs-lookup"><span data-stu-id="77639-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="77639-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77639-120">Header</span></span><br/> | <dl> <span data-ttu-id="77639-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="77639-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77639-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77639-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77639-123">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="77639-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




