---
title: Maschera di penna
description: Valori che possono essere visualizzati nel campo penMask della struttura POINTER_PEN_INFO.
ms.assetid: 6A44B701-55E1-41D4-9C4A-807E57441DA4
topic_type:
- apiref
api_name:
- PEN_MASK_NONE
- PEN_MASK_PRESSURE
- PEN_MASK_ROTATION
- PEN_MASK_TILT_X
- PEN_MASK_TILT_Y
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bd181b5eafbe1cf6de56c95886deb04e5bd6d2b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120359"
---
# <a name="pen-mask"></a><span data-ttu-id="9ecdf-103">Maschera di penna</span><span class="sxs-lookup"><span data-stu-id="9ecdf-103">Pen Mask</span></span>

<span data-ttu-id="9ecdf-104">Valori che possono essere visualizzati nel campo **penMask** della struttura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="9ecdf-104">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="9ecdf-105"><span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**</span><span class="sxs-lookup"><span data-stu-id="9ecdf-105"><span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecdf-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ecdf-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="9ecdf-107">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="9ecdf-107">Default.</span></span> <span data-ttu-id="9ecdf-108">Nessuno dei campi facoltativi è valido.</span><span class="sxs-lookup"><span data-stu-id="9ecdf-108">None of the optional fields are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecdf-109"><span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**</span><span class="sxs-lookup"><span data-stu-id="9ecdf-109"><span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecdf-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9ecdf-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="9ecdf-111">la **pressione** della struttura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) è valida.</span><span class="sxs-lookup"><span data-stu-id="9ecdf-111">**pressure** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecdf-112"><span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**</span><span class="sxs-lookup"><span data-stu-id="9ecdf-112"><span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecdf-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9ecdf-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="9ecdf-114">la **rotazione** della struttura del [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) è valida.</span><span class="sxs-lookup"><span data-stu-id="9ecdf-114">**rotation** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecdf-115"><span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X**</span><span class="sxs-lookup"><span data-stu-id="9ecdf-115"><span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecdf-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9ecdf-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="9ecdf-117">**tiltX** della struttura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) è valido.</span><span class="sxs-lookup"><span data-stu-id="9ecdf-117">**tiltX** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9ecdf-118"><span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**</span><span class="sxs-lookup"><span data-stu-id="9ecdf-118"><span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ecdf-119">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9ecdf-119">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="9ecdf-120">l' **inclinazione** della struttura del [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) è valida.</span><span class="sxs-lookup"><span data-stu-id="9ecdf-120">**tiltY** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ecdf-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ecdf-121">Requirements</span></span>



| <span data-ttu-id="9ecdf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ecdf-122">Requirement</span></span> | <span data-ttu-id="9ecdf-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9ecdf-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9ecdf-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ecdf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9ecdf-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9ecdf-125">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9ecdf-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ecdf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9ecdf-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9ecdf-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9ecdf-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ecdf-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ecdf-129"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ecdf-129"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ecdf-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ecdf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ecdf-131">Costanti</span><span class="sxs-lookup"><span data-stu-id="9ecdf-131">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="9ecdf-132">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="9ecdf-132">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





