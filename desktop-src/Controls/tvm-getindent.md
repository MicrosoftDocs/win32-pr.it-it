---
title: Messaggio TVM_GETINDENT (COMmctrl. h)
description: Recupera la quantità, in pixel, in base alla quale gli elementi figlio vengono rientrati rispetto ai relativi elementi padre. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TreeView GetIndent.
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- Controlli di Windows Message TVM_GETINDENT
topic_type:
- apiref
api_name:
- TVM_GETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33775341adc47d84ead9a633d7d31b16ffc4a723
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874478"
---
# <a name="tvm_getindent-message"></a><span data-ttu-id="d074d-105">\_Messaggio TVM GETindent</span><span class="sxs-lookup"><span data-stu-id="d074d-105">TVM\_GETINDENT message</span></span>

<span data-ttu-id="d074d-106">Recupera la quantità, in pixel, in base alla quale gli elementi figlio vengono rientrati rispetto ai relativi elementi padre.</span><span class="sxs-lookup"><span data-stu-id="d074d-106">Retrieves the amount, in pixels, that child items are indented relative to their parent items.</span></span> <span data-ttu-id="d074d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TreeView \_ GetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) .</span><span class="sxs-lookup"><span data-stu-id="d074d-107">You can send this message explicitly or by using the [**TreeView\_GetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d074d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d074d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d074d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d074d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d074d-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d074d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d074d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d074d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d074d-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d074d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d074d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d074d-113">Return value</span></span>

<span data-ttu-id="d074d-114">Restituisce la quantità di rientri.</span><span class="sxs-lookup"><span data-stu-id="d074d-114">Returns the amount of indentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d074d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d074d-115">Requirements</span></span>



| <span data-ttu-id="d074d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d074d-116">Requirement</span></span> | <span data-ttu-id="d074d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d074d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d074d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d074d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d074d-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d074d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d074d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d074d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d074d-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d074d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d074d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d074d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d074d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d074d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





