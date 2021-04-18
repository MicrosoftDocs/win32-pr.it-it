---
description: Il \_ tipo di enumerazione WPD Flash Modes \_ descrive una modalità flash da usare durante l'acquisizione di immagini con un dispositivo.
ms.assetid: 4e92c86d-2f35-4bc6-8d37-ec1ab5c518b2
title: Enumerazione WPD_FLASH_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FLASH_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 09a2a5b95e86d9d17267cafcfbf723e734ffc74f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328966"
---
# <a name="wpd_flash_modes-enumeration"></a><span data-ttu-id="dda11-103">\_Enumerazione delle \_ modalità flash WPD</span><span class="sxs-lookup"><span data-stu-id="dda11-103">WPD\_FLASH\_MODES enumeration</span></span>

<span data-ttu-id="dda11-104">Il tipo di enumerazione **WPD \_ Flash \_** Modes descrive una modalità flash da usare durante l'acquisizione di immagini con un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dda11-104">The **WPD\_FLASH\_MODES** enumeration type describes a flash mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="dda11-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dda11-105">Syntax</span></span>


```C++
typedef enum WPD_FLASH_MODES { 
  WPD_FLASH_MODE_UNDEFINED      = 0,
  WPD_FLASH_MODE_AUTO           = 1,
  WPD_FLASH_MODE_OFF            = 2,
  WPD_FLASH_MODE_FILL           = 3,
  WPD_FLASH_MODE_RED_EYE_AUTO   = 4,
  WPD_FLASH_MODE_RED_EYE_FILL   = 5,
  WPD_FLASH_MODE_EXTERNAL_SYNC  = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="dda11-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="dda11-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dda11-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**\_modalità flash WPD non \_ \_ definita**</span><span class="sxs-lookup"><span data-stu-id="dda11-107"><span id="WPD_FLASH_MODE_UNDEFINED"></span><span id="wpd_flash_mode_undefined"></span>**WPD\_FLASH\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="dda11-108">Non è stata specificata alcuna modalità flash.</span><span class="sxs-lookup"><span data-stu-id="dda11-108">No flash mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="dda11-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**WPD \_ \_ modalità Flash \_ automatica**</span><span class="sxs-lookup"><span data-stu-id="dda11-109"><span id="WPD_FLASH_MODE_AUTO"></span><span id="wpd_flash_mode_auto"></span>**WPD\_FLASH\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="dda11-110">Specifica che il flash deve essere usato in modalità automatica, come specificato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dda11-110">Specifies that the flash should be used in the automatic mode, as specified by the device.</span></span>

</dd> <dt>

<span data-ttu-id="dda11-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**\_modalità Flash \_ WPD \_ disabilitata**</span><span class="sxs-lookup"><span data-stu-id="dda11-111"><span id="WPD_FLASH_MODE_OFF"></span><span id="wpd_flash_mode_off"></span>**WPD\_FLASH\_MODE\_OFF**</span></span>
</dt> <dd>

<span data-ttu-id="dda11-112">Specifica che non deve essere utilizzato alcun flash.</span><span class="sxs-lookup"><span data-stu-id="dda11-112">Specifies that no flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="dda11-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**\_ \_ riempimento modalità Flash \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="dda11-113"><span id="WPD_FLASH_MODE_FILL"></span><span id="wpd_flash_mode_fill"></span>**WPD\_FLASH\_MODE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="dda11-114">Specifica un flash di tipo Fill.</span><span class="sxs-lookup"><span data-stu-id="dda11-114">Specifies a fill-type flash.</span></span>

</dd> <dt>

<span data-ttu-id="dda11-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD \_ in \_ modalità \_ Flash \_ automatico a occhi rossi \_**</span><span class="sxs-lookup"><span data-stu-id="dda11-115"><span id="WPD_FLASH_MODE_RED_EYE_AUTO"></span><span id="wpd_flash_mode_red_eye_auto"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="dda11-116">Specifica che deve essere usato il flash di riduzione degli occhi rossi.</span><span class="sxs-lookup"><span data-stu-id="dda11-116">Specifies that the red eye reduction flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="dda11-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**\_riempimento a \_ \_ occhi rossi \_ in modalità flash WPD \_**</span><span class="sxs-lookup"><span data-stu-id="dda11-117"><span id="WPD_FLASH_MODE_RED_EYE_FILL"></span><span id="wpd_flash_mode_red_eye_fill"></span>**WPD\_FLASH\_MODE\_RED\_EYE\_FILL**</span></span>
</dt> <dd>

<span data-ttu-id="dda11-118">Specifica che deve essere usato il flash di riempimento a occhi rossi.</span><span class="sxs-lookup"><span data-stu-id="dda11-118">Specifies that the red eye fill flash should be used.</span></span>

</dd> <dt>

<span data-ttu-id="dda11-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**\_ \_ sincronizzazione esterna in modalità Flash \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="dda11-119"><span id="WPD_FLASH_MODE_EXTERNAL_SYNC"></span><span id="wpd_flash_mode_external_sync"></span>**WPD\_FLASH\_MODE\_EXTERNAL\_SYNC**</span></span>
</dt> <dd>

<span data-ttu-id="dda11-120">Specifica che il flash deve essere sincronizzato con altri dispositivi flash esterni.</span><span class="sxs-lookup"><span data-stu-id="dda11-120">Specifies that the flash should be synchronized with other external flash devices.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dda11-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="dda11-121">Remarks</span></span>

<span data-ttu-id="dda11-122">Questa enumerazione viene utilizzata dalla proprietà [WPD \_ still \_ Image \_ Flash \_ mode](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="dda11-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_FLASH\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="dda11-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dda11-123">Requirements</span></span>



| <span data-ttu-id="dda11-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dda11-124">Requirement</span></span> | <span data-ttu-id="dda11-125">Valore</span><span class="sxs-lookup"><span data-stu-id="dda11-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dda11-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dda11-126">Header</span></span><br/> | <dl> <span data-ttu-id="dda11-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="dda11-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dda11-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dda11-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dda11-129">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="dda11-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




