---
title: Messaggio TVM_GETSCROLLTIME (COMmctrl. h)
description: Recupera il tempo massimo di scorrimento per il controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetScrollTime di TreeView.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- Controlli di Windows Message TVM_GETSCROLLTIME
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f0bacc6c12dd7f54f20d882faf738c11848d59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119315"
---
# <a name="tvm_getscrolltime-message"></a><span data-ttu-id="f80dd-105">\_Messaggio GETSCROLLTIME TVM</span><span class="sxs-lookup"><span data-stu-id="f80dd-105">TVM\_GETSCROLLTIME message</span></span>

<span data-ttu-id="f80dd-106">Recupera il tempo massimo di scorrimento per il controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="f80dd-106">Retrieves the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="f80dd-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetScrollTime di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) .</span><span class="sxs-lookup"><span data-stu-id="f80dd-107">You can send this message explicitly or by using the [**TreeView\_GetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f80dd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f80dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f80dd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f80dd-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f80dd-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f80dd-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f80dd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f80dd-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f80dd-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f80dd-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f80dd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f80dd-113">Return value</span></span>

<span data-ttu-id="f80dd-114">Restituisce il tempo massimo di scorrimento, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="f80dd-114">Returns the maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="f80dd-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f80dd-115">Remarks</span></span>

<span data-ttu-id="f80dd-116">Il tempo massimo di scorrimento è la quantità di tempo più lungo che può essere eseguita da un'operazione di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="f80dd-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="f80dd-117">Lo scorrimento verrà regolato in modo che lo scorrimento avvenga entro il tempo massimo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="f80dd-117">The scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="f80dd-118">Un'operazione di scorrimento potrebbe richiedere meno tempo rispetto al valore massimo.</span><span class="sxs-lookup"><span data-stu-id="f80dd-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="f80dd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f80dd-119">Requirements</span></span>



| <span data-ttu-id="f80dd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f80dd-120">Requirement</span></span> | <span data-ttu-id="f80dd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f80dd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f80dd-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f80dd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f80dd-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f80dd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f80dd-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f80dd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f80dd-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f80dd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f80dd-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f80dd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f80dd-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f80dd-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f80dd-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f80dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f80dd-129">**\_SETSCROLLTIME TVM**</span><span class="sxs-lookup"><span data-stu-id="f80dd-129">**TVM\_SETSCROLLTIME**</span></span>](tvm-setscrolltime.md)
</dt> </dl>

 

 





