---
title: Messaggio CB_GETDROPPEDSTATE (winuser. h)
description: Determina se la casella di riepilogo di una casella combinata viene rilasciata.
ms.assetid: a3f4e352-298d-45ea-a5a7-007f1fc1a387
keywords:
- Controlli di Windows Message CB_GETDROPPEDSTATE
topic_type:
- apiref
api_name:
- CB_GETDROPPEDSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae321bbaa3078a04ffc97d4a8083a674d03d651
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048778"
---
# <a name="cb_getdroppedstate-message"></a><span data-ttu-id="921fe-104">\_Messaggio GETDROPPEDSTATE CB</span><span class="sxs-lookup"><span data-stu-id="921fe-104">CB\_GETDROPPEDSTATE message</span></span>

<span data-ttu-id="921fe-105">Determina se la casella di riepilogo di una casella combinata viene rilasciata.</span><span class="sxs-lookup"><span data-stu-id="921fe-105">Determines whether the list box of a combo box is dropped down.</span></span>

## <a name="parameters"></a><span data-ttu-id="921fe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="921fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="921fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="921fe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="921fe-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="921fe-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="921fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="921fe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="921fe-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="921fe-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="921fe-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="921fe-111">Return value</span></span>

<span data-ttu-id="921fe-112">Se la casella di riepilogo è visibile, il valore restituito è **true**; in caso contrario, è **false**.</span><span class="sxs-lookup"><span data-stu-id="921fe-112">If the list box is visible, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="921fe-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="921fe-113">Requirements</span></span>



| <span data-ttu-id="921fe-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="921fe-114">Requirement</span></span> | <span data-ttu-id="921fe-115">Valore</span><span class="sxs-lookup"><span data-stu-id="921fe-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="921fe-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="921fe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="921fe-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="921fe-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="921fe-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="921fe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="921fe-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="921fe-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="921fe-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="921fe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="921fe-121"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="921fe-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="921fe-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="921fe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="921fe-123">**CB \_ SHOWDROPDOWN**</span><span class="sxs-lookup"><span data-stu-id="921fe-123">**CB\_SHOWDROPDOWN**</span></span>](cb-showdropdown.md)
</dt> </dl>

 

 





