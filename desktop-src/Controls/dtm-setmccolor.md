---
title: Messaggio DTM_SETMCCOLOR (COMmctrl. h)
description: Imposta il colore per una porzione specificata del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime SetMonthCalColor.
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- Controlli di Windows Message DTM_SETMCCOLOR
topic_type:
- apiref
api_name:
- DTM_SETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e496abb4dd28b040dd4a8035073ffa32a3f3847
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742562"
---
# <a name="dtm_setmccolor-message"></a><span data-ttu-id="4f585-105">\_Messaggio SETMCCOLOR DTM</span><span class="sxs-lookup"><span data-stu-id="4f585-105">DTM\_SETMCCOLOR message</span></span>

<span data-ttu-id="4f585-106">Imposta il colore per una porzione specificata del calendario mensile all'interno di un controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="4f585-106">Sets the color for a given portion of the month calendar within a date and time picker (DTP) control.</span></span> <span data-ttu-id="4f585-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) .</span><span class="sxs-lookup"><span data-stu-id="4f585-107">You can send this message explicitly or use the [**DateTime\_SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f585-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f585-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f585-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f585-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f585-110">Valore di tipo **int** che specifica il colore del calendario mensile da impostare.</span><span class="sxs-lookup"><span data-stu-id="4f585-110">A value of type **int** specifying which month calendar color to set.</span></span> <span data-ttu-id="4f585-111">I valori validi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4f585-111">This value can be one of the following:</span></span>



| <span data-ttu-id="4f585-112">Valore</span><span class="sxs-lookup"><span data-stu-id="4f585-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="4f585-113">Significato</span><span class="sxs-lookup"><span data-stu-id="4f585-113">Meaning</span></span>                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="4f585-114"><dt>**\_sfondo MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="4f585-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="4f585-115">Imposta il colore di sfondo visualizzato tra i mesi.</span><span class="sxs-lookup"><span data-stu-id="4f585-115">Set the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="4f585-116"><dt>**\_MONTHBK MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="4f585-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="4f585-117">Imposta il colore di sfondo visualizzato nel mese.</span><span class="sxs-lookup"><span data-stu-id="4f585-117">Set the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="4f585-118"><dt>**\_testo MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="4f585-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="4f585-119">Imposta il colore utilizzato per visualizzare il testo all'interno di un mese.</span><span class="sxs-lookup"><span data-stu-id="4f585-119">Set the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="4f585-120"><dt>**\_TITLEBK MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="4f585-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="4f585-121">Imposta il colore di sfondo visualizzato nel titolo del calendario.</span><span class="sxs-lookup"><span data-stu-id="4f585-121">Set the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="4f585-122"><dt>**\_TITLETEXT MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="4f585-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="4f585-123">Consente di impostare il colore utilizzato per visualizzare il testo all'interno del titolo del calendario.</span><span class="sxs-lookup"><span data-stu-id="4f585-123">Set the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="4f585-124"><dt>**\_TRAILINGTEXT MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="4f585-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="4f585-125">Imposta il colore utilizzato per visualizzare il testo dell'intestazione e il giorno finale.</span><span class="sxs-lookup"><span data-stu-id="4f585-125">Set the color used to display header day and trailing day text.</span></span> <span data-ttu-id="4f585-126">Le intestazioni e i giorni finali sono i giorni dei mesi precedenti e successivi visualizzati nel calendario del mese corrente.</span><span class="sxs-lookup"><span data-stu-id="4f585-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4f585-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f585-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f585-128">Valore **COLORREF** che rappresenta il colore che verrà impostato per l'area specificata del calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="4f585-128">A **COLORREF** value representing the color that will be set for the specified area of the month calendar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f585-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f585-129">Return value</span></span>

<span data-ttu-id="4f585-130">Restituisce un valore **COLORREF** che rappresenta l'impostazione del colore precedente per la parte specificata del controllo calendario mensile, se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4f585-130">Returns a **COLORREF** value that represents the previous color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="4f585-131">In caso contrario, il messaggio restituisce-1.</span><span class="sxs-lookup"><span data-stu-id="4f585-131">Otherwise, the message returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f585-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f585-132">Remarks</span></span>

<span data-ttu-id="4f585-133">Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto tranne quando *wParam* è MCSC \_ sfondo.</span><span class="sxs-lookup"><span data-stu-id="4f585-133">When visual styles are enabled, this message has no effect except when *wParam* is MCSC\_BACKGROUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f585-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f585-134">Requirements</span></span>



| <span data-ttu-id="4f585-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f585-135">Requirement</span></span> | <span data-ttu-id="4f585-136">Valore</span><span class="sxs-lookup"><span data-stu-id="4f585-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f585-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f585-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4f585-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4f585-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4f585-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f585-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4f585-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4f585-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f585-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f585-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f585-142"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f585-142"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





