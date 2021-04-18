---
title: Messaggio MCM_GETMONTHRANGE (COMmctrl. h)
description: Recupera le informazioni sulla data (usando le strutture SYSTEMTIME) che rappresentano i limiti massimo e minimo della visualizzazione di un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetMonthRange.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- Controlli di Windows Message MCM_GETMONTHRANGE
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022ca7e05cc0c69cd32f6ad92531420cdaed7c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302795"
---
# <a name="mcm_getmonthrange-message"></a><span data-ttu-id="58e13-105">\_Messaggio GETMONTHRANGE MCM</span><span class="sxs-lookup"><span data-stu-id="58e13-105">MCM\_GETMONTHRANGE message</span></span>

<span data-ttu-id="58e13-106">Recupera le informazioni sulla data (usando le strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) ) che rappresentano i limiti massimo e minimo della visualizzazione di un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="58e13-106">Retrieves date information (using [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures) that represents the high and low limits of a month calendar control's display.</span></span> <span data-ttu-id="58e13-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) .</span><span class="sxs-lookup"><span data-stu-id="58e13-107">You can send this message explicitly or by using the [**MonthCal\_GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="58e13-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="58e13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58e13-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="58e13-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58e13-110">Valore che specifica l'ambito dei limiti di intervallo da recuperare.</span><span class="sxs-lookup"><span data-stu-id="58e13-110">Value specifying the scope of the range limits to be retrieved.</span></span> <span data-ttu-id="58e13-111">Questo valore deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="58e13-111">This value must be one of the following:</span></span>



| <span data-ttu-id="58e13-112">Valore</span><span class="sxs-lookup"><span data-stu-id="58e13-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="58e13-113">Significato</span><span class="sxs-lookup"><span data-stu-id="58e13-113">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <span data-ttu-id="58e13-114"><dt>**\_DAYSTATE GMR**</dt></span><span class="sxs-lookup"><span data-stu-id="58e13-114"><dt>**GMR\_DAYSTATE**</dt></span></span> </dl> | <span data-ttu-id="58e13-115">Includere i mesi precedenti e finali dell'intervallo visibile che vengono visualizzati solo parzialmente.</span><span class="sxs-lookup"><span data-stu-id="58e13-115">Include preceding and trailing months of visible range that are only partially displayed.</span></span> <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <span data-ttu-id="58e13-116"><dt>**GMR \_ visibile**</dt></span><span class="sxs-lookup"><span data-stu-id="58e13-116"><dt>**GMR\_VISIBLE**</dt></span></span> </dl>    | <span data-ttu-id="58e13-117">Includere solo i mesi che vengono visualizzati interamente.</span><span class="sxs-lookup"><span data-stu-id="58e13-117">Include only those months that are entirely displayed.</span></span> <br/>                                    |



 

</dd> <dt>

<span data-ttu-id="58e13-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58e13-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58e13-119">Puntatore a una matrice a due elementi di strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceveranno i limiti inferiore e superiore dell'ambito specificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="58e13-119">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the scope specified by *wParam*.</span></span> <span data-ttu-id="58e13-120">I limiti inferiore e superiore vengono inseriti rispettivamente in *lprgSysTimeArray* \[ 0 \] e *lprgSysTimeArray* \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="58e13-120">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="58e13-121">Questo parametro deve essere un indirizzo valido e non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="58e13-121">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58e13-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58e13-122">Return value</span></span>

<span data-ttu-id="58e13-123">Restituisce un valore INT che rappresenta l'intervallo, in mesi, esteso dai due limiti restituiti in *lParam*.</span><span class="sxs-lookup"><span data-stu-id="58e13-123">Returns an INT value that represents the range, in months, spanned by the two limits returned at *lParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e13-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58e13-124">Requirements</span></span>



| <span data-ttu-id="58e13-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="58e13-125">Requirement</span></span> | <span data-ttu-id="58e13-126">Valore</span><span class="sxs-lookup"><span data-stu-id="58e13-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58e13-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58e13-127">Minimum supported client</span></span><br/> | <span data-ttu-id="58e13-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58e13-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="58e13-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58e13-129">Minimum supported server</span></span><br/> | <span data-ttu-id="58e13-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58e13-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58e13-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58e13-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="58e13-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="58e13-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e13-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58e13-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e13-134">Orari del controllo calendario mensile</span><span class="sxs-lookup"><span data-stu-id="58e13-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

