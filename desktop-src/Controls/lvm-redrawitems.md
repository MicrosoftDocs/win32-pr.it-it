---
title: Messaggio LVM_REDRAWITEMS (COMmctrl. h)
description: Impone a un controllo di visualizzazione elenco di ricreare un intervallo di elementi. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro RedrawItems di ListView.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- Controlli di Windows Message LVM_REDRAWITEMS
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048345"
---
# <a name="lvm_redrawitems-message"></a><span data-ttu-id="e4637-105">\_Messaggio REDRAWITEMS LVM</span><span class="sxs-lookup"><span data-stu-id="e4637-105">LVM\_REDRAWITEMS message</span></span>

<span data-ttu-id="e4637-106">Impone a un controllo di visualizzazione elenco di ricreare un intervallo di elementi.</span><span class="sxs-lookup"><span data-stu-id="e4637-106">Forces a list-view control to redraw a range of items.</span></span> <span data-ttu-id="e4637-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ RedrawItems di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) .</span><span class="sxs-lookup"><span data-stu-id="e4637-107">You can send this message explicitly or by using the [**ListView\_RedrawItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4637-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4637-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4637-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4637-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4637-110">Indice del primo elemento da ricreare.</span><span class="sxs-lookup"><span data-stu-id="e4637-110">Index of the first item to redraw.</span></span>

</dd> <dt>

<span data-ttu-id="e4637-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4637-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4637-112">Indice dell'ultimo elemento da ricreare.</span><span class="sxs-lookup"><span data-stu-id="e4637-112">Index of the last item to redraw.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4637-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4637-113">Return value</span></span>

<span data-ttu-id="e4637-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e4637-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4637-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4637-115">Remarks</span></span>

<span data-ttu-id="e4637-116">Gli elementi specificati non vengono effettivamente ridisegnati fino a quando la finestra elenco-visualizzazione non riceve un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) da ridisegnare.</span><span class="sxs-lookup"><span data-stu-id="e4637-116">The specified items are not actually redrawn until the list-view window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message to repaint.</span></span> <span data-ttu-id="e4637-117">Per ridisegnare immediatamente, chiamare la funzione [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) dopo l'uso di questa macro.</span><span class="sxs-lookup"><span data-stu-id="e4637-117">To repaint immediately, call the [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) function after using this macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4637-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4637-118">Requirements</span></span>



| <span data-ttu-id="e4637-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4637-119">Requirement</span></span> | <span data-ttu-id="e4637-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e4637-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4637-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4637-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e4637-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4637-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4637-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4637-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e4637-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4637-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4637-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4637-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4637-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4637-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

