---
title: Messaggio MCM_GETCURSEL (COMmctrl. h)
description: Recupera la data attualmente selezionata. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal GetCurSel.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- Controlli di Windows Message MCM_GETCURSEL
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dece95c65e900119c7043c0d5eda22bf473e6c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477555"
---
# <a name="mcm_getcursel-message"></a><span data-ttu-id="46b2b-105">Messaggio di MCM \_ GETcursel</span><span class="sxs-lookup"><span data-stu-id="46b2b-105">MCM\_GETCURSEL message</span></span>

<span data-ttu-id="46b2b-106">Recupera la data attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="46b2b-106">Retrieves the currently selected date.</span></span> <span data-ttu-id="46b2b-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**MonthCal \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="46b2b-107">You can send this message explicitly or by using the [**MonthCal\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="46b2b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="46b2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46b2b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46b2b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="46b2b-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="46b2b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="46b2b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46b2b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46b2b-112">Puntatore a una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceverà le informazioni sulla data attualmente selezionate.</span><span class="sxs-lookup"><span data-stu-id="46b2b-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the currently selected date information.</span></span> <span data-ttu-id="46b2b-113">Questo parametro deve essere un indirizzo valido e non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="46b2b-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46b2b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46b2b-114">Return value</span></span>

<span data-ttu-id="46b2b-115">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="46b2b-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="46b2b-116">Questo messaggio avrà sempre esito negativo quando applicato ai controlli calendario mensile impostati sullo stile [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="46b2b-116">This message will always fail when applied to month calendar controls set to the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="46b2b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46b2b-117">Requirements</span></span>



| <span data-ttu-id="46b2b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="46b2b-118">Requirement</span></span> | <span data-ttu-id="46b2b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="46b2b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46b2b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46b2b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="46b2b-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46b2b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46b2b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46b2b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="46b2b-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="46b2b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46b2b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46b2b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="46b2b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46b2b-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46b2b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46b2b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46b2b-127">Orari del controllo calendario mensile</span><span class="sxs-lookup"><span data-stu-id="46b2b-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

