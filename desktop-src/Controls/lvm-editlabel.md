---
title: Messaggio LVM_EDITLABEL (COMmctrl. h)
description: Inizia la modifica sul posto del testo specificato dell'elemento della visualizzazione elenco. Il messaggio seleziona e concentra in modo implicito l'elemento specificato. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro EditLabel di ListView.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- Controlli di Windows Message LVM_EDITLABEL
topic_type:
- apiref
api_name:
- LVM_EDITLABEL
- LVM_EDITLABELA
- LVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25cb4e119731c41130e1c19fdea2f74882796435
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739967"
---
# <a name="lvm_editlabel-message"></a><span data-ttu-id="4d16d-106">\_Messaggio EDITLABEL LVM</span><span class="sxs-lookup"><span data-stu-id="4d16d-106">LVM\_EDITLABEL message</span></span>

<span data-ttu-id="4d16d-107">Inizia la modifica sul posto del testo specificato dell'elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="4d16d-107">Begins in-place editing of the specified list-view item's text.</span></span> <span data-ttu-id="4d16d-108">Il messaggio seleziona e concentra in modo implicito l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="4d16d-108">The message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="4d16d-109">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ EditLabel di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) .</span><span class="sxs-lookup"><span data-stu-id="4d16d-109">You can send this message explicitly or by using the [**ListView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4d16d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d16d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d16d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d16d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d16d-112">Indice dell'elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="4d16d-112">The index of the list-view item.</span></span> <span data-ttu-id="4d16d-113">Per annullare la modifica, impostare l'indice su-1.</span><span class="sxs-lookup"><span data-stu-id="4d16d-113">To cancel editing, set the index to -1.</span></span>

</dd> <dt>

<span data-ttu-id="4d16d-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d16d-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4d16d-115">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4d16d-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d16d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d16d-116">Return value</span></span>

<span data-ttu-id="4d16d-117">Restituisce l'handle per il controllo di modifica utilizzato per modificare il testo dell'elemento in caso di esito positivo; in caso contrario, **null** .</span><span class="sxs-lookup"><span data-stu-id="4d16d-117">Returns the handle to the edit control that is used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d16d-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d16d-118">Remarks</span></span>

<span data-ttu-id="4d16d-119">Quando l'utente completa o Annulla la modifica, il controllo di modifica viene eliminato definitivamente e l'handle non è più valido.</span><span class="sxs-lookup"><span data-stu-id="4d16d-119">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="4d16d-120">È possibile sottoclassare il controllo di modifica, ma non eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="4d16d-120">You can subclass the edit control, but you should not destroy it.</span></span>

<span data-ttu-id="4d16d-121">Il controllo deve avere lo stato attivo prima di inviare questo messaggio al controllo.</span><span class="sxs-lookup"><span data-stu-id="4d16d-121">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="4d16d-122">È possibile impostare lo stato attivo tramite la funzione [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="4d16d-122">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

<span data-ttu-id="4d16d-123">Se *wParam* è-1, viene inviato un codice di notifica [ \_ ENDLABELEDIT LVN](lvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="4d16d-123">If *wParam* is -1, an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d16d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d16d-124">Requirements</span></span>



| <span data-ttu-id="4d16d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d16d-125">Requirement</span></span> | <span data-ttu-id="4d16d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4d16d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d16d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d16d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4d16d-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d16d-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4d16d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d16d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4d16d-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4d16d-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d16d-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d16d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d16d-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d16d-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4d16d-133">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4d16d-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4d16d-134">**LVM \_ EDITLABELW** (Unicode) e **LVM \_ EDITLABELA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4d16d-134">**LVM\_EDITLABELW** (Unicode) and **LVM\_EDITLABELA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4d16d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d16d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d16d-136">**\_CANCELMODE WM**</span><span class="sxs-lookup"><span data-stu-id="4d16d-136">**WM\_CANCELMODE**</span></span>](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

