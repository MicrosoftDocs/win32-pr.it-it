---
title: Messaggio MCM_SETTODAY (COMmctrl. h)
description: Imposta il \ 0034; Today \ 0034; selezione per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal.
ms.assetid: fcd4d33d-e661-4e02-8d19-666d80e1a070
keywords:
- Controlli di Windows Message MCM_SETTODAY
topic_type:
- apiref
api_name:
- MCM_SETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b725e5f61e3c08170a323b063616434acb857e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743815"
---
# <a name="mcm_settoday-message"></a><span data-ttu-id="ea175-105">Messaggio di data/ \_ ora MCM</span><span class="sxs-lookup"><span data-stu-id="ea175-105">MCM\_SETTODAY message</span></span>

<span data-ttu-id="ea175-106">Imposta la selezione "Today" per un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="ea175-106">Sets the "today" selection for a month calendar control.</span></span> <span data-ttu-id="ea175-107">È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro MonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) .</span><span class="sxs-lookup"><span data-stu-id="ea175-107">You can send this message explicitly or by using the [**MonthCal\_SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea175-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea175-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea175-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea175-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ea175-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ea175-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ea175-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea175-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea175-112">Puntatore a una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che contiene la data da impostare come selezione "Today" per il controllo.</span><span class="sxs-lookup"><span data-stu-id="ea175-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the "today" selection for the control.</span></span> <span data-ttu-id="ea175-113">Se questo parametro è impostato su **null**, il controllo torna all'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ea175-113">If this parameter is set to **NULL**, the control returns to the default setting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea175-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea175-114">Return value</span></span>

<span data-ttu-id="ea175-115">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="ea175-115">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea175-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea175-116">Remarks</span></span>

<span data-ttu-id="ea175-117">Se la selezione "Today" è impostata su una data diversa da quella predefinita, si applicano le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea175-117">If the "today" selection is set to any date other than the default, the following conditions apply:</span></span>

-   <span data-ttu-id="ea175-118">Il controllo non aggiornerà automaticamente la selezione "Today" quando il tempo passa a mezzanotte del giorno corrente.</span><span class="sxs-lookup"><span data-stu-id="ea175-118">The control will not automatically update the "today" selection when the time passes midnight for the current day.</span></span>
-   <span data-ttu-id="ea175-119">Il controllo non aggiornerà automaticamente la visualizzazione in base alle modifiche delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="ea175-119">The control will not automatically update its display based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea175-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea175-120">Requirements</span></span>



| <span data-ttu-id="ea175-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea175-121">Requirement</span></span> | <span data-ttu-id="ea175-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ea175-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea175-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea175-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ea175-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea175-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea175-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea175-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ea175-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea175-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea175-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea175-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea175-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea175-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea175-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea175-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea175-130">Orari del controllo calendario mensile</span><span class="sxs-lookup"><span data-stu-id="ea175-130">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

