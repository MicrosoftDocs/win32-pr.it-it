---
title: Messaggio TVM_SELECTITEM (COMmctrl. h)
description: Seleziona l'elemento della visualizzazione struttura ad albero specificato, scorre l'elemento nella visualizzazione o ridisegna l'elemento nello stile usato per indicare la destinazione di un'operazione di trascinamento della selezione.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- Controlli di Windows Message TVM_SELECTITEM
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873473"
---
# <a name="tvm_selectitem-message"></a><span data-ttu-id="9a037-104">\_Messaggio SELECTITEM TVM</span><span class="sxs-lookup"><span data-stu-id="9a037-104">TVM\_SELECTITEM message</span></span>

<span data-ttu-id="9a037-105">Seleziona l'elemento della visualizzazione struttura ad albero specificato, scorre l'elemento nella visualizzazione o ridisegna l'elemento nello stile usato per indicare la destinazione di un'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="9a037-105">Selects the specified tree-view item, scrolls the item into view, or redraws the item in the style used to indicate the target of a drag-and-drop operation.</span></span> <span data-ttu-id="9a037-106">È possibile inviare questo messaggio in modo esplicito o usando la macro TreeView [**\_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)o [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="9a037-106">You can send this message explicitly or by using the [**TreeView\_Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem), or [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a037-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a037-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a037-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a037-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a037-109">Flag di azione.</span><span class="sxs-lookup"><span data-stu-id="9a037-109">Action flag.</span></span> <span data-ttu-id="9a037-110">Questo parametro può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="9a037-110">This parameter can be one of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9a037-111">Valore</span><span class="sxs-lookup"><span data-stu-id="9a037-111">Value</span></span></th>
<th><span data-ttu-id="9a037-112">Significato</span><span class="sxs-lookup"><span data-stu-id="9a037-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <span data-ttu-id="9a037-113"><dt><strong>TVGN_CARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9a037-113"><dt><strong>TVGN_CARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9a037-114">Imposta la selezione sull'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="9a037-114">Sets the selection to the specified item.</span></span> <span data-ttu-id="9a037-115">La finestra padre del controllo visualizzazione struttura ad albero riceve i codici di notifica <a href="tvn-selchanging.md">TVN_SELCHANGING</a> e <a href="tvn-selchanged.md">TVN_SELCHANGED</a> .</span><span class="sxs-lookup"><span data-stu-id="9a037-115">The tree-view control's parent window receives the <a href="tvn-selchanging.md">TVN_SELCHANGING</a> and <a href="tvn-selchanged.md">TVN_SELCHANGED</a> notification codes.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <span data-ttu-id="9a037-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9a037-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9a037-117">Ridisegna l'elemento specificato nello stile usato per indicare la destinazione di un'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="9a037-117">Redraws the specified item in the style used to indicate the target of a drag-and-drop operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <span data-ttu-id="9a037-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9a037-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9a037-119">Assicura che l'elemento specificato sia visibile e, se possibile, lo Visualizza nella parte superiore della finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="9a037-119">Ensures that the specified item is visible, and, if possible, displays it at the top of the control's window.</span></span> <span data-ttu-id="9a037-120">I controlli di visualizzazione albero visualizzano tutti gli elementi che rientrano nella finestra.</span><span class="sxs-lookup"><span data-stu-id="9a037-120">Tree-view controls display as many items as will fit in the window.</span></span> <span data-ttu-id="9a037-121">Se l'elemento specificato si trova nella parte inferiore della gerarchia di elementi del controllo, potrebbe non diventare il primo elemento visibile, a seconda del numero di elementi che rientrano nella finestra.</span><span class="sxs-lookup"><span data-stu-id="9a037-121">If the specified item is near the bottom of the control's hierarchy of items, it might not become the first visible item, depending on how many items fit in the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <span data-ttu-id="9a037-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9a037-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="9a037-123">Quando viene selezionato un singolo elemento, verifica che TreeView non espanda gli elementi figlio di tale elemento.</span><span class="sxs-lookup"><span data-stu-id="9a037-123">When a single item is selected, ensures that the treeview does not expand the children of that item.</span></span> <span data-ttu-id="9a037-124">Questo valore è valido solo se utilizzato con il flag TVGN_CARET.</span><span class="sxs-lookup"><span data-stu-id="9a037-124">This is valid only if used with the TVGN_CARET flag.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9a037-125">Per usare questo flag, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="9a037-125">To use this flag, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="9a037-126">Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.</span><span class="sxs-lookup"><span data-stu-id="9a037-126">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="9a037-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a037-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a037-128">Handle per un elemento.</span><span class="sxs-lookup"><span data-stu-id="9a037-128">Handle to an item.</span></span> <span data-ttu-id="9a037-129">Se *lParam* è **null**, il controllo è impostato su non è selezionato alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="9a037-129">If *lParam* is **NULL**, the control is set to have no selected item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a037-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a037-130">Return value</span></span>

<span data-ttu-id="9a037-131">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9a037-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a037-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a037-132">Remarks</span></span>

<span data-ttu-id="9a037-133">Se l'elemento specificato è figlio di un elemento padre compresso, l'elenco di elementi figlio dell'elemento padre viene espanso per rivelare l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="9a037-133">If the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item.</span></span> <span data-ttu-id="9a037-134">In questo caso, la finestra padre del controllo riceve i codici di notifica di [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) e [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .</span><span class="sxs-lookup"><span data-stu-id="9a037-134">In this case, the control's parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

<span data-ttu-id="9a037-135">L'uso della macro [**\_ SelectItem di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) equivale a inviare il messaggio di **\_ SelectItem TVM** con *wParam* impostato sul valore di punto di \_ inserimento TVGN.</span><span class="sxs-lookup"><span data-stu-id="9a037-135">Using the [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_CARET value.</span></span> <span data-ttu-id="9a037-136">L'uso della macro [**\_ SelectDropTarget di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) equivale a inviare il messaggio di **\_ SELECTITEM TVM** con *wParam* impostato sul \_ valore DROPHILITE di TVGN.</span><span class="sxs-lookup"><span data-stu-id="9a037-136">Using the [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_DROPHILITE value.</span></span> <span data-ttu-id="9a037-137">L'uso di [**TreeView \_ SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) equivale all'invio del messaggio **\_ SELECTITEM TVM** con *wParam* impostato sul \_ valore FIRSTVISIBLE di TVGN.</span><span class="sxs-lookup"><span data-stu-id="9a037-137">Using [**TreeView\_SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_FIRSTVISIBLE value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a037-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a037-138">Requirements</span></span>



| <span data-ttu-id="9a037-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a037-139">Requirement</span></span> | <span data-ttu-id="9a037-140">Valore</span><span class="sxs-lookup"><span data-stu-id="9a037-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a037-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a037-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9a037-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a037-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a037-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a037-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9a037-144">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9a037-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a037-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a037-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a037-146"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a037-146"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





