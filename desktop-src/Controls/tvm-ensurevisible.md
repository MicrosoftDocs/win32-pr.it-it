---
title: Messaggio TVM_ENSUREVISIBLE (COMmctrl. h)
description: Garantisce che un elemento della visualizzazione struttura ad albero sia visibile, espandendo l'elemento padre o scorrendo il controllo di visualizzazione albero, se necessario. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro EnsureVisible di TreeView.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- Controlli di Windows Message TVM_ENSUREVISIBLE
topic_type:
- apiref
api_name:
- TVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06100ee33106736076608aa216d2aebc03b76ebe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964033"
---
# <a name="tvm_ensurevisible-message"></a><span data-ttu-id="607bc-105">\_Messaggio ENSUREVISIBLE TVM</span><span class="sxs-lookup"><span data-stu-id="607bc-105">TVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="607bc-106">Garantisce che un elemento della visualizzazione struttura ad albero sia visibile, espandendo l'elemento padre o scorrendo il controllo di visualizzazione albero, se necessario.</span><span class="sxs-lookup"><span data-stu-id="607bc-106">Ensures that a tree-view item is visible, expanding the parent item or scrolling the tree-view control, if necessary.</span></span> <span data-ttu-id="607bc-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ EnsureVisible di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) .</span><span class="sxs-lookup"><span data-stu-id="607bc-107">You can send this message explicitly or by using the [**TreeView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="607bc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="607bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="607bc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="607bc-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="607bc-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="607bc-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="607bc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="607bc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="607bc-112">Handle per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="607bc-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="607bc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="607bc-113">Return value</span></span>

<span data-ttu-id="607bc-114">Restituisce un valore diverso da zero se il sistema ha eseguito lo scorrimento degli elementi nel controllo di visualizzazione albero e nessun elemento è stato espanso.</span><span class="sxs-lookup"><span data-stu-id="607bc-114">Returns nonzero if the system scrolled the items in the tree-view control and no items were expanded.</span></span> <span data-ttu-id="607bc-115">In caso contrario, il messaggio restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="607bc-115">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="607bc-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="607bc-116">Remarks</span></span>

<span data-ttu-id="607bc-117">Se il \_ messaggio TVM ENSUREVISIBLE espande l'elemento padre, la finestra padre riceve i codici di notifica [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) e [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .</span><span class="sxs-lookup"><span data-stu-id="607bc-117">If the TVM\_ENSUREVISIBLE message expands the parent item, the parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="607bc-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="607bc-118">Requirements</span></span>



| <span data-ttu-id="607bc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="607bc-119">Requirement</span></span> | <span data-ttu-id="607bc-120">Valore</span><span class="sxs-lookup"><span data-stu-id="607bc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="607bc-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="607bc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="607bc-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="607bc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="607bc-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="607bc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="607bc-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="607bc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="607bc-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="607bc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="607bc-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="607bc-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





