---
title: Messaggio TVM_EXPAND (COMmctrl. h)
description: Il \_ messaggio di espansione TVM espande o comprime l'elenco di elementi figlio associati all'elemento padre specificato, se presente. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro di espansione TreeView.
ms.assetid: d6c2e5b2-ce36-4c2b-b527-91c6de56e305
keywords:
- Controlli di Windows Message TVM_EXPAND
topic_type:
- apiref
api_name:
- TVM_EXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d5cd7577c6f4581865569c3aefca93f13aa305
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478485"
---
# <a name="tvm_expand-message"></a><span data-ttu-id="da8c7-105">\_Messaggio espansione TVM</span><span class="sxs-lookup"><span data-stu-id="da8c7-105">TVM\_EXPAND message</span></span>

<span data-ttu-id="da8c7-106">Il messaggio di **\_ espansione TVM** espande o comprime l'elenco di elementi figlio associati all'elemento padre specificato, se presente.</span><span class="sxs-lookup"><span data-stu-id="da8c7-106">The **TVM\_EXPAND** message expands or collapses the list of child items associated with the specified parent item, if any.</span></span> <span data-ttu-id="da8c7-107">È possibile inviare questo messaggio in modo esplicito o usando la macro di [**\_ espansione TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) .</span><span class="sxs-lookup"><span data-stu-id="da8c7-107">You can send this message explicitly or by using the [**TreeView\_Expand**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="da8c7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="da8c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da8c7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da8c7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da8c7-110">Flag di azione.</span><span class="sxs-lookup"><span data-stu-id="da8c7-110">Action flag.</span></span> <span data-ttu-id="da8c7-111">Il parametro può essere costituito da uno o più dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="da8c7-111">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="da8c7-112">Valore</span><span class="sxs-lookup"><span data-stu-id="da8c7-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="da8c7-113">Significato</span><span class="sxs-lookup"><span data-stu-id="da8c7-113">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <span data-ttu-id="da8c7-114"><dt>**\_compressione TVE**</dt></span><span class="sxs-lookup"><span data-stu-id="da8c7-114"><dt>**TVE\_COLLAPSE**</dt></span></span> </dl>                | <span data-ttu-id="da8c7-115">Comprime l'elenco.</span><span class="sxs-lookup"><span data-stu-id="da8c7-115">Collapses the list.</span></span> <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <span data-ttu-id="da8c7-116"><dt>**\_COLLAPSERESET TVE**</dt></span><span class="sxs-lookup"><span data-stu-id="da8c7-116"><dt>**TVE\_COLLAPSERESET**</dt></span></span> </dl> | <span data-ttu-id="da8c7-117">Comprime l'elenco e rimuove gli elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="da8c7-117">Collapses the list and removes the child items.</span></span> <span data-ttu-id="da8c7-118">Il flag di stato [**\_ EXPANDEDONCE di TVIS**](tree-view-control-item-states.md) viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="da8c7-118">The [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is reset.</span></span> <span data-ttu-id="da8c7-119">Questo flag deve essere usato con il \_ flag di compressione TVE.</span><span class="sxs-lookup"><span data-stu-id="da8c7-119">This flag must be used with the TVE\_COLLAPSE flag.</span></span><br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <span data-ttu-id="da8c7-120"><dt>**\_espansione TVE**</dt></span><span class="sxs-lookup"><span data-stu-id="da8c7-120"><dt>**TVE\_EXPAND**</dt></span></span> </dl>                      | <span data-ttu-id="da8c7-121">Espande l'elenco.</span><span class="sxs-lookup"><span data-stu-id="da8c7-121">Expands the list.</span></span><br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <span data-ttu-id="da8c7-122"><dt>**\_EXPANDPARTIAL TVE**</dt></span><span class="sxs-lookup"><span data-stu-id="da8c7-122"><dt>**TVE\_EXPANDPARTIAL**</dt></span></span> </dl> | <span data-ttu-id="da8c7-123">[Versione 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="da8c7-123">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="da8c7-124">Espande parzialmente l'elenco.</span><span class="sxs-lookup"><span data-stu-id="da8c7-124">Partially expands the list.</span></span> <span data-ttu-id="da8c7-125">In questo stato gli elementi figlio sono visibili e il segno più (+) dell'elemento padre, che indica che è possibile espanderlo, viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="da8c7-125">In this state the child items are visible and the parent item's plus sign (+), indicating that it can be expanded, is displayed.</span></span> <span data-ttu-id="da8c7-126">Questo flag deve essere usato in combinazione con il \_ flag di espansione TVE.</span><span class="sxs-lookup"><span data-stu-id="da8c7-126">This flag must be used in combination with the TVE\_EXPAND flag.</span></span><br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <span data-ttu-id="da8c7-127"><dt>**\_interruttore TVE**</dt></span><span class="sxs-lookup"><span data-stu-id="da8c7-127"><dt>**TVE\_TOGGLE**</dt></span></span> </dl>                      | <span data-ttu-id="da8c7-128">Comprime l'elenco se è espanso o lo espande se è compresso.</span><span class="sxs-lookup"><span data-stu-id="da8c7-128">Collapses the list if it is expanded or expands it if it is collapsed.</span></span><br/>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="da8c7-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da8c7-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da8c7-130">Handle per l'elemento padre da espandere o comprimere.</span><span class="sxs-lookup"><span data-stu-id="da8c7-130">Handle to the parent item to expand or collapse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da8c7-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da8c7-131">Return value</span></span>

<span data-ttu-id="da8c7-132">Restituisce un valore diverso da zero se l'operazione ha avuto esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="da8c7-132">Returns nonzero if the operation was successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="da8c7-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="da8c7-133">Remarks</span></span>

<span data-ttu-id="da8c7-134">L'espansione di un nodo già espanso è considerata un'operazione riuscita e [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="da8c7-134">Expanding a node that is already expanded is considered a successful operation and [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns a nonzero value.</span></span> <span data-ttu-id="da8c7-135">Se il nodo è già compresso, il collasso di un nodo restituisce zero. in caso contrario, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="da8c7-135">Collapsing a node returns zero if the node is already collapsed; otherwise it returns nonzero.</span></span> <span data-ttu-id="da8c7-136">Il tentativo di espandere o comprimere un nodo privo di elementi figlio viene considerato un errore e **SendMessage** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="da8c7-136">Attempting to expand or collapse a node that has no children is considered a failure and **SendMessage** returns zero.</span></span>

<span data-ttu-id="da8c7-137">Quando un elemento viene espanso per la prima volta da un messaggio di **\_ espansione TVM** , l'azione genera i codici di notifica [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) e [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) e viene impostato il flag di stato [**TVIS \_ EXPANDEDONCE**](tree-view-control-item-states.md) dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="da8c7-137">When an item is first expanded by a **TVM\_EXPAND** message, the action generates [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes and the item's [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is set.</span></span> <span data-ttu-id="da8c7-138">Fino a quando questo flag di stato rimane impostato, i messaggi di **\_ espansione TVM** successivi non generano le \_ notifiche TVN ITEMEXPANDING o TVN \_ ITEMEXPANDED.</span><span class="sxs-lookup"><span data-stu-id="da8c7-138">As long as this state flag remains set, subsequent **TVM\_EXPAND** messages do not generate TVN\_ITEMEXPANDING or TVN\_ITEMEXPANDED notifications.</span></span> <span data-ttu-id="da8c7-139">Per reimpostare il flag di stato **TVIS \_ EXPANDEDONCE** , è necessario inviare un messaggio di **\_ espansione TVM** con i \_ flag TVE Collapse e TVE \_ COLLAPSERESET impostati.</span><span class="sxs-lookup"><span data-stu-id="da8c7-139">To reset the **TVIS\_EXPANDEDONCE** state flag, you must send a **TVM\_EXPAND** message with the TVE\_COLLAPSE and TVE\_COLLAPSERESET flags set.</span></span> <span data-ttu-id="da8c7-140">Il tentativo di impostare in modo esplicito **TVIS \_ EXPANDEDONCE** comporterà un comportamento imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="da8c7-140">Attempting to explicitly set **TVIS\_EXPANDEDONCE** will result in unpredictable behavior.</span></span>

<span data-ttu-id="da8c7-141">L'operazione di espansione potrebbe non riuscire se il proprietario del controllo TreeView nega l'operazione in risposta a una notifica [ \_ ITEMEXPANDING di TVN](tvn-itemexpanding.md) .</span><span class="sxs-lookup"><span data-stu-id="da8c7-141">The expand operation may fail if the owner of the treeview control denies the operation in response to a [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="da8c7-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da8c7-142">Requirements</span></span>



| <span data-ttu-id="da8c7-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="da8c7-143">Requirement</span></span> | <span data-ttu-id="da8c7-144">Valore</span><span class="sxs-lookup"><span data-stu-id="da8c7-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da8c7-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da8c7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="da8c7-146">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="da8c7-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da8c7-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da8c7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="da8c7-148">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="da8c7-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da8c7-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da8c7-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="da8c7-150"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="da8c7-150"><dt>Commctrl.h</dt></span></span> </dl> |



 

