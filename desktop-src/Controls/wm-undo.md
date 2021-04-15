---
title: Messaggio WM_UNDO (winuser. h)
description: Un'applicazione invia un \_ messaggio di annullamento WM a un controllo di modifica per annullare l'ultima operazione. Quando questo messaggio viene inviato a un controllo di modifica, il testo eliminato in precedenza viene ripristinato o il testo aggiunto in precedenza viene eliminato.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- Controlli di Windows Message WM_UNDO
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c5eb9182b6d8d3fc1360565f6661e989f3b6d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477525"
---
# <a name="wm_undo-message"></a><span data-ttu-id="e9e40-105">\_Messaggio di annullamento WM</span><span class="sxs-lookup"><span data-stu-id="e9e40-105">WM\_UNDO message</span></span>

<span data-ttu-id="e9e40-106">Un'applicazione invia un messaggio di **\_ annullamento WM** a un controllo di modifica per annullare l'ultima operazione.</span><span class="sxs-lookup"><span data-stu-id="e9e40-106">An application sends a **WM\_UNDO** message to an edit control to undo the last operation.</span></span> <span data-ttu-id="e9e40-107">Quando questo messaggio viene inviato a un controllo di modifica, il testo eliminato in precedenza viene ripristinato o il testo aggiunto in precedenza viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="e9e40-107">When this message is sent to an edit control, the previously deleted text is restored or the previously added text is deleted.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9e40-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9e40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9e40-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9e40-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e40-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e9e40-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e9e40-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9e40-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e40-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e9e40-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9e40-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9e40-113">Return value</span></span>

<span data-ttu-id="e9e40-114">Se il messaggio ha esito positivo, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="e9e40-114">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="e9e40-115">Se il messaggio ha esito negativo, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="e9e40-115">If the message fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9e40-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9e40-116">Remarks</span></span>

<span data-ttu-id="e9e40-117">**Modifica avanzata:** È consigliabile usare l' [**\_ annullamento em**](em-undo.md) anziché **WM \_ Undo**.</span><span class="sxs-lookup"><span data-stu-id="e9e40-117">**Rich Edit:** It is recommended that [**EM\_UNDO**](em-undo.md) be used instead of **WM\_UNDO**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9e40-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9e40-118">Requirements</span></span>



| <span data-ttu-id="e9e40-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9e40-119">Requirement</span></span> | <span data-ttu-id="e9e40-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e9e40-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9e40-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9e40-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e9e40-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9e40-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e9e40-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9e40-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e9e40-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e9e40-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e9e40-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9e40-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9e40-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9e40-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9e40-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9e40-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9e40-128">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="e9e40-128">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e9e40-129">**chiaro di WM \_**</span><span class="sxs-lookup"><span data-stu-id="e9e40-129">**WM\_CLEAR**</span></span>](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[<span data-ttu-id="e9e40-130">**\_copia WM**</span><span class="sxs-lookup"><span data-stu-id="e9e40-130">**WM\_COPY**</span></span>](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[<span data-ttu-id="e9e40-131">**\_taglia WM**</span><span class="sxs-lookup"><span data-stu-id="e9e40-131">**WM\_CUT**</span></span>](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[<span data-ttu-id="e9e40-132">**\_Incolla WM**</span><span class="sxs-lookup"><span data-stu-id="e9e40-132">**WM\_PASTE**</span></span>](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

