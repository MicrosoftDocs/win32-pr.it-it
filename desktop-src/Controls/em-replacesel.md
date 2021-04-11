---
title: Messaggio EM_REPLACESEL (winuser. h)
description: Sostituisce il testo selezionato in un controllo di modifica o un controllo Rich Edit con il testo specificato.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- Controlli di Windows Message EM_REPLACESEL
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9745b870a310626a6cbbbddbef118a63c64479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121498"
---
# <a name="em_replacesel-message"></a><span data-ttu-id="ae18f-104">\_Messaggio REPLACESEL em</span><span class="sxs-lookup"><span data-stu-id="ae18f-104">EM\_REPLACESEL message</span></span>

<span data-ttu-id="ae18f-105">Sostituisce il testo selezionato in un controllo di modifica o un controllo Rich Edit con il testo specificato.</span><span class="sxs-lookup"><span data-stu-id="ae18f-105">Replaces the selected text in an edit control or a rich edit control with the specified text.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae18f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae18f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae18f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae18f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae18f-108">Specifica se l'operazione di sostituzione può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="ae18f-108">Specifies whether the replacement operation can be undone.</span></span> <span data-ttu-id="ae18f-109">Se il valore è **true**, l'operazione può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="ae18f-109">If this is **TRUE**, the operation can be undone.</span></span> <span data-ttu-id="ae18f-110">Se è **false** , l'operazione non può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="ae18f-110">If this is **FALSE** , the operation cannot be undone.</span></span>

</dd> <dt>

<span data-ttu-id="ae18f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae18f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae18f-112">Puntatore a una stringa con terminazione null che contiene il testo di sostituzione.</span><span class="sxs-lookup"><span data-stu-id="ae18f-112">A pointer to a null-terminated string containing the replacement text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae18f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae18f-113">Return value</span></span>

<span data-ttu-id="ae18f-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="ae18f-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae18f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae18f-115">Remarks</span></span>

<span data-ttu-id="ae18f-116">Usare il **messaggio \_ REPLACESEL em** per sostituire solo una parte del testo in un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="ae18f-116">Use the **EM\_REPLACESEL** message to replace only a portion of the text in an edit control.</span></span> <span data-ttu-id="ae18f-117">Per sostituire tutto il testo, utilizzare il messaggio [**di \_ testo WM**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="ae18f-117">To replace all of the text, use the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span>

<span data-ttu-id="ae18f-118">Se non è presente alcuna selezione, il testo di sostituzione viene inserito nel punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="ae18f-118">If there is no selection, the replacement text is inserted at the caret.</span></span>

<span data-ttu-id="ae18f-119">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ae18f-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="ae18f-120">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="ae18f-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="ae18f-121">In un controllo Rich Edit il testo di sostituzione acquisisce la formattazione del carattere nel punto di inserimento o, se è presente una selezione, del primo carattere nella selezione.</span><span class="sxs-lookup"><span data-stu-id="ae18f-121">In a rich edit control, the replacement text takes the formatting of the character at the caret or, if there is a selection, of the first character in the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae18f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae18f-122">Requirements</span></span>



| <span data-ttu-id="ae18f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae18f-123">Requirement</span></span> | <span data-ttu-id="ae18f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ae18f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae18f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae18f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ae18f-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae18f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ae18f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae18f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ae18f-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae18f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ae18f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae18f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae18f-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae18f-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae18f-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae18f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae18f-132">**\_testo WM**</span><span class="sxs-lookup"><span data-stu-id="ae18f-132">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

