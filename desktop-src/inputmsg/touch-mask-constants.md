---
title: Touch mask
description: Valori che possono essere visualizzati nel campo touchMask della struttura POINTER_TOUCH_INFO.
ms.assetid: 23AD50C8-C769-48D6-9F27-DB2755C03D5C
topic_type:
- apiref
api_name:
- TOUCH_MASK_NONE
- TOUCH_MASK_CONTACTAREA
- TOUCH_MASK_ORIENTATION
- TOUCH_MASK_PRESSURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5ac389894d9096b389af127685feb9a2d81756ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478754"
---
# <a name="touch-mask"></a><span data-ttu-id="7e060-103">Touch mask</span><span class="sxs-lookup"><span data-stu-id="7e060-103">Touch Mask</span></span>

<span data-ttu-id="7e060-104">Valori che possono essere visualizzati nel campo **touchMask** della struttura [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="7e060-104">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="7e060-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span><span class="sxs-lookup"><span data-stu-id="7e060-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e060-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e060-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="7e060-107">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7e060-107">Default.</span></span> <span data-ttu-id="7e060-108">Nessuno dei campi facoltativi è valido.</span><span class="sxs-lookup"><span data-stu-id="7e060-108">None of the optional fields are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7e060-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span><span class="sxs-lookup"><span data-stu-id="7e060-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e060-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7e060-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="7e060-111">**rcContact** della struttura [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) è valido.</span><span class="sxs-lookup"><span data-stu-id="7e060-111">**rcContact** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7e060-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span><span class="sxs-lookup"><span data-stu-id="7e060-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e060-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7e060-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="7e060-114">l' **orientamento** della struttura del [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) è valido.</span><span class="sxs-lookup"><span data-stu-id="7e060-114">**orientation** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7e060-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span><span class="sxs-lookup"><span data-stu-id="7e060-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e060-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7e060-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="7e060-117">la **pressione** della struttura [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) è valida.</span><span class="sxs-lookup"><span data-stu-id="7e060-117">**pressure** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e060-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e060-118">Requirements</span></span>



| <span data-ttu-id="7e060-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e060-119">Requirement</span></span> | <span data-ttu-id="7e060-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7e060-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7e060-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e060-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7e060-122">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7e060-122">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7e060-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7e060-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7e060-124">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7e060-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7e060-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e060-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e060-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e060-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e060-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e060-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e060-128">Costanti</span><span class="sxs-lookup"><span data-stu-id="7e060-128">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="7e060-129">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="7e060-129">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





