---
title: Messaggio TVM_SETHOT (COMmctrl. h)
description: Imposta l'elemento attivo per un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetHot di TreeView.
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- Controlli di Windows Message TVM_SETHOT
topic_type:
- apiref
api_name:
- TVM_SETHOT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beccd5429267350682a6721cde66cca9316cf438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964788"
---
# <a name="tvm_sethot-message"></a><span data-ttu-id="6fe2f-105">\_Messaggio SETHOT TVM</span><span class="sxs-lookup"><span data-stu-id="6fe2f-105">TVM\_SETHOT message</span></span>

<span data-ttu-id="6fe2f-106">\[Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="6fe2f-107">Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6fe2f-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="6fe2f-108">Imposta l'elemento attivo per un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-108">Sets the hot item for a tree-view control.</span></span> <span data-ttu-id="6fe2f-109">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetHot di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) .</span><span class="sxs-lookup"><span data-stu-id="6fe2f-109">You can send this message explicitly or by using the [**TreeView\_SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6fe2f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6fe2f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fe2f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6fe2f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fe2f-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-112">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6fe2f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6fe2f-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fe2f-114">Handle per il nuovo elemento attivo.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-114">Handle to the new hot item.</span></span> <span data-ttu-id="6fe2f-115">Se questo valore è **null**, il controllo di visualizzazione albero verrà impostato in modo da non avere alcun elemento attivo.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-115">If this value is **NULL**, the tree-view control will be set to have no hot item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fe2f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6fe2f-116">Return value</span></span>

<span data-ttu-id="6fe2f-117">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="6fe2f-118">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="6fe2f-118">Security Considerations</span></span>

<span data-ttu-id="6fe2f-119">L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fe2f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fe2f-120">Remarks</span></span>

<span data-ttu-id="6fe2f-121">L' *elemento critico* è l'elemento su cui è posizionato il mouse.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-121">The *hot item* is the item that the mouse is hovering over.</span></span> <span data-ttu-id="6fe2f-122">Questo messaggio rende un elemento simile a quello dell'elemento attivo anche se il mouse non è posizionato su di esso.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-122">This message makes an item look like it is the hot item even if the mouse is not hovering over it.</span></span>

<span data-ttu-id="6fe2f-123">Questo messaggio non ha alcun effetto visibile se lo stile [**\_ TRACKSELECT TV**](tree-view-control-window-styles.md) non è impostato.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-123">This message has no visible effect if the [**TVS\_TRACKSELECT**](tree-view-control-window-styles.md) style is not set.</span></span>

<span data-ttu-id="6fe2f-124">Se ha esito positivo, questo messaggio causa il ridisegnato dell'elemento sensibile.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-124">If it succeeds, this message causes the hot item to be redrawn.</span></span>

<span data-ttu-id="6fe2f-125">Questo messaggio viene ignorato se *lParam* è **null** e il controllo di visualizzazione albero tiene traccia del mouse.</span><span class="sxs-lookup"><span data-stu-id="6fe2f-125">This message is ignored if *lParam* is **NULL** and the tree-view control is tracking the mouse.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fe2f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fe2f-126">Requirements</span></span>



| <span data-ttu-id="6fe2f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fe2f-127">Requirement</span></span> | <span data-ttu-id="6fe2f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="6fe2f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe2f-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fe2f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6fe2f-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fe2f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6fe2f-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fe2f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6fe2f-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6fe2f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6fe2f-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6fe2f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fe2f-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fe2f-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fe2f-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fe2f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fe2f-136">**\_SetHot TreeView**</span><span class="sxs-lookup"><span data-stu-id="6fe2f-136">**TreeView\_SetHot**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





