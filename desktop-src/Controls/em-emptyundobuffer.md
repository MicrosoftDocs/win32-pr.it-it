---
title: Messaggio EM_EMPTYUNDOBUFFER (winuser. h)
description: Reimposta il flag di annullamento di un controllo di modifica. Il flag di annullamento viene impostato ogni volta che un'operazione all'interno del controllo di modifica può essere annullata. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- Controlli di Windows Message EM_EMPTYUNDOBUFFER
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abbdc067b603a032b8d311ddd7930a8ca6de01c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477603"
---
# <a name="em_emptyundobuffer-message"></a><span data-ttu-id="b2d68-106">\_Messaggio EMPTYUNDOBUFFER em</span><span class="sxs-lookup"><span data-stu-id="b2d68-106">EM\_EMPTYUNDOBUFFER message</span></span>

<span data-ttu-id="b2d68-107">Reimposta il flag di annullamento di un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="b2d68-107">Resets the undo flag of an edit control.</span></span> <span data-ttu-id="b2d68-108">Il flag di annullamento viene impostato ogni volta che un'operazione all'interno del controllo di modifica può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="b2d68-108">The undo flag is set whenever an operation within the edit control can be undone.</span></span> <span data-ttu-id="b2d68-109">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b2d68-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2d68-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2d68-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2d68-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2d68-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2d68-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b2d68-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b2d68-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2d68-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2d68-114">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b2d68-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2d68-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2d68-115">Return value</span></span>

<span data-ttu-id="b2d68-116">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="b2d68-116">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2d68-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2d68-117">Remarks</span></span>

<span data-ttu-id="b2d68-118">Il flag di annullamento viene reimpostato automaticamente ogni volta che il controllo di modifica riceve un messaggio di selettore [**WM \_**](/windows/desktop/winmsg/wm-settext) o di [**em \_**](em-sethandle.md) .</span><span class="sxs-lookup"><span data-stu-id="b2d68-118">The undo flag is automatically reset whenever the edit control receives a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) or [**EM\_SETHANDLE**](em-sethandle.md) message.</span></span>

<span data-ttu-id="b2d68-119">**Modificare i controlli e rich edit 1,0:** Il controllo può annullare o ripristinare solo l'operazione più recente.</span><span class="sxs-lookup"><span data-stu-id="b2d68-119">**Edit controls and Rich Edit 1.0:** The control can only undo or redo the most recent operation.</span></span>

<span data-ttu-id="b2d68-120">**Rich Edit 2,0 e versioni successive:** Il **messaggio \_ EMPTYUNDOBUFFER em** svuota tutti i buffer di annullamento e ripristino.</span><span class="sxs-lookup"><span data-stu-id="b2d68-120">**Rich Edit 2.0 and later:** The **EM\_EMPTYUNDOBUFFER** message empties all undo and redo buffers.</span></span> <span data-ttu-id="b2d68-121">I controlli Rich Edit consentono all'utente di annullare o ripristinare più operazioni.</span><span class="sxs-lookup"><span data-stu-id="b2d68-121">Rich edit controls enable the user to undo or redo multiple operations.</span></span>

<span data-ttu-id="b2d68-122">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b2d68-122">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="b2d68-123">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="b2d68-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2d68-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2d68-124">Requirements</span></span>



| <span data-ttu-id="b2d68-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2d68-125">Requirement</span></span> | <span data-ttu-id="b2d68-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b2d68-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d68-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2d68-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b2d68-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2d68-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b2d68-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2d68-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b2d68-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2d68-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b2d68-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2d68-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2d68-132"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2d68-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2d68-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2d68-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2d68-134">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b2d68-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b2d68-135">**\_CANUNDO em**</span><span class="sxs-lookup"><span data-stu-id="b2d68-135">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="b2d68-136">**filehandle EM \_**</span><span class="sxs-lookup"><span data-stu-id="b2d68-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

[<span data-ttu-id="b2d68-137">**\_Annulla**</span><span class="sxs-lookup"><span data-stu-id="b2d68-137">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

<span data-ttu-id="b2d68-138">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="b2d68-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b2d68-139">**\_testo WM**</span><span class="sxs-lookup"><span data-stu-id="b2d68-139">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

