---
title: Messaggio TVM_SETITEM (COMmctrl. h)
description: Il messaggio della macchina virtuale TVM \_ imposta alcuni o tutti gli attributi di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro elemento TreeView.
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- Controlli di Windows Message TVM_SETITEM
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95750af3aa43a25f0ff4eae5533df5d9aef23537
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476949"
---
# <a name="tvm_setitem-message"></a><span data-ttu-id="ce26d-105">\_Messaggio di SETITEM TVM</span><span class="sxs-lookup"><span data-stu-id="ce26d-105">TVM\_SETITEM message</span></span>

<span data-ttu-id="ce26d-106">Il messaggio della macchina virtuale **TVM \_** imposta alcuni o tutti gli attributi di un elemento della visualizzazione struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="ce26d-106">The **TVM\_SETITEM** message sets some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="ce26d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ elemento TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) .</span><span class="sxs-lookup"><span data-stu-id="ce26d-107">You can send this message explicitly or by using the [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce26d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce26d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce26d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce26d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce26d-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ce26d-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ce26d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce26d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce26d-112">Puntatore a una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene gli attributi del nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="ce26d-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="ce26d-113">Con la [versione 4,71](common-control-versions.md) e successive, è invece possibile usare una struttura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .</span><span class="sxs-lookup"><span data-stu-id="ce26d-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce26d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce26d-114">Return value</span></span>

<span data-ttu-id="ce26d-115">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ce26d-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce26d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce26d-116">Remarks</span></span>

<span data-ttu-id="ce26d-117">Il membro **hitey** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica l'elemento e il membro **mask** specifica gli attributi da impostare.</span><span class="sxs-lookup"><span data-stu-id="ce26d-117">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item, and the **mask** member specifies which attributes to set.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce26d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce26d-118">Requirements</span></span>



| <span data-ttu-id="ce26d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce26d-119">Requirement</span></span> | <span data-ttu-id="ce26d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ce26d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce26d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce26d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ce26d-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce26d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce26d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce26d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ce26d-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ce26d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce26d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce26d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce26d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce26d-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ce26d-127">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ce26d-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ce26d-128">**TVM \_ SETITEMW** (Unicode) e **TVM \_ seitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ce26d-128">**TVM\_SETITEMW** (Unicode) and **TVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





