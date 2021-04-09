---
title: Messaggio TVM_GETITEMSTATE (COMmctrl. h)
description: Recupera alcuni o tutti gli attributi di stato di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemState di TreeView.
ms.assetid: 89aaaa82-2809-4e4e-a325-5666a57c5cbb
keywords:
- Controlli di Windows Message TVM_GETITEMSTATE
topic_type:
- apiref
api_name:
- TVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b851ff3845743c802a2a914a0f40d5d9eb65c6a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048544"
---
# <a name="tvm_getitemstate-message"></a><span data-ttu-id="ab028-105">\_Messaggio GETITEMSTATE TVM</span><span class="sxs-lookup"><span data-stu-id="ab028-105">TVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="ab028-106">Recupera alcuni o tutti gli attributi di stato di un elemento della visualizzazione struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="ab028-106">Retrieves some or all of a tree-view item's state attributes.</span></span> <span data-ttu-id="ab028-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemState di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) .</span><span class="sxs-lookup"><span data-stu-id="ab028-107">You can send this message explicitly or by using the [**TreeView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab028-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab028-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab028-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ab028-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab028-110">Handle per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="ab028-110">Handle to the item.</span></span>

</dd> <dt>

<span data-ttu-id="ab028-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab028-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab028-112">Maschera utilizzata per specificare gli stati in cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="ab028-112">Mask used to specify the states to query for.</span></span> <span data-ttu-id="ab028-113">Equivale al membro **stateMask** di [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span><span class="sxs-lookup"><span data-stu-id="ab028-113">It is equivalent to the **stateMask** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab028-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab028-114">Return value</span></span>

<span data-ttu-id="ab028-115">Restituisce un valore **uint** con i bit di stato appropriati impostati su **true**.</span><span class="sxs-lookup"><span data-stu-id="ab028-115">Returns a **UINT** value with the appropriate state bits set to **TRUE**.</span></span> <span data-ttu-id="ab028-116">Verranno impostati solo i bit specificati da *lParam* e che sono **true** .</span><span class="sxs-lookup"><span data-stu-id="ab028-116">Only those bits that are specified by *lParam* and that are **TRUE** will be set.</span></span> <span data-ttu-id="ab028-117">Questo valore è equivalente al membro di **stato** di [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span><span class="sxs-lookup"><span data-stu-id="ab028-117">This value is equivalent to the **state** member of [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab028-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab028-118">Requirements</span></span>



| <span data-ttu-id="ab028-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab028-119">Requirement</span></span> | <span data-ttu-id="ab028-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ab028-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ab028-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab028-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ab028-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab028-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab028-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab028-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ab028-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ab028-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ab028-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab028-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab028-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab028-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





