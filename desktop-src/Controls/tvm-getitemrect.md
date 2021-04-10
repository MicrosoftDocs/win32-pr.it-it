---
title: Messaggio TVM_GETITEMRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione per un elemento della visualizzazione struttura ad albero e indica se l'elemento è visibile. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemRect di TreeView.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- Controlli di Windows Message TVM_GETITEMRECT
topic_type:
- apiref
api_name:
- TVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebdf4d73fb83ddbd8e9e682f11ee1f5ecfbd5153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119567"
---
# <a name="tvm_getitemrect-message"></a><span data-ttu-id="6d4bd-105">\_Messaggio GETITEMRECT TVM</span><span class="sxs-lookup"><span data-stu-id="6d4bd-105">TVM\_GETITEMRECT message</span></span>

<span data-ttu-id="6d4bd-106">Recupera il rettangolo di delimitazione per un elemento della visualizzazione struttura ad albero e indica se l'elemento è visibile.</span><span class="sxs-lookup"><span data-stu-id="6d4bd-106">Retrieves the bounding rectangle for a tree-view item and indicates whether the item is visible.</span></span> <span data-ttu-id="6d4bd-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemRect di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="6d4bd-107">You can send this message explicitly or by using the [**TreeView\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d4bd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d4bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d4bd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d4bd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d4bd-110">Valore che specifica la parte dell'elemento per la quale recuperare il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="6d4bd-110">Value specifying the portion of the item for which to retrieve the bounding rectangle.</span></span> <span data-ttu-id="6d4bd-111">Se questo parametro è **true**, il rettangolo di delimitazione include solo il testo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="6d4bd-111">If this parameter is **TRUE**, the bounding rectangle includes only the text of the item.</span></span> <span data-ttu-id="6d4bd-112">In caso contrario, include l'intera riga occupata dall'elemento nel controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="6d4bd-112">Otherwise, it includes the entire line that the item occupies in the tree-view control.</span></span>

</dd> <dt>

<span data-ttu-id="6d4bd-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d4bd-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d4bd-114">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che, quando invia il messaggio, contiene l'handle dell'elemento per il quale recuperare il rettangolo.</span><span class="sxs-lookup"><span data-stu-id="6d4bd-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that, when sending the message, contains the handle of the item to retrieve the rectangle for.</span></span> <span data-ttu-id="6d4bd-115">Vedere l'esempio seguente per altre informazioni su come inserire l'handle di elemento in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6d4bd-115">See the example below for more information on how to place the item handle in this parameter.</span></span> <span data-ttu-id="6d4bd-116">Dopo la restituzione dal messaggio, questo parametro contiene il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="6d4bd-116">After returning from the message, this parameter contains the bounding rectangle.</span></span> <span data-ttu-id="6d4bd-117">Le coordinate sono relative all'angolo superiore sinistro del controllo di visualizzazione ad albero.</span><span class="sxs-lookup"><span data-stu-id="6d4bd-117">The coordinates are relative to the upper-left corner of the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d4bd-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d4bd-118">Return value</span></span>

<span data-ttu-id="6d4bd-119">Se l'elemento è visibile e il rettangolo di delimitazione è stato recuperato correttamente, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="6d4bd-119">If the item is visible and the bounding rectangle was successfully retrieved, the return value is **TRUE**.</span></span> <span data-ttu-id="6d4bd-120">In caso contrario, il messaggio restituisce **false** e non recupera il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="6d4bd-120">Otherwise, the message returns **FALSE** and does not retrieve the bounding rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d4bd-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d4bd-121">Remarks</span></span>

<span data-ttu-id="6d4bd-122">Quando si invia questo messaggio, il parametro *lParam* contiene l'handle dell'elemento per il quale viene recuperato il rettangolo.</span><span class="sxs-lookup"><span data-stu-id="6d4bd-122">When sending this message, the *lParam* parameter contains the handle of the item that the rectangle is being retrieved for.</span></span> <span data-ttu-id="6d4bd-123">L'handle viene inserito in *lParam* come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="6d4bd-123">The handle is placed in *lParam* as shown in the following example:</span></span>


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a><span data-ttu-id="6d4bd-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d4bd-124">Requirements</span></span>



| <span data-ttu-id="6d4bd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d4bd-125">Requirement</span></span> | <span data-ttu-id="6d4bd-126">Valore</span><span class="sxs-lookup"><span data-stu-id="6d4bd-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d4bd-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d4bd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6d4bd-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d4bd-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d4bd-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d4bd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6d4bd-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d4bd-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d4bd-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d4bd-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d4bd-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d4bd-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

