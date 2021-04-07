---
title: Messaggio MCM_GETSELRANGE (COMmctrl. h)
description: Recupera le informazioni sulla data che rappresentano i limiti superiore e inferiore dell'intervallo di date attualmente selezionato dall'utente. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetSelRange.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- Controlli di Windows Message MCM_GETSELRANGE
topic_type:
- apiref
api_name:
- MCM_GETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0d2f922b013a3eab525228bda4f5b99f33e70d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964043"
---
# <a name="mcm_getselrange-message"></a><span data-ttu-id="9ac51-105">\_Messaggio GETSELRANGE MCM</span><span class="sxs-lookup"><span data-stu-id="9ac51-105">MCM\_GETSELRANGE message</span></span>

<span data-ttu-id="9ac51-106">Recupera le informazioni sulla data che rappresentano i limiti superiore e inferiore dell'intervallo di date attualmente selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9ac51-106">Retrieves date information that represents the upper and lower limits of the date range currently selected by the user.</span></span> <span data-ttu-id="9ac51-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) .</span><span class="sxs-lookup"><span data-stu-id="9ac51-107">You can send this message explicitly or by using the [**MonthCal\_GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ac51-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ac51-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ac51-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ac51-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9ac51-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9ac51-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9ac51-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ac51-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ac51-112">Puntatore a una matrice a due elementi di strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceverà i limiti inferiore e superiore della selezione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9ac51-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the user's selection.</span></span> <span data-ttu-id="9ac51-113">I limiti inferiore e superiore vengono inseriti rispettivamente in *lprgSysTimeArray* \[ 0 \] e *lprgSysTimeArray* \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="9ac51-113">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="9ac51-114">Questo parametro deve essere un indirizzo valido e non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="9ac51-114">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ac51-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ac51-115">Return value</span></span>

<span data-ttu-id="9ac51-116">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9ac51-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="9ac51-117">**MCM \_ GETSELRANGE** avrà esito negativo se applicato a un controllo calendario mensile che non usa lo stile [**\_ MultiSelect MCS**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9ac51-117">**MCM\_GETSELRANGE** will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ac51-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ac51-118">Requirements</span></span>



| <span data-ttu-id="9ac51-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ac51-119">Requirement</span></span> | <span data-ttu-id="9ac51-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9ac51-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac51-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ac51-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9ac51-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ac51-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ac51-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ac51-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9ac51-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ac51-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ac51-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ac51-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ac51-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ac51-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ac51-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ac51-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ac51-128">Orari del controllo calendario mensile</span><span class="sxs-lookup"><span data-stu-id="9ac51-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

