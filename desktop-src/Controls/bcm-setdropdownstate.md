---
title: Messaggio BCM_SETDROPDOWNSTATE (COMmctrl. h)
description: Imposta lo stato di elenco a discesa per un pulsante con lo stile \_ elenco a discesa TBSTYLE. Inviare questo messaggio in modo esplicito o tramite il pulsante \_ SetDropDownState macro.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- Controlli di Windows Message BCM_SETDROPDOWNSTATE
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc44ec58d40e047708591121f81c84f327ca47c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119739"
---
# <a name="bcm_setdropdownstate-message"></a><span data-ttu-id="a4f0d-105">\_Messaggio SETDROPDOWNSTATE BCM</span><span class="sxs-lookup"><span data-stu-id="a4f0d-105">BCM\_SETDROPDOWNSTATE message</span></span>

<span data-ttu-id="a4f0d-106">Imposta lo stato di elenco a discesa per un pulsante con lo stile [**\_ elenco a discesa TBSTYLE**](toolbar-control-and-button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="a4f0d-106">Sets the drop down state for a button with style [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span> <span data-ttu-id="a4f0d-107">Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) macro.</span><span class="sxs-lookup"><span data-stu-id="a4f0d-107">Send this message explicitly or by using the [**Button\_SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a4f0d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4f0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f0d-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4f0d-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f0d-110">**Bool** che è **true** per lo stato di BST \_ DROPDOWNPUSHED o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a4f0d-110">A **BOOL** that is **TRUE** for state of BST\_DROPDOWNPUSHED, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="a4f0d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4f0d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4f0d-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a4f0d-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f0d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4f0d-113">Return value</span></span>

<span data-ttu-id="a4f0d-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a4f0d-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f0d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4f0d-115">Requirements</span></span>



| <span data-ttu-id="a4f0d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4f0d-116">Requirement</span></span> | <span data-ttu-id="a4f0d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a4f0d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f0d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4f0d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f0d-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4f0d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4f0d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4f0d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f0d-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4f0d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a4f0d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4f0d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4f0d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4f0d-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f0d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4f0d-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="a4f0d-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a4f0d-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a4f0d-126">Stili dei pulsanti</span><span class="sxs-lookup"><span data-stu-id="a4f0d-126">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="a4f0d-127">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a4f0d-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a4f0d-128">Tipi di pulsante</span><span class="sxs-lookup"><span data-stu-id="a4f0d-128">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





