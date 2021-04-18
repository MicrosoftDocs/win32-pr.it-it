---
title: Messaggio MCM_SETRANGE (COMmctrl. h)
description: Imposta le date minime e massime consentite per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetRange MonthCal.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- Controlli di Windows Message MCM_SETRANGE
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380e599da8cd4a054c02135bc64f57f29d2c81d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302281"
---
# <a name="mcm_setrange-message"></a><span data-ttu-id="21e9f-105">\_Messaggio di SEtrange MCM</span><span class="sxs-lookup"><span data-stu-id="21e9f-105">MCM\_SETRANGE message</span></span>

<span data-ttu-id="21e9f-106">Imposta le date minime e massime consentite per un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="21e9f-106">Sets the minimum and maximum allowable dates for a month calendar control.</span></span> <span data-ttu-id="21e9f-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetRange MonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) .</span><span class="sxs-lookup"><span data-stu-id="21e9f-107">You can send this message explicitly or by using the [**MonthCal\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="21e9f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="21e9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21e9f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="21e9f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21e9f-110">Flag che specificano i limiti di data da impostare.</span><span class="sxs-lookup"><span data-stu-id="21e9f-110">Flag values that specify which date limits are being set.</span></span> <span data-ttu-id="21e9f-111">Questo valore deve essere uno o entrambi gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="21e9f-111">This value must be one or both of the following:</span></span>



| <span data-ttu-id="21e9f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="21e9f-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="21e9f-113">Significato</span><span class="sxs-lookup"><span data-stu-id="21e9f-113">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="21e9f-114"><dt>**GDTR \_ Max**</dt></span><span class="sxs-lookup"><span data-stu-id="21e9f-114"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="21e9f-115">È in corso l'impostazione della data massima consentita.</span><span class="sxs-lookup"><span data-stu-id="21e9f-115">The maximum allowable date is being set.</span></span> <span data-ttu-id="21e9f-116">La struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in *lpSysTimeArray* \[ 1 \] deve contenere informazioni sulla data.</span><span class="sxs-lookup"><span data-stu-id="21e9f-116">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[1\] must contain date information.</span></span> <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="21e9f-117"><dt>**GDTR \_ min**</dt></span><span class="sxs-lookup"><span data-stu-id="21e9f-117"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="21e9f-118">È in corso l'impostazione della data minima consentita.</span><span class="sxs-lookup"><span data-stu-id="21e9f-118">The minimum allowable date is being set.</span></span> <span data-ttu-id="21e9f-119">La struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in *lpSysTimeArray* \[ 0 \] deve contenere informazioni sulla data.</span><span class="sxs-lookup"><span data-stu-id="21e9f-119">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[0\] must contain date information.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="21e9f-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21e9f-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21e9f-121">Puntatore a una matrice a due elementi di strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che contengono i limiti di data.</span><span class="sxs-lookup"><span data-stu-id="21e9f-121">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain the date limits.</span></span> <span data-ttu-id="21e9f-122">Il limite massimo deve trovarsi in *lpSysTimeArray* \[ 1 \] se \_ si specifica GDTR Max e *lpSysTimeArray* \[ 0 \] deve contenere il limite minimo se \_ viene specificato GDTR min.</span><span class="sxs-lookup"><span data-stu-id="21e9f-122">The maximum limit must be in *lpSysTimeArray*\[1\] if GDTR\_MAX is specified, and *lpSysTimeArray*\[0\] must contain the minimum limit if GDTR\_MIN is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21e9f-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21e9f-123">Return value</span></span>

<span data-ttu-id="21e9f-124">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="21e9f-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="21e9f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21e9f-125">Requirements</span></span>



| <span data-ttu-id="21e9f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="21e9f-126">Requirement</span></span> | <span data-ttu-id="21e9f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="21e9f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21e9f-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21e9f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="21e9f-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="21e9f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21e9f-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21e9f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="21e9f-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="21e9f-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21e9f-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21e9f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="21e9f-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="21e9f-133"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21e9f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21e9f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21e9f-135">Orari del controllo calendario mensile</span><span class="sxs-lookup"><span data-stu-id="21e9f-135">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

