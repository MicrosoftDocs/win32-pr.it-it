---
title: Messaggio MCM_SETCOLOR (COMmctrl. h)
description: Imposta il colore per una determinata parte di un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal Secolor.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- Controlli di Windows Message MCM_SETCOLOR
topic_type:
- apiref
api_name:
- MCM_SETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476aafd8356359cf6b4313f4b945253af6b493c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121310"
---
# <a name="mcm_setcolor-message"></a><span data-ttu-id="49031-105">\_Messaggio di SECOLORI MCM</span><span class="sxs-lookup"><span data-stu-id="49031-105">MCM\_SETCOLOR message</span></span>

<span data-ttu-id="49031-106">Imposta il colore per una determinata parte di un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="49031-106">Sets the color for a given portion of a month calendar control.</span></span> <span data-ttu-id="49031-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ Secolor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) .</span><span class="sxs-lookup"><span data-stu-id="49031-107">You can send this message explicitly or by using the [**MonthCal\_SetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="49031-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="49031-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49031-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49031-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49031-110">Valore di tipo **int** che specifica il colore del calendario mensile da impostare.</span><span class="sxs-lookup"><span data-stu-id="49031-110">Value of type **int** specifying which month calendar color to set.</span></span> <span data-ttu-id="49031-111">I valori validi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="49031-111">This value can be one of the following:</span></span>



| <span data-ttu-id="49031-112">Valore</span><span class="sxs-lookup"><span data-stu-id="49031-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="49031-113">Significato</span><span class="sxs-lookup"><span data-stu-id="49031-113">Meaning</span></span>                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="49031-114"><dt>**\_sfondo MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="49031-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="49031-115">Imposta il colore di sfondo visualizzato tra i mesi.</span><span class="sxs-lookup"><span data-stu-id="49031-115">Set the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="49031-116"><dt>**\_MONTHBK MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="49031-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="49031-117">Imposta il colore di sfondo visualizzato nel mese.</span><span class="sxs-lookup"><span data-stu-id="49031-117">Set the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="49031-118"><dt>**\_testo MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="49031-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="49031-119">Imposta il colore utilizzato per visualizzare il testo all'interno di un mese.</span><span class="sxs-lookup"><span data-stu-id="49031-119">Set the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="49031-120"><dt>**\_TITLEBK MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="49031-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="49031-121">Imposta il colore di sfondo visualizzato nel titolo del calendario.</span><span class="sxs-lookup"><span data-stu-id="49031-121">Set the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="49031-122"><dt>**\_TITLETEXT MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="49031-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="49031-123">Consente di impostare il colore utilizzato per visualizzare il testo all'interno del titolo del calendario.</span><span class="sxs-lookup"><span data-stu-id="49031-123">Set the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="49031-124"><dt>**\_TRAILINGTEXT MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="49031-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="49031-125">Imposta il colore utilizzato per visualizzare il testo dell'intestazione e il giorno finale.</span><span class="sxs-lookup"><span data-stu-id="49031-125">Set the color used to display header day and trailing day text.</span></span> <span data-ttu-id="49031-126">Le intestazioni e i giorni finali sono i giorni dei mesi precedenti e successivi visualizzati nel calendario del mese corrente.</span><span class="sxs-lookup"><span data-stu-id="49031-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="49031-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49031-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49031-128">Valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta il colore che verrà impostato per l'area specificata del calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="49031-128">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the color that will be set for the specified area of the month calendar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49031-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49031-129">Return value</span></span>

<span data-ttu-id="49031-130">Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che rappresenta l'impostazione del colore precedente per la parte specificata del controllo calendario mensile, se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="49031-130">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="49031-131">In caso contrario, il risultato restituito è-1.</span><span class="sxs-lookup"><span data-stu-id="49031-131">Otherwise, the return is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="49031-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="49031-132">Remarks</span></span>

<span data-ttu-id="49031-133">Se gli stili di visualizzazione sono attivi, questo messaggio non ha alcun effetto tranne quando *wParam* è MCSC \_ sfondo.</span><span class="sxs-lookup"><span data-stu-id="49031-133">If visual styles are active, this message has no effect except when *wParam* is MCSC\_BACKGROUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="49031-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49031-134">Requirements</span></span>



| <span data-ttu-id="49031-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="49031-135">Requirement</span></span> | <span data-ttu-id="49031-136">Valore</span><span class="sxs-lookup"><span data-stu-id="49031-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49031-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49031-137">Minimum supported client</span></span><br/> | <span data-ttu-id="49031-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49031-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49031-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49031-139">Minimum supported server</span></span><br/> | <span data-ttu-id="49031-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49031-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49031-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49031-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="49031-142"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49031-142"><dt>Commctrl.h</dt></span></span> </dl> |



 

