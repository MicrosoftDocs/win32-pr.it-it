---
description: Il \_ \_ tipo di enumerazione modalità di acquisizione WPD descrive la modalità di temporizzazione di acquisizione di un'acquisizione di immagini ancora.
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: Enumerazione WPD_CAPTURE_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326584"
---
# <a name="wpd_capture_modes-enumeration"></a><span data-ttu-id="5eaaf-103">\_Enumerazione modalità di acquisizione WPD \_</span><span class="sxs-lookup"><span data-stu-id="5eaaf-103">WPD\_CAPTURE\_MODES enumeration</span></span>

<span data-ttu-id="5eaaf-104">Il tipo di enumerazione **\_ \_ modalità di acquisizione WPD** descrive la modalità di temporizzazione di acquisizione di un'acquisizione di immagini ancora.</span><span class="sxs-lookup"><span data-stu-id="5eaaf-104">The **WPD\_CAPTURE\_MODES** enumeration type describes the capture timing mode of a still image capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eaaf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5eaaf-105">Syntax</span></span>


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="5eaaf-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="5eaaf-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5eaaf-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**modalità di acquisizione WPD non \_ \_ \_ definita**</span><span class="sxs-lookup"><span data-stu-id="5eaaf-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**WPD\_CAPTURE\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="5eaaf-108">La modalità di acquisizione non è stata definita.</span><span class="sxs-lookup"><span data-stu-id="5eaaf-108">The capture mode has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="5eaaf-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**\_modalità di acquisizione WPD \_ \_ normale**</span><span class="sxs-lookup"><span data-stu-id="5eaaf-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**WPD\_CAPTURE\_MODE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="5eaaf-110">Non è necessario utilizzare la modalità di ritardo o di scatto.</span><span class="sxs-lookup"><span data-stu-id="5eaaf-110">No delay or burst mode should be used.</span></span>

</dd> <dt>

<span data-ttu-id="5eaaf-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**\_modalità di acquisizione WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5eaaf-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**WPD\_CAPTURE\_MODE\_BURST**</span></span>
</dt> <dd>

<span data-ttu-id="5eaaf-112">Specifica che un numero definito di immagini deve essere acquisito con un intervallo definito tra di essi.</span><span class="sxs-lookup"><span data-stu-id="5eaaf-112">Specifies that a defined number of images should be captured with a defined interval between them.</span></span> <span data-ttu-id="5eaaf-113">Il numero di immagini da acquisire e l'intervallo di tempo tra di essi vengono specificate dalle proprietà [WPD \_ still \_ Image \_ \_ numero di picchi](still-image-properties.md) e [WPD \_ still \_ Image \_ \_ ](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="5eaaf-113">The number of images to capture and time delay between them are specified by the [WPD\_STILL\_IMAGE\_BURST\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_BURST\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="5eaaf-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**\_modalità di acquisizione WPD \_ \_ timelapse**</span><span class="sxs-lookup"><span data-stu-id="5eaaf-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**WPD\_CAPTURE\_MODE\_TIMELAPSE**</span></span>
</dt> <dd>

<span data-ttu-id="5eaaf-115">L'acquisizione di immagini deve usare la fotografia time lapse.</span><span class="sxs-lookup"><span data-stu-id="5eaaf-115">Image capture should use time lapse photography.</span></span> <span data-ttu-id="5eaaf-116">Il numero di immagini e l'intervallo tra di essi è descritto dalle proprietà [WPD \_ still \_ Image \_ timelapse \_ Number](still-image-properties.md) e [WPD \_ still \_ Image \_ timelapse \_ Interval](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="5eaaf-116">The number of images and interval between them are described by the [WPD\_STILL\_IMAGE\_TIMELAPSE\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_TIMELAPSE\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5eaaf-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5eaaf-117">Remarks</span></span>

<span data-ttu-id="5eaaf-118">Questa enumerazione viene utilizzata dalla proprietà [WPD \_ still \_ Image \_ Capture \_ mode](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="5eaaf-118">This enumeration is used by the [WPD\_STILL\_IMAGE\_CAPTURE\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eaaf-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5eaaf-119">Requirements</span></span>



| <span data-ttu-id="5eaaf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eaaf-120">Requirement</span></span> | <span data-ttu-id="5eaaf-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5eaaf-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eaaf-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5eaaf-122">Header</span></span><br/> | <dl> <span data-ttu-id="5eaaf-123"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eaaf-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eaaf-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5eaaf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eaaf-125">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="5eaaf-125">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="5eaaf-126">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="5eaaf-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




