---
title: Messaggio RB_ENDDRAG (COMmctrl. h)
description: Termina l'operazione di trascinamento e rilascio del controllo Rebar. Questo messaggio non comporta l' \_ invio di una notifica RBN ENDDRAG.
ms.assetid: 4991dda6-32ea-4d3e-9d39-17c2b6995f09
keywords:
- Controlli di Windows Message RB_ENDDRAG
topic_type:
- apiref
api_name:
- RB_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b6f201471b6f260555aacb9d89c1363492ed6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964553"
---
# <a name="rb_enddrag-message"></a><span data-ttu-id="e6b8a-105">\_Messaggio ENDDRAG RB</span><span class="sxs-lookup"><span data-stu-id="e6b8a-105">RB\_ENDDRAG message</span></span>

<span data-ttu-id="e6b8a-106">Termina l'operazione di trascinamento e rilascio del controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="e6b8a-106">Terminates the rebar control's drag-and-drop operation.</span></span> <span data-ttu-id="e6b8a-107">Questo messaggio non comporta l'invio di una notifica [RBN \_ ENDDRAG](rbn-enddrag.md) .</span><span class="sxs-lookup"><span data-stu-id="e6b8a-107">This message does not cause an [RBN\_ENDDRAG](rbn-enddrag.md) notification to be sent.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6b8a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6b8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6b8a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6b8a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e6b8a-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e6b8a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e6b8a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6b8a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e6b8a-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e6b8a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6b8a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6b8a-113">Return value</span></span>

<span data-ttu-id="e6b8a-114">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e6b8a-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6b8a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6b8a-115">Requirements</span></span>



| <span data-ttu-id="e6b8a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6b8a-116">Requirement</span></span> | <span data-ttu-id="e6b8a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e6b8a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6b8a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6b8a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e6b8a-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6b8a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6b8a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6b8a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e6b8a-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6b8a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6b8a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6b8a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6b8a-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6b8a-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6b8a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6b8a-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6b8a-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e6b8a-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e6b8a-126">**RB \_ BEGINDRAG**</span><span class="sxs-lookup"><span data-stu-id="e6b8a-126">**RB\_BEGINDRAG**</span></span>](rb-begindrag.md)
</dt> <dt>

[<span data-ttu-id="e6b8a-127">**RB \_ DRAGMOVE**</span><span class="sxs-lookup"><span data-stu-id="e6b8a-127">**RB\_DRAGMOVE**</span></span>](rb-dragmove.md)
</dt> </dl>

 

 





