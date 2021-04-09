---
title: Messaggio TTM_TRACKPOSITION (COMmctrl. h)
description: Imposta la posizione di una descrizione comando di rilevamento.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- Controlli di Windows Message TTM_TRACKPOSITION
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6eab8184049d8bf876a7e782b9adc2091d5fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048515"
---
# <a name="ttm_trackposition-message"></a><span data-ttu-id="49ccb-104">\_Messaggio TTM TRACKPOSITION</span><span class="sxs-lookup"><span data-stu-id="49ccb-104">TTM\_TRACKPOSITION message</span></span>

<span data-ttu-id="49ccb-105">Imposta la posizione di una descrizione comando di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="49ccb-105">Sets the position of a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="49ccb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="49ccb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49ccb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49ccb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49ccb-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="49ccb-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="49ccb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49ccb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49ccb-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la coordinata x del punto in corrispondenza del quale verrà visualizzata la descrizione comando di rilevamento, espressa in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="49ccb-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span> <span data-ttu-id="49ccb-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la coordinata y del punto in corrispondenza del quale verrà visualizzata la descrizione comando di rilevamento, espressa in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="49ccb-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49ccb-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49ccb-112">Return value</span></span>

<span data-ttu-id="49ccb-113">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="49ccb-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="49ccb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="49ccb-114">Remarks</span></span>

<span data-ttu-id="49ccb-115">Il controllo ToolTip sceglie la posizione in cui visualizzare la finestra della descrizione comando in base alle coordinate fornite con il messaggio.</span><span class="sxs-lookup"><span data-stu-id="49ccb-115">The tooltip control chooses where to display the tooltip window based on the coordinates you provide with this message.</span></span> <span data-ttu-id="49ccb-116">In questo modo la finestra della descrizione comando viene visualizzata accanto allo strumento a cui corrisponde.</span><span class="sxs-lookup"><span data-stu-id="49ccb-116">This causes the tooltip window to appear beside the tool to which it corresponds.</span></span> <span data-ttu-id="49ccb-117">Per visualizzare le finestre della descrizione comando in coordinate specifiche, includere il \_ flag assoluto ttf nel membro **uFlags** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) quando si aggiunge lo strumento.</span><span class="sxs-lookup"><span data-stu-id="49ccb-117">To have tooltip windows displayed at specific coordinates, include the TTF\_ABSOLUTE flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when adding the tool.</span></span>

## <a name="requirements"></a><span data-ttu-id="49ccb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49ccb-118">Requirements</span></span>



| <span data-ttu-id="49ccb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="49ccb-119">Requirement</span></span> | <span data-ttu-id="49ccb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="49ccb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49ccb-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49ccb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="49ccb-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49ccb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49ccb-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49ccb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="49ccb-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49ccb-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49ccb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49ccb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="49ccb-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49ccb-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49ccb-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49ccb-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="49ccb-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="49ccb-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="49ccb-129">**\_TRACKACTIVATE TTM**</span><span class="sxs-lookup"><span data-stu-id="49ccb-129">**TTM\_TRACKACTIVATE**</span></span>](ttm-trackactivate.md)
</dt> <dt>

<span data-ttu-id="49ccb-130">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="49ccb-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="49ccb-131">Uso di controlli ToolTip</span><span class="sxs-lookup"><span data-stu-id="49ccb-131">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

