---
title: Messaggio TVM_INSERTITEM (COMmctrl. h)
description: Inserisce un nuovo elemento in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TreeView InsertItem.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- Controlli di Windows Message TVM_INSERTITEM
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719de4c2391ff924c9f6deb8cb4206cfdb56c3ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873517"
---
# <a name="tvm_insertitem-message"></a><span data-ttu-id="d2dac-105">\_Messaggio INSERTITEM INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="d2dac-105">TVM\_INSERTITEM message</span></span>

<span data-ttu-id="d2dac-106">Inserisce un nuovo elemento in un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="d2dac-106">Inserts a new item in a tree-view control.</span></span> <span data-ttu-id="d2dac-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TreeView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="d2dac-107">You can send this message explicitly or by using the [**TreeView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2dac-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2dac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2dac-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2dac-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d2dac-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d2dac-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d2dac-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2dac-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2dac-112">Puntatore a una struttura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) che specifica gli attributi dell'elemento della visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="d2dac-112">Pointer to a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure that specifies the attributes of the tree-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2dac-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2dac-113">Return value</span></span>

<span data-ttu-id="d2dac-114">Restituisce l'handle **HTREEITEM** al nuovo elemento in caso di esito positivo; in caso contrario, **null** .</span><span class="sxs-lookup"><span data-stu-id="d2dac-114">Returns the **HTREEITEM** handle to the new item if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2dac-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2dac-115">Requirements</span></span>



| <span data-ttu-id="d2dac-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2dac-116">Requirement</span></span> | <span data-ttu-id="d2dac-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d2dac-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2dac-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2dac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d2dac-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2dac-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2dac-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2dac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d2dac-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2dac-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2dac-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2dac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2dac-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2dac-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d2dac-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d2dac-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d2dac-125">**TVM \_ INSERTITEMW** (Unicode) e **TVM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d2dac-125">**TVM\_INSERTITEMW** (Unicode) and **TVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d2dac-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2dac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2dac-127">\_ENDLABELEDIT TVN</span><span class="sxs-lookup"><span data-stu-id="d2dac-127">TVN\_ENDLABELEDIT</span></span>](tvn-endlabeledit.md)
</dt> </dl>

 

 





