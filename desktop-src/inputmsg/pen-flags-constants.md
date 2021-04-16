---
title: Flag di penna
description: Valori che possono essere visualizzati nel campo penFlags della struttura POINTER_PEN_INFO.
ms.assetid: BC3CE568-4090-4451-B780-18530C988305
topic_type:
- apiref
api_name:
- PEN_FLAG_NONE
- PEN_FLAG_BARREL
- PEN_FLAG_INVERTED
- PEN_FLAG_ERASER
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: d7c28beaf58b6fa96bb8dd82b2dd650b2a7d6950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477950"
---
# <a name="pen-flags"></a><span data-ttu-id="8cae6-103">Flag di penna</span><span class="sxs-lookup"><span data-stu-id="8cae6-103">Pen Flags</span></span>

<span data-ttu-id="8cae6-104">Valori che possono essere visualizzati nel campo **penFlags** della struttura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="8cae6-104">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="8cae6-105"><span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**</span><span class="sxs-lookup"><span data-stu-id="8cae6-105"><span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cae6-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cae6-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="8cae6-107">Nessun flag di penna.</span><span class="sxs-lookup"><span data-stu-id="8cae6-107">There is no pen flag.</span></span> <span data-ttu-id="8cae6-108">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="8cae6-108">This is the default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cae6-109"><span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**</span><span class="sxs-lookup"><span data-stu-id="8cae6-109"><span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cae6-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8cae6-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="8cae6-111">Il pulsante Barrel è premuto.</span><span class="sxs-lookup"><span data-stu-id="8cae6-111">The barrel button is pressed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cae6-112"><span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**</span><span class="sxs-lookup"><span data-stu-id="8cae6-112"><span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cae6-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8cae6-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="8cae6-114">La penna è invertita.</span><span class="sxs-lookup"><span data-stu-id="8cae6-114">The pen is inverted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cae6-115"><span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**</span><span class="sxs-lookup"><span data-stu-id="8cae6-115"><span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8cae6-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="8cae6-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="8cae6-117">Viene premuto il pulsante della gomma.</span><span class="sxs-lookup"><span data-stu-id="8cae6-117">The eraser button is pressed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8cae6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8cae6-118">Requirements</span></span>



| <span data-ttu-id="8cae6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cae6-119">Requirement</span></span> | <span data-ttu-id="8cae6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8cae6-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8cae6-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cae6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8cae6-122">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8cae6-122">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8cae6-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cae6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8cae6-124">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8cae6-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8cae6-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8cae6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cae6-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cae6-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cae6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8cae6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cae6-128">Costanti</span><span class="sxs-lookup"><span data-stu-id="8cae6-128">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="8cae6-129">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="8cae6-129">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





