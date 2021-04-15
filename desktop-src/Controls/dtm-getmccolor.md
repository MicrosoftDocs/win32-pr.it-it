---
title: Messaggio DTM_GETMCCOLOR (COMmctrl. h)
description: Ottiene il colore per una porzione specificata del calendario mensile all'interno di un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime GetMonthCalColor.
ms.assetid: 892e8c23-f0d0-4fd6-98ed-39592c4d316f
keywords:
- Controlli di Windows Message DTM_GETMCCOLOR
topic_type:
- apiref
api_name:
- DTM_GETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690c461c5bccbd050fb3d698d1a41c6d1e513944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479464"
---
# <a name="dtm_getmccolor-message"></a><span data-ttu-id="e4b30-105">\_Messaggio GETMCCOLOR DTM</span><span class="sxs-lookup"><span data-stu-id="e4b30-105">DTM\_GETMCCOLOR message</span></span>

<span data-ttu-id="e4b30-106">Ottiene il colore per una porzione specificata del calendario mensile all'interno di un controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="e4b30-106">Gets the color for a given portion of the month calendar within a date and time picker (DTP) control.</span></span> <span data-ttu-id="e4b30-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) .</span><span class="sxs-lookup"><span data-stu-id="e4b30-107">You can send this message explicitly or use the [**DateTime\_GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4b30-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4b30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b30-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4b30-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4b30-110">Valore di tipo **int** che specifica il colore del calendario mensile da recuperare.</span><span class="sxs-lookup"><span data-stu-id="e4b30-110">A value of type **int** specifying which month calendar color to retrieve.</span></span> <span data-ttu-id="e4b30-111">I valori validi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e4b30-111">This value can be one of the following:</span></span>



| <span data-ttu-id="e4b30-112">Valore</span><span class="sxs-lookup"><span data-stu-id="e4b30-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="e4b30-113">Significato</span><span class="sxs-lookup"><span data-stu-id="e4b30-113">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="e4b30-114"><dt>**\_sfondo MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="e4b30-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="e4b30-115">Recupera il colore di sfondo visualizzato tra i mesi.</span><span class="sxs-lookup"><span data-stu-id="e4b30-115">Retrieve the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="e4b30-116"><dt>**\_MONTHBK MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="e4b30-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="e4b30-117">Recupera il colore di sfondo visualizzato nel mese.</span><span class="sxs-lookup"><span data-stu-id="e4b30-117">Retrieve the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="e4b30-118"><dt>**\_testo MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="e4b30-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="e4b30-119">Recupera il colore utilizzato per visualizzare il testo nel corso di un mese.</span><span class="sxs-lookup"><span data-stu-id="e4b30-119">Retrieve the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="e4b30-120"><dt>**\_TITLEBK MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="e4b30-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="e4b30-121">Recupera il colore di sfondo visualizzato nel titolo del calendario.</span><span class="sxs-lookup"><span data-stu-id="e4b30-121">Retrieve the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="e4b30-122"><dt>**\_TITLETEXT MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="e4b30-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="e4b30-123">Recupera il colore utilizzato per visualizzare il testo all'interno del titolo del calendario.</span><span class="sxs-lookup"><span data-stu-id="e4b30-123">Retrieve the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="e4b30-124"><dt>**\_TRAILINGTEXT MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="e4b30-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="e4b30-125">Recupera il colore utilizzato per visualizzare il testo dell'intestazione e del giorno finale.</span><span class="sxs-lookup"><span data-stu-id="e4b30-125">Retrieve the color used to display header day and trailing day text.</span></span> <span data-ttu-id="e4b30-126">Le intestazioni e i giorni finali sono i giorni dei mesi precedenti e successivi visualizzati nel calendario del mese corrente.</span><span class="sxs-lookup"><span data-stu-id="e4b30-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e4b30-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4b30-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e4b30-128">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e4b30-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b30-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4b30-129">Return value</span></span>

<span data-ttu-id="e4b30-130">Restituisce un valore **COLORREF** che rappresenta l'impostazione del colore per la parte specificata del controllo calendario mensile, se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e4b30-130">Returns a **COLORREF** value that represents the color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="e4b30-131">Il messaggio restituisce-1 in caso di esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e4b30-131">The message returns -1 if unsuccessful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b30-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4b30-132">Requirements</span></span>



| <span data-ttu-id="e4b30-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4b30-133">Requirement</span></span> | <span data-ttu-id="e4b30-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e4b30-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b30-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4b30-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b30-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4b30-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4b30-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4b30-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b30-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4b30-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4b30-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4b30-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b30-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b30-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





