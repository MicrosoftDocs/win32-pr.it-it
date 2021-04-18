---
title: Messaggio PGM_FORWARDMOUSE (COMmctrl. h)
description: Abilita o Disabilita l'avanzamento del mouse per il controllo pager. Quando l'avanzamento del mouse è abilitato, il controllo pager trasmette i \_ messaggi di WM MOUSEMOVE alla finestra contenuta. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro ForwardMouse del cercapersone.
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- Controlli di Windows Message PGM_FORWARDMOUSE
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: addc1c6bf762f540e9d7d785a5af2ba3fb7da93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302052"
---
# <a name="pgm_forwardmouse-message"></a><span data-ttu-id="d3dbd-106">\_Messaggio FORWARDMOUSE PGM</span><span class="sxs-lookup"><span data-stu-id="d3dbd-106">PGM\_FORWARDMOUSE message</span></span>

<span data-ttu-id="d3dbd-107">Abilita o Disabilita l'avanzamento del mouse per il controllo pager.</span><span class="sxs-lookup"><span data-stu-id="d3dbd-107">Enables or disables mouse forwarding for the pager control.</span></span> <span data-ttu-id="d3dbd-108">Quando l'avanzamento del mouse è abilitato, il controllo pager trasmette i messaggi di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) alla finestra contenuta.</span><span class="sxs-lookup"><span data-stu-id="d3dbd-108">When mouse forwarding is enabled, the pager control forwards [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to the contained window.</span></span> <span data-ttu-id="d3dbd-109">È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ ForwardMouse del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) .</span><span class="sxs-lookup"><span data-stu-id="d3dbd-109">You can send this message explicitly or use the [**Pager\_ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3dbd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3dbd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3dbd-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3dbd-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3dbd-112">Valore **bool** che determina se l'avanzamento del mouse è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d3dbd-112">**BOOL** value that determines if mouse forwarding is enabled or disabled.</span></span> <span data-ttu-id="d3dbd-113">Se questo valore è diverso da zero, l'avanzamento del mouse è abilitato.</span><span class="sxs-lookup"><span data-stu-id="d3dbd-113">If this value is nonzero, mouse forwarding is enabled.</span></span> <span data-ttu-id="d3dbd-114">Se questo valore è zero, l'avanzamento del mouse è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d3dbd-114">If this value is zero, mouse forwarding is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="d3dbd-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3dbd-115">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d3dbd-116">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d3dbd-116">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3dbd-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3dbd-117">Return value</span></span>

<span data-ttu-id="d3dbd-118">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d3dbd-118">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3dbd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3dbd-119">Requirements</span></span>



| <span data-ttu-id="d3dbd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3dbd-120">Requirement</span></span> | <span data-ttu-id="d3dbd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d3dbd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3dbd-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3dbd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d3dbd-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3dbd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3dbd-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3dbd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d3dbd-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3dbd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d3dbd-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3dbd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3dbd-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3dbd-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

