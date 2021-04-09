---
title: Messaggio DTM_GETMONTHCAL (COMmctrl. h)
description: Ottiene l'handle per un controllo calendario mensile figlio (DTP) di selezione data e ora. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime GetMonthCal.
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- Controlli di Windows Message DTM_GETMONTHCAL
topic_type:
- apiref
api_name:
- DTM_GETMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99609ed3a437990889066da9a3424ef147c3d6b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964583"
---
# <a name="dtm_getmonthcal-message"></a><span data-ttu-id="959d6-105">\_Messaggio GETMONTHCAL DTM</span><span class="sxs-lookup"><span data-stu-id="959d6-105">DTM\_GETMONTHCAL message</span></span>

<span data-ttu-id="959d6-106">Ottiene l'handle per un controllo calendario mensile figlio (DTP) di selezione data e ora.</span><span class="sxs-lookup"><span data-stu-id="959d6-106">Gets the handle to a date and time picker's (DTP) child month calendar control.</span></span> <span data-ttu-id="959d6-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) .</span><span class="sxs-lookup"><span data-stu-id="959d6-107">You can send this message explicitly or use the [**DateTime\_GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="959d6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="959d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="959d6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="959d6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="959d6-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="959d6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="959d6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="959d6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="959d6-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="959d6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="959d6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="959d6-113">Return value</span></span>

<span data-ttu-id="959d6-114">Restituisce l'handle a un controllo calendario mensile figlio di un controllo DTP, se ha esito positivo, oppure **null** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="959d6-114">Returns the handle to a DTP control's child month calendar control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="959d6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="959d6-115">Remarks</span></span>

<span data-ttu-id="959d6-116">I controlli DTP creano un controllo calendario mensile figlio quando l'utente fa clic sulla freccia a discesa (notifica a[ \_ discesa DTN](dtn-dropdown.md) ).</span><span class="sxs-lookup"><span data-stu-id="959d6-116">DTP controls create a child month calendar control when the user clicks the drop-down arrow ([DTN\_DROPDOWN](dtn-dropdown.md) notification).</span></span> <span data-ttu-id="959d6-117">Quando il calendario mensile non è più necessario, viene eliminato definitivamente, ovvero viene inviata una notifica di [ \_ primo piano DTN](dtn-closeup.md) per la distruzione.</span><span class="sxs-lookup"><span data-stu-id="959d6-117">When the month calendar is no longer needed, it is destroyed (a [DTN\_CLOSEUP](dtn-closeup.md) notification is sent on destruction).</span></span> <span data-ttu-id="959d6-118">Quindi, l'applicazione non deve basarsi su un handle statico per il calendario mensile figlio del controllo DTP.</span><span class="sxs-lookup"><span data-stu-id="959d6-118">So your application must not rely on a static handle to the DTP control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="959d6-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="959d6-119">Requirements</span></span>



| <span data-ttu-id="959d6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="959d6-120">Requirement</span></span> | <span data-ttu-id="959d6-121">Valore</span><span class="sxs-lookup"><span data-stu-id="959d6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="959d6-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="959d6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="959d6-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="959d6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="959d6-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="959d6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="959d6-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="959d6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="959d6-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="959d6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="959d6-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="959d6-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="959d6-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="959d6-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="959d6-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="959d6-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="959d6-130">primo piano DTN \_</span><span class="sxs-lookup"><span data-stu-id="959d6-130">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="959d6-131">\_elenco a discesa DTN</span><span class="sxs-lookup"><span data-stu-id="959d6-131">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> </dl>

 

 





