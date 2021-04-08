---
title: Messaggio EM_SETMODIFY (winuser. h)
description: Imposta o cancella il flag di modifica per un controllo di modifica. Il flag di modifica indica se il testo all'interno del controllo di modifica è stato modificato. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Controlli di Windows Message EM_SETMODIFY
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591b57dbc5441e96c1c6d3963172864713ed939f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874037"
---
# <a name="em_setmodify-message"></a><span data-ttu-id="507ab-106">Messaggio di modifica di EM \_</span><span class="sxs-lookup"><span data-stu-id="507ab-106">EM\_SETMODIFY message</span></span>

<span data-ttu-id="507ab-107">Imposta o cancella il flag di modifica per un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="507ab-107">Sets or clears the modification flag for an edit control.</span></span> <span data-ttu-id="507ab-108">Il flag di modifica indica se il testo all'interno del controllo di modifica è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="507ab-108">The modification flag indicates whether the text within the edit control has been modified.</span></span> <span data-ttu-id="507ab-109">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="507ab-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="507ab-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="507ab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="507ab-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="507ab-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="507ab-112">Nuovo valore per il flag di modifica.</span><span class="sxs-lookup"><span data-stu-id="507ab-112">The new value for the modification flag.</span></span> <span data-ttu-id="507ab-113">Il valore **true** indica che il testo è stato modificato e il valore **false** indica che non è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="507ab-113">A value of **TRUE** indicates the text has been modified, and a value of **FALSE** indicates it has not been modified.</span></span>

</dd> <dt>

<span data-ttu-id="507ab-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="507ab-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="507ab-115">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="507ab-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="507ab-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="507ab-116">Return value</span></span>

<span data-ttu-id="507ab-117">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="507ab-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="507ab-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="507ab-118">Remarks</span></span>

<span data-ttu-id="507ab-119">Il sistema cancella automaticamente il flag di modifica a zero quando viene creato il controllo.</span><span class="sxs-lookup"><span data-stu-id="507ab-119">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="507ab-120">Se l'utente modifica il testo del controllo, il sistema imposta il flag su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="507ab-120">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="507ab-121">È possibile inviare il messaggio [**em \_ GetModify**](em-getmodify.md) al controllo Edit per recuperare lo stato corrente del flag.</span><span class="sxs-lookup"><span data-stu-id="507ab-121">You can send the [**EM\_GETMODIFY**](em-getmodify.md) message to the edit control to retrieve the current state of the flag.</span></span>

<span data-ttu-id="507ab-122">**Modifica dettagliata 1,0:** Gli oggetti creati senza il flag **reo \_ DYNAMICSIZE** bloccano gli extent quando il flag di modifica è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="507ab-122">**Rich Edit 1.0:** Objects created without the **REO\_DYNAMICSIZE** flag will lock in their extents when the modify flag is set to **FALSE**.</span></span>

<span data-ttu-id="507ab-123">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="507ab-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="507ab-124">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="507ab-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="507ab-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="507ab-125">Requirements</span></span>



| <span data-ttu-id="507ab-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="507ab-126">Requirement</span></span> | <span data-ttu-id="507ab-127">Valore</span><span class="sxs-lookup"><span data-stu-id="507ab-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="507ab-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="507ab-128">Minimum supported client</span></span><br/> | <span data-ttu-id="507ab-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="507ab-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="507ab-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="507ab-130">Minimum supported server</span></span><br/> | <span data-ttu-id="507ab-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="507ab-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="507ab-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="507ab-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="507ab-133"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="507ab-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="507ab-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="507ab-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="507ab-135">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="507ab-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="507ab-136">**GetModify EM \_**</span><span class="sxs-lookup"><span data-stu-id="507ab-136">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> <dt>

[<span data-ttu-id="507ab-137">**REOBJECT**</span><span class="sxs-lookup"><span data-stu-id="507ab-137">**REOBJECT**</span></span>](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





