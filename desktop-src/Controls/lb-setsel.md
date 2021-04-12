---
title: Messaggio LB_SETSEL (winuser. h)
description: Seleziona un elemento in una casella di riepilogo a selezione multipla e, se necessario, scorre l'elemento nella visualizzazione.
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- Controlli di Windows Message LB_SETSEL
topic_type:
- apiref
api_name:
- LB_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd50f12c4190ba9ecafad11b167c1ac60adf691d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478538"
---
# <a name="lb_setsel-message"></a><span data-ttu-id="cbb83-104">\_Messaggio SETSEL lb</span><span class="sxs-lookup"><span data-stu-id="cbb83-104">LB\_SETSEL message</span></span>

<span data-ttu-id="cbb83-105">Seleziona un elemento in una casella di riepilogo a selezione multipla e, se necessario, scorre l'elemento nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="cbb83-105">Selects an item in a multiple-selection list box and, if necessary, scrolls the item into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="cbb83-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cbb83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbb83-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cbb83-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbb83-108">Specifica come impostare la selezione.</span><span class="sxs-lookup"><span data-stu-id="cbb83-108">Specifies how to set the selection.</span></span> <span data-ttu-id="cbb83-109">Se questo parametro è **true**, l'elemento viene selezionato ed evidenziato; Se è **false**, l'evidenziazione viene rimossa e l'elemento non è più selezionato.</span><span class="sxs-lookup"><span data-stu-id="cbb83-109">If this parameter is **TRUE**, the item is selected and highlighted; if it is **FALSE**, the highlight is removed and the item is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="cbb83-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cbb83-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cbb83-111">Specifica l'indice in base zero dell'elemento da impostare.</span><span class="sxs-lookup"><span data-stu-id="cbb83-111">Specifies the zero-based index of the item to set.</span></span> <span data-ttu-id="cbb83-112">Se questo parametro è-1, la selezione viene aggiunta o rimossa da tutti gli elementi, a seconda del valore di *wParam*, e non si verifica alcuno scorrimento.</span><span class="sxs-lookup"><span data-stu-id="cbb83-112">If this parameter is -1, the selection is added to or removed from all items, depending on the value of *wParam*, and no scrolling occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbb83-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cbb83-113">Return value</span></span>

<span data-ttu-id="cbb83-114">Se si verifica un errore, il valore restituito è LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="cbb83-114">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbb83-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbb83-115">Remarks</span></span>

<span data-ttu-id="cbb83-116">Utilizzare questo messaggio solo con caselle di riepilogo a selezione multipla.</span><span class="sxs-lookup"><span data-stu-id="cbb83-116">Use this message only with multiple-selection list boxes.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbb83-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbb83-117">Requirements</span></span>



| <span data-ttu-id="cbb83-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbb83-118">Requirement</span></span> | <span data-ttu-id="cbb83-119">Valore</span><span class="sxs-lookup"><span data-stu-id="cbb83-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb83-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbb83-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cbb83-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbb83-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cbb83-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbb83-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cbb83-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cbb83-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cbb83-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cbb83-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbb83-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbb83-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbb83-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbb83-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="cbb83-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="cbb83-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cbb83-128">**\_GETSEL lb**</span><span class="sxs-lookup"><span data-stu-id="cbb83-128">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="cbb83-129">**\_SELITEMRANGE lb**</span><span class="sxs-lookup"><span data-stu-id="cbb83-129">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> </dl>

 

 





