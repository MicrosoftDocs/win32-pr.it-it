---
title: Messaggio TVM_GETVISIBLECOUNT (COMmctrl. h)
description: Ottiene il numero di elementi che possono essere completamente visibili nella finestra client di un controllo di visualizzazione ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetVisibleCount di TreeView.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- Controlli di Windows Message TVM_GETVISIBLECOUNT
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1927d21741b109c5f00aa964b058dc0c34732529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963931"
---
# <a name="tvm_getvisiblecount-message"></a><span data-ttu-id="14f9f-105">\_Messaggio GETVISIBLECOUNT TVM</span><span class="sxs-lookup"><span data-stu-id="14f9f-105">TVM\_GETVISIBLECOUNT message</span></span>

<span data-ttu-id="14f9f-106">Ottiene il numero di elementi che possono essere completamente visibili nella finestra client di un controllo di visualizzazione ad albero.</span><span class="sxs-lookup"><span data-stu-id="14f9f-106">Obtains the number of items that can be fully visible in the client window of a tree-view control.</span></span> <span data-ttu-id="14f9f-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetVisibleCount di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) .</span><span class="sxs-lookup"><span data-stu-id="14f9f-107">You can send this message explicitly or by using the [**TreeView\_GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="14f9f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="14f9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14f9f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14f9f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="14f9f-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="14f9f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="14f9f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14f9f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="14f9f-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="14f9f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14f9f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14f9f-113">Return value</span></span>

<span data-ttu-id="14f9f-114">Restituisce il numero di elementi che possono essere completamente visibili nella finestra del client del controllo di visualizzazione ad albero.</span><span class="sxs-lookup"><span data-stu-id="14f9f-114">Returns the number of items that can be fully visible in the client window of the tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="14f9f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="14f9f-115">Remarks</span></span>

<span data-ttu-id="14f9f-116">Il numero di elementi che possono essere completamente visibili può essere maggiore del numero di elementi nel controllo.</span><span class="sxs-lookup"><span data-stu-id="14f9f-116">The number of items that can be fully visible may be greater than the number of items in the control.</span></span> <span data-ttu-id="14f9f-117">Il controllo calcola questo valore dividendo l'altezza della finestra client per l'altezza di un elemento.</span><span class="sxs-lookup"><span data-stu-id="14f9f-117">The control calculates this value by dividing the height of the client window by the height of an item.</span></span>

<span data-ttu-id="14f9f-118">Si noti che il valore restituito è il numero di elementi che possono essere *completamente* visibili.</span><span class="sxs-lookup"><span data-stu-id="14f9f-118">Note that the return value is the number of items that can be *fully* visible.</span></span> <span data-ttu-id="14f9f-119">Se è possibile visualizzare tutti e 20 gli elementi e parte di uno più elementi, il valore restituito è 20.</span><span class="sxs-lookup"><span data-stu-id="14f9f-119">If you can see all of 20 items and part of one more item, the return value is 20.</span></span>

## <a name="requirements"></a><span data-ttu-id="14f9f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14f9f-120">Requirements</span></span>



| <span data-ttu-id="14f9f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="14f9f-121">Requirement</span></span> | <span data-ttu-id="14f9f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="14f9f-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14f9f-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14f9f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="14f9f-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14f9f-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14f9f-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14f9f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="14f9f-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14f9f-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14f9f-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14f9f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="14f9f-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="14f9f-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





