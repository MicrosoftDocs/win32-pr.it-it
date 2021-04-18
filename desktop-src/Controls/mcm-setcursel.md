---
title: Messaggio MCM_SETCURSEL (COMmctrl. h)
description: Imposta la data attualmente selezionata per un controllo di calendario mensile. Se la data specificata non è visualizzata, il controllo Aggiorna la visualizzazione per visualizzarla. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- Controlli di Windows Message MCM_SETCURSEL
topic_type:
- apiref
api_name:
- MCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cceff48fbc4ffdb7446277d506c369e1bd89c92b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302521"
---
# <a name="mcm_setcursel-message"></a><span data-ttu-id="5c1b8-106">Messaggio in MCM \_</span><span class="sxs-lookup"><span data-stu-id="5c1b8-106">MCM\_SETCURSEL message</span></span>

<span data-ttu-id="5c1b8-107">Imposta la data attualmente selezionata per un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-107">Sets the currently selected date for a month calendar control.</span></span> <span data-ttu-id="5c1b8-108">Se la data specificata non è visualizzata, il controllo Aggiorna la visualizzazione per visualizzarla.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-108">If the specified date is not in view, the control updates the display to bring it into view.</span></span> <span data-ttu-id="5c1b8-109">È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro MonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="5c1b8-109">You can send this message explicitly or by using the [**MonthCal\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c1b8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c1b8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c1b8-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c1b8-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5c1b8-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5c1b8-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c1b8-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c1b8-114">Puntatore a una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che contiene la data da impostare come selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-114">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the current selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c1b8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c1b8-115">Return value</span></span>

<span data-ttu-id="5c1b8-116">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="5c1b8-117">Questo messaggio avrà esito negativo se applicato a un controllo calendario mensile che usa lo stile [**\_ MultiSelect MCS**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5c1b8-117">This message will fail if applied to a month calendar control that uses the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c1b8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c1b8-118">Requirements</span></span>



| <span data-ttu-id="5c1b8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c1b8-119">Requirement</span></span> | <span data-ttu-id="5c1b8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5c1b8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c1b8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c1b8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5c1b8-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c1b8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c1b8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c1b8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5c1b8-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5c1b8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c1b8-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c1b8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c1b8-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c1b8-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c1b8-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c1b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c1b8-128">Orari del controllo calendario mensile</span><span class="sxs-lookup"><span data-stu-id="5c1b8-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

