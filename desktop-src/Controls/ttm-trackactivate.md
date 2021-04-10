---
title: Messaggio TTM_TRACKACTIVATE (COMmctrl. h)
description: Attiva o disattiva una descrizione comando di rilevamento.
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- Controlli di Windows Message TTM_TRACKACTIVATE
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964466"
---
# <a name="ttm_trackactivate-message"></a><span data-ttu-id="d9782-104">\_Messaggio TTM TRACKACTIVATE</span><span class="sxs-lookup"><span data-stu-id="d9782-104">TTM\_TRACKACTIVATE message</span></span>

<span data-ttu-id="d9782-105">Attiva o disattiva una descrizione comando di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="d9782-105">Activates or deactivates a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9782-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9782-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9782-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9782-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9782-108">Valore che specifica se è in corso l'attivazione o la disattivazione del rilevamento.</span><span class="sxs-lookup"><span data-stu-id="d9782-108">Value specifying whether tracking is being activated or deactivated.</span></span> <span data-ttu-id="d9782-109">I valori validi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9782-109">This value can be one of the following:</span></span>



| <span data-ttu-id="d9782-110">Valore</span><span class="sxs-lookup"><span data-stu-id="d9782-110">Value</span></span>                                                                                                                                | <span data-ttu-id="d9782-111">Significato</span><span class="sxs-lookup"><span data-stu-id="d9782-111">Meaning</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="d9782-112"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="d9782-112"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="d9782-113">Attivare il rilevamento.</span><span class="sxs-lookup"><span data-stu-id="d9782-113">Activate tracking.</span></span><br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="d9782-114"><dt>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="d9782-114"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="d9782-115">Disattiva il rilevamento.</span><span class="sxs-lookup"><span data-stu-id="d9782-115">Deactivate tracking.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d9782-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9782-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9782-117">Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) che identifica lo strumento a cui si applica questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="d9782-117">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that identifies the tool to which this message applies.</span></span> <span data-ttu-id="d9782-118">I membri **HWND** e **UID** identificano lo strumento e il membro **cbSize** specifica le dimensioni della struttura.</span><span class="sxs-lookup"><span data-stu-id="d9782-118">The **hwnd** and **uId** members identify the tool, and the **cbSize** member specifies the size of the structure.</span></span> <span data-ttu-id="d9782-119">Tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="d9782-119">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9782-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9782-120">Return value</span></span>

<span data-ttu-id="d9782-121">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d9782-121">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9782-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9782-122">Requirements</span></span>



| <span data-ttu-id="d9782-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9782-123">Requirement</span></span> | <span data-ttu-id="d9782-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d9782-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9782-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9782-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d9782-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9782-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9782-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9782-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d9782-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d9782-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9782-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9782-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9782-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9782-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9782-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9782-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="d9782-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d9782-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d9782-133">**\_TRACKPOSITION TTM**</span><span class="sxs-lookup"><span data-stu-id="d9782-133">**TTM\_TRACKPOSITION**</span></span>](ttm-trackposition.md)
</dt> <dt>

<span data-ttu-id="d9782-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d9782-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d9782-135">Uso di controlli ToolTip</span><span class="sxs-lookup"><span data-stu-id="d9782-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 





