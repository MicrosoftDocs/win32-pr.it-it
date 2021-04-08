---
title: Messaggio EM_UNDO (winuser. h)
description: Questo messaggio annulla l'ultima operazione di modifica del controllo nella coda di annullamento del controllo. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- Controlli di Windows Message EM_UNDO
topic_type:
- apiref
api_name:
- EM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c75d79e7ed25e582682830b1323c27878bbdbb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741578"
---
# <a name="em_undo-message"></a><span data-ttu-id="83588-105">\_Messaggio di annullamento em</span><span class="sxs-lookup"><span data-stu-id="83588-105">EM\_UNDO message</span></span>

<span data-ttu-id="83588-106">Questo messaggio annulla l'ultima operazione di modifica del controllo nella coda di annullamento del controllo.</span><span class="sxs-lookup"><span data-stu-id="83588-106">This message undoes the last edit control operation in the control's undo queue.</span></span> <span data-ttu-id="83588-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="83588-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="83588-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="83588-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83588-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83588-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83588-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="83588-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="83588-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83588-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83588-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="83588-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83588-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83588-113">Return value</span></span>

<span data-ttu-id="83588-114">Per un controllo di modifica a riga singola, il valore restituito è sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="83588-114">For a single-line edit control, the return value is always **TRUE**.</span></span>

<span data-ttu-id="83588-115">Per un controllo di modifica su più righe, il valore restituito è **true** se l'operazione di annullamento ha esito positivo o **false** se l'operazione di annullamento ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="83588-115">For a multiline edit control, the return value is **TRUE** if the undo operation is successful, or **FALSE** if the undo operation fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="83588-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="83588-116">Remarks</span></span>

<span data-ttu-id="83588-117">**Modificare i controlli e rich edit 1,0:** Un'operazione di annullamento può anche essere annullata.</span><span class="sxs-lookup"><span data-stu-id="83588-117">**Edit controls and Rich Edit 1.0:** An undo operation can also be undone.</span></span> <span data-ttu-id="83588-118">Ad esempio, è possibile ripristinare il testo eliminato con il primo messaggio di **\_ annullamento em** e rimuovere nuovamente il testo con un secondo messaggio di **\_ annullamento** , purché non sia presente alcuna operazione di modifica.</span><span class="sxs-lookup"><span data-stu-id="83588-118">For example, you can restore deleted text with the first **EM\_UNDO** message, and remove the text again with a second **EM\_UNDO** message as long as there is no intervening edit operation.</span></span>

<span data-ttu-id="83588-119">**Rich Edit 2,0 e versioni successive:** La funzionalità di annullamento è multilivello, quindi l'invio di due messaggi di **\_ annullamento em** Annulla le ultime due operazioni nella coda di annullamento.</span><span class="sxs-lookup"><span data-stu-id="83588-119">**Rich Edit 2.0 and later:** The undo feature is multilevel so sending two **EM\_UNDO** messages will undo the last two operations in the undo queue.</span></span> <span data-ttu-id="83588-120">Per ripetere un'operazione, inviare il messaggio di [**\_ ripetizione em**](em-redo.md) .</span><span class="sxs-lookup"><span data-stu-id="83588-120">To redo an operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

<span data-ttu-id="83588-121">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="83588-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="83588-122">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="83588-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83588-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83588-123">Requirements</span></span>



| <span data-ttu-id="83588-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="83588-124">Requirement</span></span> | <span data-ttu-id="83588-125">Valore</span><span class="sxs-lookup"><span data-stu-id="83588-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83588-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83588-126">Minimum supported client</span></span><br/> | <span data-ttu-id="83588-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83588-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="83588-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83588-128">Minimum supported server</span></span><br/> | <span data-ttu-id="83588-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83588-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="83588-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83588-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="83588-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83588-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83588-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83588-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83588-133">**\_CANUNDO em**</span><span class="sxs-lookup"><span data-stu-id="83588-133">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> </dl>

 

 





