---
title: Messaggio EM_SETSEL (winuser. h)
description: Seleziona un intervallo di caratteri in un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- Controlli di Windows Message EM_SETSEL
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4981fa179ae4bdd454ab0b0a6d7485185ed31d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476097"
---
# <a name="em_setsel-message"></a><span data-ttu-id="78f61-105">\_Messaggio SETSEL em</span><span class="sxs-lookup"><span data-stu-id="78f61-105">EM\_SETSEL message</span></span>

<span data-ttu-id="78f61-106">Seleziona un intervallo di caratteri in un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="78f61-106">Selects a range of characters in an edit control.</span></span> <span data-ttu-id="78f61-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="78f61-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="78f61-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="78f61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78f61-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78f61-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78f61-110">Posizione iniziale del carattere della selezione.</span><span class="sxs-lookup"><span data-stu-id="78f61-110">The starting character position of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="78f61-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78f61-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78f61-112">Posizione del carattere finale della selezione.</span><span class="sxs-lookup"><span data-stu-id="78f61-112">The ending character position of the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78f61-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78f61-113">Return value</span></span>

<span data-ttu-id="78f61-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="78f61-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78f61-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="78f61-115">Remarks</span></span>

<span data-ttu-id="78f61-116">Il valore iniziale può essere maggiore del valore finale.</span><span class="sxs-lookup"><span data-stu-id="78f61-116">The start value can be greater than the end value.</span></span> <span data-ttu-id="78f61-117">Il minore dei due valori specifica la posizione del carattere del primo carattere nella selezione.</span><span class="sxs-lookup"><span data-stu-id="78f61-117">The lower of the two values specifies the character position of the first character in the selection.</span></span> <span data-ttu-id="78f61-118">Il valore più alto specifica la posizione del primo carattere oltre la selezione.</span><span class="sxs-lookup"><span data-stu-id="78f61-118">The higher value specifies the position of the first character beyond the selection.</span></span>

<span data-ttu-id="78f61-119">Il valore iniziale è il punto di ancoraggio della selezione e il valore finale è l'estremità attiva.</span><span class="sxs-lookup"><span data-stu-id="78f61-119">The start value is the anchor point of the selection, and the end value is the active end.</span></span> <span data-ttu-id="78f61-120">Se l'utente usa il tasto MAIUSC per modificare le dimensioni della selezione, l'estremità attiva può essere spostata, ma il punto di ancoraggio rimane lo stesso.</span><span class="sxs-lookup"><span data-stu-id="78f61-120">If the user uses the SHIFT key to adjust the size of the selection, the active end can move but the anchor point remains the same.</span></span>

<span data-ttu-id="78f61-121">Se l'inizio è 0 e la fine è-1, viene selezionato tutto il testo nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="78f61-121">If the start is 0 and the end is -1, all the text in the edit control is selected.</span></span> <span data-ttu-id="78f61-122">Se l'inizio è-1, viene deselezionata la selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="78f61-122">If the start is -1, any current selection is deselected.</span></span>

<span data-ttu-id="78f61-123">**Controlli di modifica:** Il controllo Visualizza un cursore lampeggiante nella posizione finale indipendentemente dai valori relativi di inizio e fine.</span><span class="sxs-lookup"><span data-stu-id="78f61-123">**Edit controls:** The control displays a flashing caret at the end position regardless of the relative values of start and end.</span></span>

<span data-ttu-id="78f61-124">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="78f61-124">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="78f61-125">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="78f61-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="78f61-126">Se il controllo di modifica ha lo stile [**es \_ NOHIDESEL**](edit-control-styles.md) , il testo selezionato viene evidenziato indipendentemente dal fatto che il controllo abbia lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="78f61-126">If the edit control has the [**ES\_NOHIDESEL**](edit-control-styles.md) style, the selected text is highlighted regardless of whether the control has focus.</span></span> <span data-ttu-id="78f61-127">Senza lo stile **es \_ NOHIDESEL** , il testo selezionato viene evidenziato solo quando il controllo di modifica ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="78f61-127">Without the **ES\_NOHIDESEL** style, the selected text is highlighted only when the edit control has the focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="78f61-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78f61-128">Requirements</span></span>



| <span data-ttu-id="78f61-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="78f61-129">Requirement</span></span> | <span data-ttu-id="78f61-130">Valore</span><span class="sxs-lookup"><span data-stu-id="78f61-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78f61-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78f61-131">Minimum supported client</span></span><br/> | <span data-ttu-id="78f61-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78f61-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="78f61-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78f61-133">Minimum supported server</span></span><br/> | <span data-ttu-id="78f61-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78f61-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="78f61-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78f61-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="78f61-136"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78f61-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78f61-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78f61-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="78f61-138">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="78f61-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="78f61-139">**\_GETSEL em**</span><span class="sxs-lookup"><span data-stu-id="78f61-139">**EM\_GETSEL**</span></span>](em-getsel.md)
</dt> <dt>

[<span data-ttu-id="78f61-140">**\_REPLACESEL em**</span><span class="sxs-lookup"><span data-stu-id="78f61-140">**EM\_REPLACESEL**</span></span>](em-replacesel.md)
</dt> <dt>

[<span data-ttu-id="78f61-141">**\_SCROLLCARET em**</span><span class="sxs-lookup"><span data-stu-id="78f61-141">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="78f61-142">**\_EXSETSEL em**</span><span class="sxs-lookup"><span data-stu-id="78f61-142">**EM\_EXSETSEL**</span></span>](em-exsetsel.md)
</dt> </dl>

 

 





