---
title: Messaggio TTM_SETDELAYTIME (COMmctrl. h)
description: Imposta le durate iniziali, popup e reshow per un controllo ToolTip.
ms.assetid: 0a73def0-550c-4d01-9cb1-1eb1f4356fa3
keywords:
- Controlli di Windows Message TTM_SETDELAYTIME
topic_type:
- apiref
api_name:
- TTM_SETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b633dc75baa0a8f385cf8cdb9bf7e9fa254809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964235"
---
# <a name="ttm_setdelaytime-message"></a><span data-ttu-id="5fb9e-104">\_Messaggio TTM SETDELAYTIME</span><span class="sxs-lookup"><span data-stu-id="5fb9e-104">TTM\_SETDELAYTIME message</span></span>

<span data-ttu-id="5fb9e-105">Imposta le durate iniziali, popup e reshow per un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-105">Sets the initial, pop-up, and reshow durations for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5fb9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fb9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fb9e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5fb9e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fb9e-108">Flag che specifica il valore di ora da impostare.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-108">Flag that specifies which time value to set.</span></span> <span data-ttu-id="5fb9e-109">Questo parametro può essere uno dei valori seguenti</span><span class="sxs-lookup"><span data-stu-id="5fb9e-109">This parameter can be one of the following values</span></span>



| <span data-ttu-id="5fb9e-110">Valore</span><span class="sxs-lookup"><span data-stu-id="5fb9e-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="5fb9e-111">Significato</span><span class="sxs-lookup"><span data-stu-id="5fb9e-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="5fb9e-112"><dt>**\_AUTOPOP TTDT**</dt></span><span class="sxs-lookup"><span data-stu-id="5fb9e-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl>       | <span data-ttu-id="5fb9e-113">Imposta la quantità di tempo in cui una finestra della descrizione comando rimane visibile se il puntatore è fermo all'interno del rettangolo di delimitazione di uno strumento.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-113">Set the amount of time a tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span> <span data-ttu-id="5fb9e-114">Per restituire il valore predefinito di autopop delay, impostare *lParam* su-1.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-114">To return the autopop delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                         |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="5fb9e-115"><dt>**TTDT \_ iniziale**</dt></span><span class="sxs-lookup"><span data-stu-id="5fb9e-115"><dt>**TTDT\_INITIAL**</dt></span></span> </dl>       | <span data-ttu-id="5fb9e-116">Imposta la quantità di tempo in cui un puntatore deve rimanere fermo nel rettangolo di delimitazione di uno strumento prima che venga visualizzata la finestra della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-116">Set the amount of time a pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span> <span data-ttu-id="5fb9e-117">Per restituire il valore predefinito dell'intervallo di ritardo iniziale, impostare *lParam* su-1.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-117">To return the initial delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                    |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="5fb9e-118"><dt>**TTDT \_ RImostra**</dt></span><span class="sxs-lookup"><span data-stu-id="5fb9e-118"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>          | <span data-ttu-id="5fb9e-119">Consente di impostare la quantità di tempo necessaria per la visualizzazione delle finestre di descrizione comando successive quando il puntatore passa da uno strumento all'altro.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-119">Set the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span> <span data-ttu-id="5fb9e-120">Per restituire il tempo di ritardo della rivisualizzazione al valore predefinito, impostare *lParam* su-1.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-120">To return the reshow delay time to its default value, set *lParam* to -1.</span></span><br/>                                                                                                                                                           |
| <span id="TTDT_AUTOMATIC"></span><span id="ttdt_automatic"></span><dl> <span data-ttu-id="5fb9e-121"><dt>**TTDT \_ automatico**</dt></span><span class="sxs-lookup"><span data-stu-id="5fb9e-121"><dt>**TTDT\_AUTOMATIC**</dt></span></span> </dl> | <span data-ttu-id="5fb9e-122">Impostare tutte e tre le ore di ritardo sulle proporzioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-122">Set all three delay times to default proportions.</span></span> <span data-ttu-id="5fb9e-123">Il tempo di autopop sarà dieci volte l'ora iniziale e il tempo di ripresentazione sarà un quinto del tempo iniziale.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-123">The autopop time will be ten times the initial time and the reshow time will be one fifth the initial time.</span></span> <span data-ttu-id="5fb9e-124">Se questo flag è impostato, utilizzare un valore positivo di *lParam* per specificare il tempo iniziale, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-124">If this flag is set, use a positive value of *lParam* to specify the initial time, in milliseconds.</span></span> <span data-ttu-id="5fb9e-125">Impostare *lParam* su un valore negativo per restituire i valori predefiniti per tutti e tre i tempi di ritardo.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-125">Set *lParam* to a negative value to return all three delay times to their default values.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5fb9e-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5fb9e-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fb9e-127">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il tempo di ritardo, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the delay time, in milliseconds.</span></span> <span data-ttu-id="5fb9e-128">Il valore di [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-128">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fb9e-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fb9e-129">Return value</span></span>

<span data-ttu-id="5fb9e-130">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-130">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fb9e-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="5fb9e-131">Remarks</span></span>

<span data-ttu-id="5fb9e-132">Le ore di ritardo predefinite sono basate sull'ora di doppio clic.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-132">The default delay times are based on the double-click time.</span></span> <span data-ttu-id="5fb9e-133">Per l'ora di doppio clic predefinita di 500 ms, i tempi di ritardo iniziale, autopop e rimostrati sono rispettivamente 500 ms, 5000 ms e 100 ms.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-133">For the default double-click time of 500 ms, the initial, autopop, and reshow delay times are 500ms, 5000ms, and 100ms respectively.</span></span> <span data-ttu-id="5fb9e-134">Il frammento di codice seguente usa la funzione [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) per determinare le tre ore di ritardo per qualsiasi sistema.</span><span class="sxs-lookup"><span data-stu-id="5fb9e-134">The following code fragment uses the [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime) function to determine the three delay times for any system.</span></span>


```
initial = GetDoubleClickTime();

autopop = GetDoubleClickTime() * 10;

reshow = GetDoubleClickTime() / 5;
```



## <a name="requirements"></a><span data-ttu-id="5fb9e-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fb9e-135">Requirements</span></span>



| <span data-ttu-id="5fb9e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fb9e-136">Requirement</span></span> | <span data-ttu-id="5fb9e-137">Valore</span><span class="sxs-lookup"><span data-stu-id="5fb9e-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb9e-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fb9e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5fb9e-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5fb9e-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5fb9e-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fb9e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5fb9e-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5fb9e-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5fb9e-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fb9e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fb9e-143"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fb9e-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fb9e-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fb9e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fb9e-145">**\_GETDELAYTIME TTM**</span><span class="sxs-lookup"><span data-stu-id="5fb9e-145">**TTM\_GETDELAYTIME**</span></span>](ttm-getdelaytime.md)
</dt> </dl>

 

