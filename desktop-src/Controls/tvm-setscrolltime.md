---
title: Messaggio TVM_SETSCROLLTIME (COMmctrl. h)
description: Imposta il tempo massimo di scorrimento per il controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetScrollTime di TreeView.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- Controlli di Windows Message TVM_SETSCROLLTIME
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fab2f662b5ec641d9ffc6cc276f2196d2613e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301834"
---
# <a name="tvm_setscrolltime-message"></a><span data-ttu-id="7fe94-105">\_Messaggio SETSCROLLTIME TVM</span><span class="sxs-lookup"><span data-stu-id="7fe94-105">TVM\_SETSCROLLTIME message</span></span>

<span data-ttu-id="7fe94-106">Imposta il tempo massimo di scorrimento per il controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="7fe94-106">Sets the maximum scroll time for the tree-view control.</span></span> <span data-ttu-id="7fe94-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetScrollTime di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) .</span><span class="sxs-lookup"><span data-stu-id="7fe94-107">You can send this message explicitly or by using the [**TreeView\_SetScrollTime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7fe94-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fe94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fe94-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7fe94-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7fe94-110">Nuovo tempo di scorrimento massimo, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="7fe94-110">New maximum scroll time, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="7fe94-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fe94-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7fe94-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7fe94-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fe94-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fe94-113">Return value</span></span>

<span data-ttu-id="7fe94-114">Restituisce il tempo di scorrimento massimo precedente, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="7fe94-114">Returns the previous maximum scroll time, in milliseconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fe94-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7fe94-115">Remarks</span></span>

<span data-ttu-id="7fe94-116">Il tempo massimo di scorrimento è la quantità di tempo più lungo che può essere eseguita da un'operazione di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="7fe94-116">The maximum scroll time is the longest amount of time that a scroll operation can take.</span></span> <span data-ttu-id="7fe94-117">Lo scorrimento viene regolato in modo che lo scorrimento avvenga entro il tempo massimo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="7fe94-117">Scrolling will be adjusted so that the scroll will take place within the maximum scroll time.</span></span> <span data-ttu-id="7fe94-118">Un'operazione di scorrimento potrebbe richiedere meno tempo rispetto al valore massimo.</span><span class="sxs-lookup"><span data-stu-id="7fe94-118">A scroll operation may take less time than the maximum.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fe94-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fe94-119">Requirements</span></span>



| <span data-ttu-id="7fe94-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fe94-120">Requirement</span></span> | <span data-ttu-id="7fe94-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7fe94-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe94-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fe94-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe94-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7fe94-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fe94-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fe94-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe94-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7fe94-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7fe94-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7fe94-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fe94-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fe94-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fe94-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fe94-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fe94-129">**\_GETSCROLLTIME TVM**</span><span class="sxs-lookup"><span data-stu-id="7fe94-129">**TVM\_GETSCROLLTIME**</span></span>](tvm-getscrolltime.md)
</dt> </dl>

 

 





