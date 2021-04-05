---
title: Messaggio TVM_GETEXTENDEDSTYLE (COMmctrl. h)
description: Recupera lo stile esteso per un controllo di visualizzazione albero. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetExtendedStyle di TreeView.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- Controlli di Windows Message TVM_GETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a00e125389ff56c7ff93370ab71945598dba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874481"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a><span data-ttu-id="fdfd3-105">Messaggio TVM_GETEXTENDEDSTYLE (COMmctrl. h)</span><span class="sxs-lookup"><span data-stu-id="fdfd3-105">TVM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="fdfd3-106">Recupera lo stile esteso per un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="fdfd3-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="fdfd3-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetExtendedStyle di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="fdfd3-107">Send this message explicitly or by using the [**TreeView\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fdfd3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fdfd3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdfd3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fdfd3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fdfd3-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="fdfd3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fdfd3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fdfd3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fdfd3-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="fdfd3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdfd3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fdfd3-113">Return value</span></span>

<span data-ttu-id="fdfd3-114">Restituisce il valore dello stile esteso. Per altre informazioni sugli stili, vedere [stili estesi del controllo di visualizzazione albero](tree-view-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="fdfd3-114">Returns the value of extended style.For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fdfd3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fdfd3-115">Remarks</span></span>

<span data-ttu-id="fdfd3-116">Gli stili estesi per un controllo di visualizzazione albero non hanno nulla a che fare con gli stili estesi usati con la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)funzione.</span><span class="sxs-lookup"><span data-stu-id="fdfd3-116">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdfd3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdfd3-117">Requirements</span></span>



| <span data-ttu-id="fdfd3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdfd3-118">Requirement</span></span> | <span data-ttu-id="fdfd3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fdfd3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdfd3-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdfd3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fdfd3-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fdfd3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fdfd3-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdfd3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fdfd3-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fdfd3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fdfd3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fdfd3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdfd3-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdfd3-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

