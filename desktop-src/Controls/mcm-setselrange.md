---
title: Messaggio MCM_SETSELRANGE (COMmctrl. h)
description: Imposta la selezione per un controllo di calendario mensile su un intervallo di date specificato. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal SetSelRange.
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- Controlli di Windows Message MCM_SETSELRANGE
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad28966ab67a5e7c0d27dd8fc9c367ec30e4cd7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047925"
---
# <a name="mcm_setselrange-message"></a><span data-ttu-id="be399-105">\_Messaggio SETSELRANGE MCM</span><span class="sxs-lookup"><span data-stu-id="be399-105">MCM\_SETSELRANGE message</span></span>

<span data-ttu-id="be399-106">Imposta la selezione per un controllo di calendario mensile su un intervallo di date specificato.</span><span class="sxs-lookup"><span data-stu-id="be399-106">Sets the selection for a month calendar control to a given date range.</span></span> <span data-ttu-id="be399-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) .</span><span class="sxs-lookup"><span data-stu-id="be399-107">You can send this message explicitly or by using the [**MonthCal\_SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="be399-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="be399-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be399-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be399-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="be399-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="be399-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="be399-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be399-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be399-112">Puntatore a una matrice a due elementi di strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che contengono informazioni sulla data che rappresentano i limiti di selezione.</span><span class="sxs-lookup"><span data-stu-id="be399-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain date information representing the selection limits.</span></span> <span data-ttu-id="be399-113">La prima data selezionata deve essere specificata in *lpSysTimeArray* \[ 0 \] e l'ultima data selezionata deve essere specificata in *lpSysTimeArray* \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="be399-113">The first selected date must be specified in *lpSysTimeArray*\[0\], and the last selected date must be specified in *lpSysTimeArray*\[1\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be399-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be399-114">Return value</span></span>

<span data-ttu-id="be399-115">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="be399-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="be399-116">Questo messaggio avrà esito negativo se applicato a un controllo calendario mensile che non usa lo stile [**\_ MultiSelect MCS**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="be399-116">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="be399-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be399-117">Requirements</span></span>



| <span data-ttu-id="be399-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="be399-118">Requirement</span></span> | <span data-ttu-id="be399-119">Valore</span><span class="sxs-lookup"><span data-stu-id="be399-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be399-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be399-120">Minimum supported client</span></span><br/> | <span data-ttu-id="be399-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be399-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be399-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="be399-122">Minimum supported server</span></span><br/> | <span data-ttu-id="be399-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be399-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be399-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be399-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="be399-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="be399-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be399-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be399-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be399-127">Orari del controllo calendario mensile</span><span class="sxs-lookup"><span data-stu-id="be399-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

