---
title: Messaggio TVM_GETTOOLTIPS (COMmctrl. h)
description: Recupera l'handle per il controllo ToolTip figlio utilizzato da un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TreeView GetToolTips.
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- Controlli di Windows Message TVM_GETTOOLTIPS
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475898"
---
# <a name="tvm_gettooltips-message"></a><span data-ttu-id="be0d3-105">\_Messaggio TVM GETtooltips</span><span class="sxs-lookup"><span data-stu-id="be0d3-105">TVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="be0d3-106">Recupera l'handle per il controllo ToolTip figlio utilizzato da un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="be0d3-106">Retrieves the handle to the child tooltip control used by a tree-view control.</span></span> <span data-ttu-id="be0d3-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TreeView \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="be0d3-107">You can send this message explicitly or by using the [**TreeView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="be0d3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="be0d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be0d3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be0d3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="be0d3-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="be0d3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="be0d3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be0d3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="be0d3-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="be0d3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be0d3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be0d3-113">Return value</span></span>

<span data-ttu-id="be0d3-114">Restituisce l'handle per il controllo ToolTip figlio oppure **null** se il controllo non utilizza descrizioni comandi.</span><span class="sxs-lookup"><span data-stu-id="be0d3-114">Returns the handle to the child tooltip control, or **NULL** if the control is not using tooltips.</span></span>

## <a name="remarks"></a><span data-ttu-id="be0d3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="be0d3-115">Remarks</span></span>

<span data-ttu-id="be0d3-116">Quando vengono creati, i controlli di visualizzazione albero creano automaticamente un controllo ToolTip figlio.</span><span class="sxs-lookup"><span data-stu-id="be0d3-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="be0d3-117">Per fare in modo che un controllo di visualizzazione albero non usi descrizioni comandi, creare il controllo con lo stile [**\_ notooltips di TV**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="be0d3-117">To cause a tree-view control not to use tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="be0d3-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be0d3-118">Requirements</span></span>



| <span data-ttu-id="be0d3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="be0d3-119">Requirement</span></span> | <span data-ttu-id="be0d3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="be0d3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be0d3-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be0d3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="be0d3-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be0d3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be0d3-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be0d3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="be0d3-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be0d3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be0d3-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be0d3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="be0d3-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="be0d3-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be0d3-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be0d3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be0d3-128">**\_descrizioni comando TVM**</span><span class="sxs-lookup"><span data-stu-id="be0d3-128">**TVM\_SETTOOLTIPS**</span></span>](tvm-settooltips.md)
</dt> </dl>

 

 





