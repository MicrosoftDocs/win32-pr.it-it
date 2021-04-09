---
title: Messaggio TVM_SETITEMHEIGHT (COMmctrl. h)
description: Imposta l'altezza degli elementi della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetItemHeight di TreeView.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- Controlli di Windows Message TVM_SETITEMHEIGHT
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114769f689cbf8d9475460e40d205c4282a1a787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964382"
---
# <a name="tvm_setitemheight-message"></a><span data-ttu-id="9384c-105">\_Messaggio SETITEMHEIGHT TVM</span><span class="sxs-lookup"><span data-stu-id="9384c-105">TVM\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="9384c-106">Imposta l'altezza degli elementi della visualizzazione struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="9384c-106">Sets the height of the tree-view items.</span></span> <span data-ttu-id="9384c-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetItemHeight di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) .</span><span class="sxs-lookup"><span data-stu-id="9384c-107">You can send this message explicitly or by using the [**TreeView\_SetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9384c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9384c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9384c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9384c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9384c-110">Nuova altezza di ogni elemento nella visualizzazione albero, in pixel.</span><span class="sxs-lookup"><span data-stu-id="9384c-110">New height of every item in the tree view, in pixels.</span></span> <span data-ttu-id="9384c-111">L'altezza minore di 1 verrà impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="9384c-111">Heights less than 1 will be set to 1.</span></span> <span data-ttu-id="9384c-112">Se questo argomento non è pari e il controllo di visualizzazione albero non ha lo stile [**\_ NONEVENHEIGHT TVS**](tree-view-control-window-styles.md) , questo valore verrà arrotondato per difetto al valore pari più vicino.</span><span class="sxs-lookup"><span data-stu-id="9384c-112">If this argument is not even and the tree-view control does not have the [**TVS\_NONEVENHEIGHT**](tree-view-control-window-styles.md) style, this value will be rounded down to the nearest even value.</span></span> <span data-ttu-id="9384c-113">Se questo argomento è-1, il controllo verrà ripristinato utilizzando l'altezza predefinita dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="9384c-113">If this argument is -1, the control will revert to using its default item height.</span></span>

</dd> <dt>

<span data-ttu-id="9384c-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9384c-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9384c-115">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9384c-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9384c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9384c-116">Return value</span></span>

<span data-ttu-id="9384c-117">Restituisce l'altezza precedente, in pixel, degli elementi.</span><span class="sxs-lookup"><span data-stu-id="9384c-117">Returns the previous height of the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="9384c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="9384c-118">Remarks</span></span>

<span data-ttu-id="9384c-119">Il controllo di visualizzazione albero utilizza questo valore per l'altezza di tutti gli elementi.</span><span class="sxs-lookup"><span data-stu-id="9384c-119">The tree-view control uses this value for the height of all items.</span></span> <span data-ttu-id="9384c-120">Per modificare l'altezza dei singoli elementi, vedere la descrizione del membro **iIntegral** della struttura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .</span><span class="sxs-lookup"><span data-stu-id="9384c-120">To modify the height of individual items, see the description of the **iIntegral** member of the [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="9384c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9384c-121">Requirements</span></span>



| <span data-ttu-id="9384c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9384c-122">Requirement</span></span> | <span data-ttu-id="9384c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9384c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9384c-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9384c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9384c-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9384c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9384c-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9384c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9384c-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9384c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9384c-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9384c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9384c-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9384c-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9384c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9384c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9384c-131">**\_GETITEMHEIGHT TVM**</span><span class="sxs-lookup"><span data-stu-id="9384c-131">**TVM\_GETITEMHEIGHT**</span></span>](tvm-getitemheight.md)
</dt> </dl>

 

 





