---
title: Messaggio LVM_GETTOOLTIPS (COMmctrl. h)
description: Recupera il controllo ToolTip utilizzato dal controllo visualizzazione elenco per visualizzare le descrizioni comandi. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView GetToolTips.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- Controlli di Windows Message LVM_GETTOOLTIPS
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478509"
---
# <a name="lvm_gettooltips-message"></a><span data-ttu-id="7fe56-105">Messaggio di LVM \_ GETtooltips</span><span class="sxs-lookup"><span data-stu-id="7fe56-105">LVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="7fe56-106">Recupera il controllo ToolTip utilizzato dal controllo visualizzazione elenco per visualizzare le descrizioni comandi.</span><span class="sxs-lookup"><span data-stu-id="7fe56-106">Retrieves the tooltip control that the list-view control uses to display tooltips.</span></span> <span data-ttu-id="7fe56-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**ListView \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="7fe56-107">You can send this message explicitly or use the [**ListView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7fe56-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fe56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fe56-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7fe56-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7fe56-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7fe56-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7fe56-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7fe56-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7fe56-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7fe56-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fe56-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fe56-113">Return value</span></span>

<span data-ttu-id="7fe56-114">Restituisce l'handle del controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="7fe56-114">Returns the handle of the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fe56-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fe56-115">Requirements</span></span>



| <span data-ttu-id="7fe56-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fe56-116">Requirement</span></span> | <span data-ttu-id="7fe56-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7fe56-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe56-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fe56-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe56-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7fe56-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7fe56-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fe56-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe56-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7fe56-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7fe56-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7fe56-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fe56-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fe56-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fe56-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fe56-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fe56-125">**\_descrizioni comando LVM**</span><span class="sxs-lookup"><span data-stu-id="7fe56-125">**LVM\_SETTOOLTIPS**</span></span>](lvm-settooltips.md)
</dt> </dl>

 

 





