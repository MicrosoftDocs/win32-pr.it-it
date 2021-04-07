---
title: Messaggio di EM_SETCTFOPENSTATUS (RichEdit. h)
description: Apre o chiude la tastiera di Text Services Framework (TSF).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- Controlli di Windows Message EM_SETCTFOPENSTATUS
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4163a415f129dfc5d3f98aa06578d13bb462e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048655"
---
# <a name="em_setctfopenstatus-message"></a><span data-ttu-id="af282-104">\_Messaggio SETCTFOPENSTATUS em</span><span class="sxs-lookup"><span data-stu-id="af282-104">EM\_SETCTFOPENSTATUS message</span></span>

<span data-ttu-id="af282-105">Apre o chiude la tastiera di Text Services Framework (TSF).</span><span class="sxs-lookup"><span data-stu-id="af282-105">Opens or closes the Text Services Framework (TSF) keyboard.</span></span>

## <a name="parameters"></a><span data-ttu-id="af282-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="af282-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af282-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af282-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af282-108">Per attivare la tastiera TSF, utilizzare **true**.</span><span class="sxs-lookup"><span data-stu-id="af282-108">To turn on the TSF keyboard, use **TRUE**.</span></span> <span data-ttu-id="af282-109">Per disattivare la tastiera TSF, utilizzare **false**.</span><span class="sxs-lookup"><span data-stu-id="af282-109">To turn off the TSF keyboard, use **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="af282-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af282-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af282-111">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="af282-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af282-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af282-112">Return value</span></span>

<span data-ttu-id="af282-113">In caso di esito positivo, il messaggio restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="af282-113">If successful, this message returns **TRUE**.</span></span> <span data-ttu-id="af282-114">Se ha esito negativo, il messaggio restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="af282-114">If unsuccessful, this message returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="af282-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af282-115">Requirements</span></span>



| <span data-ttu-id="af282-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="af282-116">Requirement</span></span> | <span data-ttu-id="af282-117">Valore</span><span class="sxs-lookup"><span data-stu-id="af282-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af282-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af282-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af282-119">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="af282-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af282-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af282-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af282-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af282-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af282-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af282-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="af282-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="af282-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af282-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af282-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af282-125">**\_GETCTFOPENSTATUS em**</span><span class="sxs-lookup"><span data-stu-id="af282-125">**EM\_GETCTFOPENSTATUS**</span></span>](em-getctfopenstatus.md)
</dt> </dl>

 

 





