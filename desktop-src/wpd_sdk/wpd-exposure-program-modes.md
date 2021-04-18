---
description: Il \_ \_ tipo di enumerazione WPD Exposure Program Modes \_ descrive una modalità di esposizione da usare per l'acquisizione di immagini con un dispositivo.
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: Enumerazione WPD_EXPOSURE_PROGRAM_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_PROGRAM_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a88ce90bb9e776cd45245b32a363635c2ccf0560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328968"
---
# <a name="wpd_exposure_program_modes-enumeration"></a><span data-ttu-id="f54aa-103">\_Enumerazione WPD Exposure \_ Program \_ modes</span><span class="sxs-lookup"><span data-stu-id="f54aa-103">WPD\_EXPOSURE\_PROGRAM\_MODES enumeration</span></span>

<span data-ttu-id="f54aa-104">Il tipo di enumerazione **WPD \_ Exposure \_ Program \_** Modes descrive una modalità di esposizione da usare per l'acquisizione di immagini con un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f54aa-104">The **WPD\_EXPOSURE\_PROGRAM\_MODES** enumeration type describes an exposure mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f54aa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f54aa-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_PROGRAM_MODES { 
  WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED          = 0,
  WPD_EXPOSURE_PROGRAM_MODE_MANUAL             = 1,
  WPD_EXPOSURE_PROGRAM_MODE_AUTO               = 2,
  WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY  = 3,
  WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY   = 4,
  WPD_EXPOSURE_PROGRAM_MODE_CREATIVE           = 5,
  WPD_EXPOSURE_PROGRAM_MODE_ACTION             = 6,
  WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT           = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="f54aa-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="f54aa-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f54aa-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**\_modalità programma esposizione WPD non \_ \_ \_ definita**</span><span class="sxs-lookup"><span data-stu-id="f54aa-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="f54aa-108">La modalità di esposizione non è stata specificata.</span><span class="sxs-lookup"><span data-stu-id="f54aa-108">The exposure mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="f54aa-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**\_ \_ \_ manuale modalità programma esposizione \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="f54aa-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="f54aa-110">L'applicazione deve specificare tutte le impostazioni di esposizione.</span><span class="sxs-lookup"><span data-stu-id="f54aa-110">The application should specify all exposure settings.</span></span>

</dd> <dt>

<span data-ttu-id="f54aa-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**\_ \_ modalità programma esposizione \_ WPD \_ auto**</span><span class="sxs-lookup"><span data-stu-id="f54aa-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="f54aa-112">Usare una modalità di esposizione automatica definita dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f54aa-112">Use a device-defined automatic exposure mode.</span></span>

</dd> <dt>

<span data-ttu-id="f54aa-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**\_priorità di \_ \_ apertura della modalità programma WPD Exposure \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f54aa-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_APERTURE\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="f54aa-114">Modalità di esposizione automatica che indica che il valore di apertura della lente deve rimanere fisso, ma la velocità dell'otturatore deve essere determinata dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f54aa-114">An automated exposure mode that indicates that the lens aperture value should remain fixed, but shutter speed should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="f54aa-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**\_priorità di \_ \_ Shutter della modalità programma WPD Exposure \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f54aa-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_SHUTTER\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="f54aa-116">Modalità di esposizione automatica che indica che la velocità dell'otturatore deve rimanere fissa, ma tale apertura della lente dovrebbe essere determinata dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f54aa-116">An automated exposure mode that indicates that the shutter speed should remain fixed, but that lens aperture should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="f54aa-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**\_creazione della \_ \_ modalità programma esposizione WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f54aa-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_CREATIVE**</span></span>
</dt> <dd>

<span data-ttu-id="f54aa-118">Modalità di esposizione automatica che tenta di ottimizzare la profondità del campo.</span><span class="sxs-lookup"><span data-stu-id="f54aa-118">An automated exposure mode that tries to maximize the depth of field.</span></span>

</dd> <dt>

<span data-ttu-id="f54aa-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**\_ \_ \_ azione modalità programma esposizione \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="f54aa-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_ACTION**</span></span>
</dt> <dd>

<span data-ttu-id="f54aa-120">Modalità di esposizione automatica che tenta di massimizzare la velocità dell'otturatore.</span><span class="sxs-lookup"><span data-stu-id="f54aa-120">An automated exposure mode that tries to maximize the shutter speed.</span></span>

</dd> <dt>

<span data-ttu-id="f54aa-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**\_ \_ \_ verticale modalità programma esposizione \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="f54aa-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_PORTRAIT**</span></span>
</dt> <dd>

<span data-ttu-id="f54aa-122">Modalità di esposizione automatica che specifica una profondità relativamente superficiale del campo.</span><span class="sxs-lookup"><span data-stu-id="f54aa-122">An automated exposure mode that specifies a relatively shallow depth of field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f54aa-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f54aa-123">Remarks</span></span>

<span data-ttu-id="f54aa-124">Indica la modalità del programma di esposizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f54aa-124">Indicates the exposure program mode of the device.</span></span> <span data-ttu-id="f54aa-125">Questa enumerazione viene utilizzata dalla proprietà [ \_ \_ \_ \_ \_ modalità programma WPD Still Image Exposure](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="f54aa-125">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_PROGRAM\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f54aa-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f54aa-126">Requirements</span></span>



| <span data-ttu-id="f54aa-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f54aa-127">Requirement</span></span> | <span data-ttu-id="f54aa-128">Valore</span><span class="sxs-lookup"><span data-stu-id="f54aa-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f54aa-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f54aa-129">Header</span></span><br/> | <dl> <span data-ttu-id="f54aa-130"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="f54aa-130"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f54aa-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f54aa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f54aa-132">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="f54aa-132">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




