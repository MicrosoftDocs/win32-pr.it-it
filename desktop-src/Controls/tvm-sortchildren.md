---
title: Messaggio TVM_SORTCHILDREN (COMmctrl. h)
description: Ordina gli elementi figlio dell'elemento padre specificato in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SortChildren di TreeView.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- Controlli di Windows Message TVM_SORTCHILDREN
topic_type:
- apiref
api_name:
- TVM_SORTCHILDREN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341591c31accb4aab0b49f611359a93ec99c0cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048697"
---
# <a name="tvm_sortchildren-message"></a><span data-ttu-id="bb267-105">\_Messaggio SORTCHILDREN TVM</span><span class="sxs-lookup"><span data-stu-id="bb267-105">TVM\_SORTCHILDREN message</span></span>

<span data-ttu-id="bb267-106">Ordina gli elementi figlio dell'elemento padre specificato in un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="bb267-106">Sorts the child items of the specified parent item in a tree-view control.</span></span> <span data-ttu-id="bb267-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SortChildren di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) .</span><span class="sxs-lookup"><span data-stu-id="bb267-107">You can send this message explicitly or by using the [**TreeView\_SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb267-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb267-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb267-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb267-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb267-110">Valore che specifica se l'ordinamento è ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="bb267-110">Value that specifies whether the sorting is recursive.</span></span> <span data-ttu-id="bb267-111">Impostare *wParam* su **true** per ordinare tutti i livelli degli elementi figlio sotto l'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="bb267-111">Set *wParam* to **TRUE** to sort all levels of child items below the parent item.</span></span> <span data-ttu-id="bb267-112">In caso contrario, vengono ordinati solo gli elementi figlio immediati dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="bb267-112">Otherwise, only the parent's immediate children are sorted.</span></span>

</dd> <dt>

<span data-ttu-id="bb267-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb267-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb267-114">Handle per l'elemento padre i cui elementi figlio devono essere ordinati.</span><span class="sxs-lookup"><span data-stu-id="bb267-114">Handle to the parent item whose child items are to be sorted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb267-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb267-115">Return value</span></span>

<span data-ttu-id="bb267-116">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bb267-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb267-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb267-117">Remarks</span></span>

<span data-ttu-id="bb267-118">Questo messaggio dispone gli elementi della struttura ad albero utilizzando [**due**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) sul nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="bb267-118">This message alphabetizes the tree items using [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) on the item name.</span></span> <span data-ttu-id="bb267-119">È possibile usare il messaggio [**TVM \_ SORTCHILDRENCB**](tvm-sortchildrencb.md) per personalizzare il comportamento di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="bb267-119">You can use the [**TVM\_SORTCHILDRENCB**](tvm-sortchildrencb.md) message to customize the ordering behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb267-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb267-120">Requirements</span></span>



| <span data-ttu-id="bb267-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb267-121">Requirement</span></span> | <span data-ttu-id="bb267-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bb267-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb267-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb267-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bb267-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb267-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb267-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb267-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bb267-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb267-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb267-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb267-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb267-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb267-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

