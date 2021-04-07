---
title: Messaggio TVM_EDITLABEL (COMmctrl. h)
description: Inizia la modifica sul posto del testo dell'elemento specificato, sostituendo il testo dell'elemento con un controllo di modifica a riga singola contenente il testo.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- Controlli di Windows Message TVM_EDITLABEL
topic_type:
- apiref
api_name:
- TVM_EDITLABEL
- TVM_EDITLABELA
- TVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3608c3f959c45571d9bc085518b763cf505180ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964034"
---
# <a name="tvm_editlabel-message"></a><span data-ttu-id="822e3-104">\_Messaggio EDITLABEL TVM</span><span class="sxs-lookup"><span data-stu-id="822e3-104">TVM\_EDITLABEL message</span></span>

<span data-ttu-id="822e3-105">Inizia la modifica sul posto del testo dell'elemento specificato, sostituendo il testo dell'elemento con un controllo di modifica a riga singola contenente il testo.</span><span class="sxs-lookup"><span data-stu-id="822e3-105">Begins in-place editing of the specified item's text, replacing the text of the item with a single-line edit control containing the text.</span></span> <span data-ttu-id="822e3-106">Questo messaggio seleziona e concentra in modo implicito l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="822e3-106">This message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="822e3-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ EditLabel di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) .</span><span class="sxs-lookup"><span data-stu-id="822e3-107">You can send this message explicitly or by using the [**TreeView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="822e3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="822e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="822e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="822e3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="822e3-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="822e3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="822e3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="822e3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="822e3-112">Handle per l'elemento da modificare.</span><span class="sxs-lookup"><span data-stu-id="822e3-112">Handle to the item to edit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="822e3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="822e3-113">Return value</span></span>

<span data-ttu-id="822e3-114">Restituisce l'handle per il controllo di modifica utilizzato per modificare il testo dell'elemento in caso di esito positivo; in caso contrario, **null** .</span><span class="sxs-lookup"><span data-stu-id="822e3-114">Returns the handle to the edit control used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="822e3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="822e3-115">Remarks</span></span>

<span data-ttu-id="822e3-116">Questo messaggio Invia un codice di notifica di [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) all'elemento padre del controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="822e3-116">This message sends a [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code to the parent of the tree-view control.</span></span>

<span data-ttu-id="822e3-117">Quando l'utente completa o Annulla la modifica, il controllo di modifica viene eliminato definitivamente e l'handle non è più valido.</span><span class="sxs-lookup"><span data-stu-id="822e3-117">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="822e3-118">È possibile sottoclassare il controllo di modifica, ma non eliminarlo definitivamente.</span><span class="sxs-lookup"><span data-stu-id="822e3-118">You can subclass the edit control, but do not destroy it.</span></span>

<span data-ttu-id="822e3-119">Il controllo deve avere lo stato attivo prima di inviare questo messaggio al controllo.</span><span class="sxs-lookup"><span data-stu-id="822e3-119">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="822e3-120">È possibile impostare lo stato attivo tramite la funzione [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="822e3-120">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="822e3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="822e3-121">Requirements</span></span>



| <span data-ttu-id="822e3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="822e3-122">Requirement</span></span> | <span data-ttu-id="822e3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="822e3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="822e3-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="822e3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="822e3-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="822e3-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="822e3-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="822e3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="822e3-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="822e3-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="822e3-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="822e3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="822e3-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="822e3-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="822e3-130">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="822e3-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="822e3-131">**TVM \_ EDITLABELW** (Unicode) e **TVM \_ EDITLABELA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="822e3-131">**TVM\_EDITLABELW** (Unicode) and **TVM\_EDITLABELA** (ANSI)</span></span><br/>               |



 

