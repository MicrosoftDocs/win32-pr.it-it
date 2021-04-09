---
title: Messaggio TVM_GETITEMHEIGHT (COMmctrl. h)
description: Recupera l'altezza corrente di ogni elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemHeight di TreeView.
ms.assetid: 017476a3-1929-4a31-97a7-0f66175d47ea
keywords:
- Controlli di Windows Message TVM_GETITEMHEIGHT
topic_type:
- apiref
api_name:
- TVM_GETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789347b7a50f9bb42a7aebb6fecddf24c42c559c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874662"
---
# <a name="tvm_getitemheight-message"></a><span data-ttu-id="36136-105">\_Messaggio GETITEMHEIGHT TVM</span><span class="sxs-lookup"><span data-stu-id="36136-105">TVM\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="36136-106">Recupera l'altezza corrente di ogni elemento della visualizzazione struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="36136-106">Retrieves the current height of the each tree-view item.</span></span> <span data-ttu-id="36136-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemHeight di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) .</span><span class="sxs-lookup"><span data-stu-id="36136-107">You can send this message explicitly or by using the [**TreeView\_GetItemHeight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="36136-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="36136-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36136-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36136-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="36136-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="36136-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="36136-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36136-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="36136-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="36136-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36136-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36136-113">Return value</span></span>

<span data-ttu-id="36136-114">Restituisce l'altezza, in pixel, di ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="36136-114">Returns the height of each item, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="36136-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36136-115">Requirements</span></span>



| <span data-ttu-id="36136-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="36136-116">Requirement</span></span> | <span data-ttu-id="36136-117">Valore</span><span class="sxs-lookup"><span data-stu-id="36136-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36136-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36136-118">Minimum supported client</span></span><br/> | <span data-ttu-id="36136-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36136-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36136-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36136-120">Minimum supported server</span></span><br/> | <span data-ttu-id="36136-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="36136-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36136-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36136-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="36136-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="36136-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36136-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36136-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36136-125">**\_SETITEMHEIGHT TVM**</span><span class="sxs-lookup"><span data-stu-id="36136-125">**TVM\_SETITEMHEIGHT**</span></span>](tvm-setitemheight.md)
</dt> </dl>

 

 





