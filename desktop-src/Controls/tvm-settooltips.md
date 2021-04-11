---
title: Messaggio TVM_SETTOOLTIPS (COMmctrl. h)
description: Imposta il controllo ToolTip figlio di un controllo di visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TreeView Setooltips.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- Controlli di Windows Message TVM_SETTOOLTIPS
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd9d5957a38d873993405a5283545472433e958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119730"
---
# <a name="tvm_settooltips-message"></a><span data-ttu-id="41a1f-105">\_Messaggio di SEtooltips TVM</span><span class="sxs-lookup"><span data-stu-id="41a1f-105">TVM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="41a1f-106">Imposta il controllo ToolTip figlio di un controllo di visualizzazione struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="41a1f-106">Sets a tree-view control's child tooltip control.</span></span> <span data-ttu-id="41a1f-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**TreeView \_ setooltips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="41a1f-107">You can send this message explicitly or by using the [**TreeView\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="41a1f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="41a1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41a1f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41a1f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41a1f-110">Handle per un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="41a1f-110">Handle to a tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="41a1f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41a1f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="41a1f-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="41a1f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41a1f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41a1f-113">Return value</span></span>

<span data-ttu-id="41a1f-114">Restituisce l'handle per il controllo ToolTip impostato in precedenza per il controllo di visualizzazione ad albero oppure **null** se le descrizioni comandi non sono state usate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="41a1f-114">Returns the handle to tooltip control previously set for the tree-view control, or **NULL** if tooltips were not previously used.</span></span>

## <a name="remarks"></a><span data-ttu-id="41a1f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="41a1f-115">Remarks</span></span>

<span data-ttu-id="41a1f-116">Quando vengono creati, i controlli di visualizzazione albero creano automaticamente un controllo ToolTip figlio.</span><span class="sxs-lookup"><span data-stu-id="41a1f-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="41a1f-117">Per impedire a un controllo di visualizzazione albero di usare le descrizioni comandi, creare il controllo con lo stile [**\_ notooltips di TV**](tree-view-control-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="41a1f-117">To prevent a tree-view control from using tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="41a1f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41a1f-118">Requirements</span></span>



| <span data-ttu-id="41a1f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="41a1f-119">Requirement</span></span> | <span data-ttu-id="41a1f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="41a1f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41a1f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41a1f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="41a1f-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41a1f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41a1f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41a1f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="41a1f-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41a1f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41a1f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41a1f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="41a1f-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41a1f-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41a1f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41a1f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41a1f-128">**\_descrizioni comando TVM**</span><span class="sxs-lookup"><span data-stu-id="41a1f-128">**TVM\_GETTOOLTIPS**</span></span>](tvm-gettooltips.md)
</dt> </dl>

 

 





