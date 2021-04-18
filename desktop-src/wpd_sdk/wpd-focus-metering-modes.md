---
description: Il \_ tipo di enumerazione modalità di misurazione dello stato attivo WPD \_ descrive il \_ modo in cui un dispositivo deve decidere quale parte di un frame utilizzare per impostare lo stato attivo.
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: Enumerazione WPD_FOCUS_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f59d6a2f1cabbbe7b072a87caa3e5d74d012fc49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328965"
---
# <a name="wpd_focus_metering_modes-enumeration"></a><span data-ttu-id="04b9c-103">\_Enumerazione delle \_ modalità di misurazione dello stato attivo WPD \_</span><span class="sxs-lookup"><span data-stu-id="04b9c-103">WPD\_FOCUS\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="04b9c-104">Il tipo di enumerazione **\_ modalità di \_ misurazione \_ dello stato attivo WPD** descrive il modo in cui un dispositivo deve decidere quale parte di un frame utilizzare per impostare lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="04b9c-104">The **WPD\_FOCUS\_METERING\_MODES** enumeration type describes how a device should decide what part of a frame to use to set focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b9c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04b9c-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="04b9c-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="04b9c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="04b9c-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**\_modalità di misurazione dello stato attivo WPD non \_ \_ \_ definita**</span><span class="sxs-lookup"><span data-stu-id="04b9c-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**WPD\_FOCUS\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="04b9c-108">Indica che non è stata specificata alcuna modalità di messa a fuoco.</span><span class="sxs-lookup"><span data-stu-id="04b9c-108">Indicates that no focusing mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="04b9c-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**\_ \_ \_ punto centrale della modalità di misurazione dello \_ stato attivo \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="04b9c-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="04b9c-110">Si concentra sul centro dell'area incorniciata.</span><span class="sxs-lookup"><span data-stu-id="04b9c-110">Focuses on the center of the framed area.</span></span>

</dd> <dt>

<span data-ttu-id="04b9c-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**\_modalità di misurazione dello stato attivo WPD \_ \_ \_ \_ multispot**</span><span class="sxs-lookup"><span data-stu-id="04b9c-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="04b9c-112">Determinare lo stato attivo analizzando più parti dell'area incorniciata.</span><span class="sxs-lookup"><span data-stu-id="04b9c-112">Determine focus by analyzing multiple parts of the framed area.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04b9c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="04b9c-113">Remarks</span></span>

<span data-ttu-id="04b9c-114">Questa enumerazione viene specificata dalla proprietà della [modalità di misurazione dello stato di WPD \_ still \_ Image \_ \_ \_ ](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="04b9c-114">This enumeration is specified by the [WPD\_STILL\_IMAGE\_FOCUS\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b9c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04b9c-115">Requirements</span></span>



| <span data-ttu-id="04b9c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="04b9c-116">Requirement</span></span> | <span data-ttu-id="04b9c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="04b9c-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="04b9c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04b9c-118">Header</span></span><br/> | <dl> <span data-ttu-id="04b9c-119"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="04b9c-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04b9c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04b9c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b9c-121">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="04b9c-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




