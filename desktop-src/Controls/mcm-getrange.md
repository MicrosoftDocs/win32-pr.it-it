---
title: Messaggio MCM_GETRANGE (COMmctrl. h)
description: Recupera le date minime e massime consentite impostate per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal GetRange.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- Controlli di Windows Message MCM_GETRANGE
topic_type:
- apiref
api_name:
- MCM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c757c046b88479072eb0771ecbf3f7fb79cdb31b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874514"
---
# <a name="mcm_getrange-message"></a><span data-ttu-id="d44fd-105">\_Messaggio MCM GETrange</span><span class="sxs-lookup"><span data-stu-id="d44fd-105">MCM\_GETRANGE message</span></span>

<span data-ttu-id="d44fd-106">Recupera le date minime e massime consentite impostate per un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="d44fd-106">Retrieves the minimum and maximum allowable dates set for a month calendar control.</span></span> <span data-ttu-id="d44fd-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**MonthCal \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) .</span><span class="sxs-lookup"><span data-stu-id="d44fd-107">You can send this message explicitly or by using the [**MonthCal\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d44fd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d44fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d44fd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d44fd-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d44fd-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d44fd-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d44fd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d44fd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d44fd-112">Puntatore a una matrice a due elementi di strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceveranno le informazioni sui limiti di data.</span><span class="sxs-lookup"><span data-stu-id="d44fd-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the date limit information.</span></span> <span data-ttu-id="d44fd-113">Il limite minimo è impostato in *lprgSysTimeArray* \[ 0 \] e *lprgSysTimeArray* \[ 1 \] riceve il limite massimo.</span><span class="sxs-lookup"><span data-stu-id="d44fd-113">The minimum limit is set in *lprgSysTimeArray*\[0\], and *lprgSysTimeArray*\[1\] receives the maximum limit.</span></span> <span data-ttu-id="d44fd-114">Se uno dei due elementi viene impostato su tutti zeri, non viene impostato alcun limite corrispondente per il controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="d44fd-114">If either element is set to all zeros, then no corresponding limit is set for the month calendar control.</span></span> <span data-ttu-id="d44fd-115">Questo parametro deve essere un indirizzo valido e non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="d44fd-115">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d44fd-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d44fd-116">Return value</span></span>

<span data-ttu-id="d44fd-117">Restituisce un **valore DWORD** che può essere zero (nessun limite impostato) o una combinazione dei valori seguenti che specificano le informazioni sui limiti:</span><span class="sxs-lookup"><span data-stu-id="d44fd-117">Returns a **DWORD** that can be zero (no limits are set) or a combination of the following values that specify limit information:</span></span>



| <span data-ttu-id="d44fd-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d44fd-118">Return code</span></span>                                                                              | <span data-ttu-id="d44fd-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d44fd-119">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d44fd-120"><dt>**GDTR \_ Max**</dt></span><span class="sxs-lookup"><span data-stu-id="d44fd-120"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="d44fd-121">Per il controllo è impostato un limite massimo. *lprgSysTimeArray* \[ 0 \] è valido e contiene le informazioni sulla data applicabili.</span><span class="sxs-lookup"><span data-stu-id="d44fd-121">A maximum limit is set for the control; *lprgSysTimeArray*\[0\] is valid and contains the applicable date information.</span></span> <br/> |
| <dl> <span data-ttu-id="d44fd-122"><dt>**GDTR \_ min**</dt></span><span class="sxs-lookup"><span data-stu-id="d44fd-122"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="d44fd-123">È stato impostato un limite minimo per il controllo; *lprgSysTimeArray* \[ 1 \] è valido e contiene le informazioni sulla data applicabili.</span><span class="sxs-lookup"><span data-stu-id="d44fd-123">A minimum limit is set for the control; *lprgSysTimeArray*\[1\] is valid and contains the applicable date information.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="d44fd-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d44fd-124">Requirements</span></span>



| <span data-ttu-id="d44fd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d44fd-125">Requirement</span></span> | <span data-ttu-id="d44fd-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d44fd-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d44fd-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d44fd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d44fd-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d44fd-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d44fd-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d44fd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d44fd-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d44fd-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d44fd-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d44fd-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d44fd-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d44fd-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d44fd-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d44fd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d44fd-134">Orari del controllo calendario mensile</span><span class="sxs-lookup"><span data-stu-id="d44fd-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

