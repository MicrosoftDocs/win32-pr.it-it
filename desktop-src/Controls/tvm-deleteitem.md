---
title: Messaggio TVM_DELETEITEM (COMmctrl. h)
description: Rimuove un elemento e tutti i relativi elementi figlio da un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro DeleteItem di TreeView.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- Controlli di Windows Message TVM_DELETEITEM
topic_type:
- apiref
api_name:
- TVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8783fd5acdf7319699cdc67cbb3ea075e4dbbc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476954"
---
# <a name="tvm_deleteitem-message"></a><span data-ttu-id="dc39b-105">\_Messaggio DeleteItem TVM</span><span class="sxs-lookup"><span data-stu-id="dc39b-105">TVM\_DELETEITEM message</span></span>

<span data-ttu-id="dc39b-106">Rimuove un elemento e tutti i relativi elementi figlio da un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="dc39b-106">Removes an item and all its children from a tree-view control.</span></span> <span data-ttu-id="dc39b-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ DeleteItem di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="dc39b-107">You can send this message explicitly or by using the [**TreeView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc39b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc39b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc39b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc39b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dc39b-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="dc39b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dc39b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc39b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc39b-112">Handle **HTREEITEM** per l'elemento da eliminare.</span><span class="sxs-lookup"><span data-stu-id="dc39b-112">**HTREEITEM** handle to the item to delete.</span></span> <span data-ttu-id="dc39b-113">Se *lParam* è impostato sulla \_ radice TVI o su **null**, tutti gli elementi vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="dc39b-113">If *lParam* is set to TVI\_ROOT or to **NULL**, all items are deleted.</span></span> <span data-ttu-id="dc39b-114">È anche possibile usare la [**macro \_ DeleteAllItems di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) per eliminare tutti gli elementi.</span><span class="sxs-lookup"><span data-stu-id="dc39b-114">You can also use the [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) macro to delete all items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc39b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc39b-115">Return value</span></span>

<span data-ttu-id="dc39b-116">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dc39b-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc39b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc39b-117">Remarks</span></span>

<span data-ttu-id="dc39b-118">Non è sicuro eliminare gli elementi in risposta a una notifica, ad esempio [TVN \_ SELCHANGING](tvn-selchanging.md).</span><span class="sxs-lookup"><span data-stu-id="dc39b-118">It is not safe to delete items in response to a notification such as [TVN\_SELCHANGING](tvn-selchanging.md).</span></span>

<span data-ttu-id="dc39b-119">Dopo che un elemento è stato eliminato, il relativo handle non è valido e non può essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="dc39b-119">Once an item is deleted, its handle is invalid and cannot be used.</span></span>

<span data-ttu-id="dc39b-120">La finestra padre riceve un codice di notifica [ \_ DeleteItem di TVN](tvn-deleteitem.md) quando ogni elemento viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="dc39b-120">The parent window receives a [TVN\_DELETEITEM](tvn-deleteitem.md) notification code when each item is removed.</span></span>

<span data-ttu-id="dc39b-121">Se l'etichetta dell'elemento viene modificata, l'operazione di modifica viene annullata e la finestra padre riceve il codice di notifica [ \_ ENDLABELEDIT di TVN](tvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="dc39b-121">If the item label is being edited, the edit operation is canceled and the parent window receives the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

<span data-ttu-id="dc39b-122">Se si eliminano tutti gli elementi di un controllo di visualizzazione albero con lo stile [**\_ NoScroll TV**](tree-view-control-window-styles.md) , gli elementi aggiunti successivamente potrebbero non essere visualizzati correttamente.</span><span class="sxs-lookup"><span data-stu-id="dc39b-122">If you delete all items in a tree-view control that has the [**TVS\_NOSCROLL**](tree-view-control-window-styles.md) style, items subsequently added may not display properly.</span></span> <span data-ttu-id="dc39b-123">Per ulteriori informazioni, vedere [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).</span><span class="sxs-lookup"><span data-stu-id="dc39b-123">For more information, see [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc39b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc39b-124">Requirements</span></span>



| <span data-ttu-id="dc39b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc39b-125">Requirement</span></span> | <span data-ttu-id="dc39b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="dc39b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc39b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc39b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dc39b-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc39b-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc39b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc39b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dc39b-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dc39b-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc39b-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc39b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc39b-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc39b-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





