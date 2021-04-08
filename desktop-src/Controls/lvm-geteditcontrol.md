---
title: Messaggio LVM_GETEDITCONTROL (COMmctrl. h)
description: Ottiene l'handle per il controllo di modifica utilizzato per modificare il testo di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetEditControl di ListView.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- Controlli di Windows Message LVM_GETEDITCONTROL
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a8790f86fee17f72078f61899edcd79b331759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047861"
---
# <a name="lvm_geteditcontrol-message"></a><span data-ttu-id="b2121-105">\_Messaggio GETEDITCONTROL LVM</span><span class="sxs-lookup"><span data-stu-id="b2121-105">LVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="b2121-106">Ottiene l'handle per il controllo di modifica utilizzato per modificare il testo di un elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="b2121-106">Gets the handle to the edit control being used to edit a list-view item's text.</span></span> <span data-ttu-id="b2121-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetEditControl di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) .</span><span class="sxs-lookup"><span data-stu-id="b2121-107">You can send this message explicitly or by using the [**ListView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2121-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2121-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2121-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2121-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b2121-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b2121-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b2121-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2121-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b2121-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b2121-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2121-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2121-113">Return value</span></span>

<span data-ttu-id="b2121-114">Restituisce l'handle per il controllo di modifica, se ha esito positivo, oppure **null** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b2121-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2121-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2121-115">Remarks</span></span>

<span data-ttu-id="b2121-116">Quando viene avviata la modifica dell'etichetta, viene creato, posizionato e inizializzato un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="b2121-116">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="b2121-117">Prima che venga visualizzato, il controllo elenco-visualizzazione Invia la finestra padre di un codice di notifica [ \_ BEGINLABELEDIT LVN](lvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="b2121-117">Before it is displayed, the list-view control sends its parent window an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="b2121-118">Per personalizzare la modifica delle etichette, implementare un gestore per [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) e inviare un messaggio **LVM \_ GETEDITCONTROL** al controllo List-View.</span><span class="sxs-lookup"><span data-stu-id="b2121-118">To customize label editing, implement a handler for [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) and have it send an **LVM\_GETEDITCONTROL** message to the list-view control.</span></span> <span data-ttu-id="b2121-119">Se è in corso la modifica di un'etichetta, il valore restituito sarà un handle per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="b2121-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="b2121-120">Utilizzare questo handle per personalizzare il controllo di modifica inviando i normali messaggi **em \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="b2121-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="b2121-121">Quando l'utente completa o Annulla la modifica, il controllo di modifica viene eliminato definitivamente e l'handle non è più valido.</span><span class="sxs-lookup"><span data-stu-id="b2121-121">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="b2121-122">È possibile sottoclassare il controllo di modifica, ma non eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="b2121-122">You can subclass the edit control, but you should not destroy it.</span></span> <span data-ttu-id="b2121-123">Per annullare la modifica, inviare il controllo elenco-visualizzazione di un messaggio [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) .</span><span class="sxs-lookup"><span data-stu-id="b2121-123">To cancel editing, send the list-view control a [**WM\_CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) message.</span></span>

<span data-ttu-id="b2121-124">L'elemento della visualizzazione elenco da modificare è l'elemento attualmente attivo, ovvero l'elemento nello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="b2121-124">The list-view item being edited is the currently focused item that is, the item in the focused state.</span></span> <span data-ttu-id="b2121-125">Per trovare un elemento in base al relativo stato, usare il messaggio [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) .</span><span class="sxs-lookup"><span data-stu-id="b2121-125">To find an item based on its state, use the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2121-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2121-126">Requirements</span></span>



| <span data-ttu-id="b2121-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2121-127">Requirement</span></span> | <span data-ttu-id="b2121-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b2121-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2121-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2121-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b2121-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2121-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b2121-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2121-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b2121-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2121-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2121-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2121-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2121-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2121-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2121-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2121-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2121-136">**\_GetEditControl ListView**</span><span class="sxs-lookup"><span data-stu-id="b2121-136">**ListView\_GetEditControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

