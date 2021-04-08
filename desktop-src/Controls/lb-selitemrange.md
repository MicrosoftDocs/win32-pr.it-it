---
title: Messaggio LB_SELITEMRANGE (winuser. h)
description: Consente di selezionare o deselezionare uno o più elementi consecutivi in una casella di riepilogo a selezione multipla.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- Controlli di Windows Message LB_SELITEMRANGE
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a137b90a817519cf23c894dc19417dd2d9b6b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048652"
---
# <a name="lb_selitemrange-message"></a><span data-ttu-id="f42a0-104">\_Messaggio SELITEMRANGE lb</span><span class="sxs-lookup"><span data-stu-id="f42a0-104">LB\_SELITEMRANGE message</span></span>

<span data-ttu-id="f42a0-105">Consente di selezionare o deselezionare uno o più elementi consecutivi in una casella di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="f42a0-105">Selects or deselects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="f42a0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f42a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f42a0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f42a0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f42a0-108">**True** per selezionare l'intervallo di elementi oppure **false** per deselezionarlo.</span><span class="sxs-lookup"><span data-stu-id="f42a0-108">**TRUE** to select the range of items, or **FALSE** to deselect it.</span></span>

</dd> <dt>

<span data-ttu-id="f42a0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f42a0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f42a0-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica l'indice in base zero del primo elemento da selezionare.</span><span class="sxs-lookup"><span data-stu-id="f42a0-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the first item to select.</span></span> <span data-ttu-id="f42a0-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica l'indice in base zero dell'ultimo elemento da selezionare.</span><span class="sxs-lookup"><span data-stu-id="f42a0-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f42a0-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f42a0-112">Return value</span></span>

<span data-ttu-id="f42a0-113">Se si verifica un errore, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="f42a0-113">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="f42a0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f42a0-114">Remarks</span></span>

<span data-ttu-id="f42a0-115">Utilizzare questo messaggio solo con caselle di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="f42a0-115">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="f42a0-116">Questo messaggio può selezionare un intervallo solo entro i primi 65.536 elementi.</span><span class="sxs-lookup"><span data-stu-id="f42a0-116">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="f42a0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f42a0-117">Requirements</span></span>



| <span data-ttu-id="f42a0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f42a0-118">Requirement</span></span> | <span data-ttu-id="f42a0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f42a0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f42a0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f42a0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f42a0-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f42a0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f42a0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f42a0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f42a0-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f42a0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f42a0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f42a0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f42a0-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f42a0-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f42a0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f42a0-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f42a0-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f42a0-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f42a0-128">**\_SELITEMRANGEEX lb**</span><span class="sxs-lookup"><span data-stu-id="f42a0-128">**LB\_SELITEMRANGEEX**</span></span>](lb-selitemrangeex.md)
</dt> <dt>

[<span data-ttu-id="f42a0-129">**\_SETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="f42a0-129">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> <dt>

<span data-ttu-id="f42a0-130">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="f42a0-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f42a0-131">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="f42a0-131">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

