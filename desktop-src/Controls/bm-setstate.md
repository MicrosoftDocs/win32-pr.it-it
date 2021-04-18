---
title: Messaggio BM_SETSTATE (winuser. h)
description: Imposta lo stato di evidenziazione di un pulsante. Lo stato di evidenziazione indica se il pulsante è evidenziato come se l'utente avesse eseguito il push. È possibile inviare questo messaggio in modo esplicito o usare la macro di stato del pulsante \_ .
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- Controlli di Windows Message BM_SETSTATE
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9b60231980f406b0aeb499d724dc6aa7025513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301276"
---
# <a name="bm_setstate-message"></a><span data-ttu-id="ecdb4-106">\_Messaggio di SESTATO BM</span><span class="sxs-lookup"><span data-stu-id="ecdb4-106">BM\_SETSTATE message</span></span>

<span data-ttu-id="ecdb4-107">Imposta lo stato di evidenziazione di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="ecdb4-107">Sets the highlight state of a button.</span></span> <span data-ttu-id="ecdb4-108">Lo stato di evidenziazione indica se il pulsante è evidenziato come se l'utente avesse eseguito il push.</span><span class="sxs-lookup"><span data-stu-id="ecdb4-108">The highlight state indicates whether the button is highlighted as if the user had pushed it.</span></span> <span data-ttu-id="ecdb4-109">È possibile inviare questo messaggio in modo esplicito o usare la macro di [**\_ stato del pulsante**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) .</span><span class="sxs-lookup"><span data-stu-id="ecdb4-109">You can send this message explicitly or use the [**Button\_SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ecdb4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecdb4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecdb4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecdb4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecdb4-112">Valore **booleano** che specifica se il pulsante è evidenziato.</span><span class="sxs-lookup"><span data-stu-id="ecdb4-112">A **BOOL** that specifies whether the button is highlighted.</span></span> <span data-ttu-id="ecdb4-113">Il valore **true** evidenzia il pulsante.</span><span class="sxs-lookup"><span data-stu-id="ecdb4-113">A value of **TRUE** highlights the button.</span></span> <span data-ttu-id="ecdb4-114">Il valore **false** consente di rimuovere tutte le evidenziazioni.</span><span class="sxs-lookup"><span data-stu-id="ecdb4-114">A value of **FALSE** removes any highlighting.</span></span>

</dd> <dt>

<span data-ttu-id="ecdb4-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecdb4-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecdb4-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="ecdb4-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecdb4-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecdb4-117">Return value</span></span>

<span data-ttu-id="ecdb4-118">Questo messaggio restituisce sempre zero.</span><span class="sxs-lookup"><span data-stu-id="ecdb4-118">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecdb4-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecdb4-119">Remarks</span></span>

<span data-ttu-id="ecdb4-120">L'evidenziazione influiscono solo sull'aspetto di un pulsante.</span><span class="sxs-lookup"><span data-stu-id="ecdb4-120">Highlighting affects only the appearance of a button.</span></span> <span data-ttu-id="ecdb4-121">Non ha alcun effetto sullo stato di selezione di un pulsante di opzione o di una casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="ecdb4-121">It has no effect on the check state of a radio button or check box.</span></span>

<span data-ttu-id="ecdb4-122">Un pulsante viene evidenziato automaticamente quando l'utente posiziona il cursore su di esso e preme e tiene premuto il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="ecdb4-122">A button is automatically highlighted when the user positions the cursor over it and presses and holds the left mouse button.</span></span> <span data-ttu-id="ecdb4-123">L'evidenziazione viene rimossa quando l'utente rilascia il pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="ecdb4-123">The highlighting is removed when the user releases the mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecdb4-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecdb4-124">Requirements</span></span>



| <span data-ttu-id="ecdb4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecdb4-125">Requirement</span></span> | <span data-ttu-id="ecdb4-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ecdb4-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecdb4-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecdb4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ecdb4-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ecdb4-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ecdb4-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecdb4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ecdb4-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ecdb4-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ecdb4-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecdb4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecdb4-132"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecdb4-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecdb4-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecdb4-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="ecdb4-134">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ecdb4-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ecdb4-135">**BM \_ GETstate**</span><span class="sxs-lookup"><span data-stu-id="ecdb4-135">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="ecdb4-136">**\_controllo BM**</span><span class="sxs-lookup"><span data-stu-id="ecdb4-136">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 





