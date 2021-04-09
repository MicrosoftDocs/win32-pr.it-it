---
title: Messaggio MCM_GETCOLOR (COMmctrl. h)
description: Recupera il colore per una determinata parte di un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal GetColor.
ms.assetid: 6c30ad0d-7584-402a-9c27-3c12c49c87f3
keywords:
- Controlli di Windows Message MCM_GETCOLOR
topic_type:
- apiref
api_name:
- MCM_GETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932b457bd1ddd870fd84facdb540e31188825504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120955"
---
# <a name="mcm_getcolor-message"></a><span data-ttu-id="8638f-105">\_Messaggio MCM GETcolor</span><span class="sxs-lookup"><span data-stu-id="8638f-105">MCM\_GETCOLOR message</span></span>

<span data-ttu-id="8638f-106">Recupera il colore per una determinata parte di un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="8638f-106">Retrieves the color for a given portion of a month calendar control.</span></span> <span data-ttu-id="8638f-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**MonthCal \_ GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) .</span><span class="sxs-lookup"><span data-stu-id="8638f-107">You can send this message explicitly or by using the [**MonthCal\_GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8638f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8638f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8638f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8638f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8638f-110">Valore di tipo **int** che specifica il colore del calendario del mese da recuperare.</span><span class="sxs-lookup"><span data-stu-id="8638f-110">Value of type **int** specifying which month calendar color to retrieve.</span></span> <span data-ttu-id="8638f-111">I valori validi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8638f-111">This value can be one of the following:</span></span>



| <span data-ttu-id="8638f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="8638f-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="8638f-113">Significato</span><span class="sxs-lookup"><span data-stu-id="8638f-113">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="8638f-114"><dt>**\_sfondo MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="8638f-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="8638f-115">Recupera il colore di sfondo visualizzato tra i mesi.</span><span class="sxs-lookup"><span data-stu-id="8638f-115">Retrieve the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="8638f-116"><dt>**\_MONTHBK MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="8638f-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="8638f-117">Recupera il colore di sfondo visualizzato nel mese.</span><span class="sxs-lookup"><span data-stu-id="8638f-117">Retrieve the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="8638f-118"><dt>**\_testo MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="8638f-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="8638f-119">Recupera il colore utilizzato per visualizzare il testo nel corso di un mese.</span><span class="sxs-lookup"><span data-stu-id="8638f-119">Retrieve the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="8638f-120"><dt>**\_TITLEBK MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="8638f-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="8638f-121">Recupera il colore di sfondo visualizzato nel titolo del calendario.</span><span class="sxs-lookup"><span data-stu-id="8638f-121">Retrieve the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="8638f-122"><dt>**\_TITLETEXT MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="8638f-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="8638f-123">Recupera il colore utilizzato per visualizzare il testo all'interno del titolo del calendario.</span><span class="sxs-lookup"><span data-stu-id="8638f-123">Retrieve the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="8638f-124"><dt>**\_TRAILINGTEXT MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="8638f-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="8638f-125">Recupera il colore utilizzato per visualizzare il testo dell'intestazione e del giorno finale.</span><span class="sxs-lookup"><span data-stu-id="8638f-125">Retrieve the color used to display header day and trailing day text.</span></span> <span data-ttu-id="8638f-126">Le intestazioni e i giorni finali sono i giorni dei mesi precedenti e successivi visualizzati nel calendario del mese corrente.</span><span class="sxs-lookup"><span data-stu-id="8638f-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8638f-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8638f-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8638f-128">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8638f-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8638f-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8638f-129">Return value</span></span>

<span data-ttu-id="8638f-130">Restituisce un valore **COLORREF** che rappresenta l'impostazione del colore per la parte specificata del controllo calendario mensile, se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8638f-130">Returns a **COLORREF** value that represents the color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="8638f-131">In caso contrario, il messaggio restituisce-1.</span><span class="sxs-lookup"><span data-stu-id="8638f-131">Otherwise, this message returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="8638f-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8638f-132">Requirements</span></span>



| <span data-ttu-id="8638f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8638f-133">Requirement</span></span> | <span data-ttu-id="8638f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="8638f-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8638f-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8638f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8638f-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8638f-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8638f-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8638f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8638f-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8638f-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8638f-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8638f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="8638f-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8638f-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





