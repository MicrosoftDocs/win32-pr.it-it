---
title: Codice di notifica LBN_SELCHANGE (winuser. h)
description: Notifica all'applicazione che la selezione in una casella di riepilogo è stata modificata in seguito all'input dell'utente. La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- Controlli di Windows per il codice di notifica LBN_SELCHANGE
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e029d1753a0fa74f39a59a459d6ede45811a40fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741570"
---
# <a name="lbn_selchange-notification-code"></a><span data-ttu-id="8cb10-105">\_Codice di notifica SelChange di LBN</span><span class="sxs-lookup"><span data-stu-id="8cb10-105">LBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="8cb10-106">Notifica all'applicazione che la selezione in una casella di riepilogo è stata modificata in seguito all'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8cb10-106">Notifies the application that the selection in a list box has changed as a result of user input.</span></span> <span data-ttu-id="8cb10-107">La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="8cb10-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="8cb10-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8cb10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cb10-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8cb10-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cb10-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="8cb10-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="8cb10-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="8cb10-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="8cb10-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8cb10-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cb10-113">Handle per la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="8cb10-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cb10-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8cb10-114">Remarks</span></span>

<span data-ttu-id="8cb10-115">Questo codice di notifica viene inviato solo da una casella di riepilogo con lo stile di [**\_ notifica lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8cb10-115">This notification code is sent only by a list box that has the [**LBS\_NOTIFY**](list-box-styles.md) style.</span></span>

<span data-ttu-id="8cb10-116">Questo codice di notifica non viene inviato se il messaggio [**lb \_ SETSEL**](lb-setsel.md), [**lb \_ secursel**](lb-setcursel.md), [**lb \_ SELECTSTRING**](lb-selectstring.md), [**lb \_ SELITEMRANGE**](lb-selitemrange.md) o [**lb \_ SELITEMRANGEEX**](lb-selitemrangeex.md) modifica la selezione.</span><span class="sxs-lookup"><span data-stu-id="8cb10-116">This notification code is not sent if the [**LB\_SETSEL**](lb-setsel.md), [**LB\_SETCURSEL**](lb-setcursel.md), [**LB\_SELECTSTRING**](lb-selectstring.md), [**LB\_SELITEMRANGE**](lb-selitemrange.md) or [**LB\_SELITEMRANGEEX**](lb-selitemrangeex.md) message changes the selection.</span></span>

<span data-ttu-id="8cb10-117">Per una casella di riepilogo a selezione multipla, \_ viene inviato il codice di notifica SelChange di LBN ogni volta che l'utente preme un tasto di direzione, anche se la selezione non cambia.</span><span class="sxs-lookup"><span data-stu-id="8cb10-117">For a multiple-selection list box, the LBN\_SELCHANGE notification code is sent whenever the user presses an arrow key, even if the selection does not change.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cb10-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8cb10-118">Requirements</span></span>



| <span data-ttu-id="8cb10-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cb10-119">Requirement</span></span> | <span data-ttu-id="8cb10-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8cb10-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cb10-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cb10-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8cb10-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8cb10-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8cb10-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8cb10-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8cb10-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8cb10-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8cb10-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8cb10-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cb10-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8cb10-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cb10-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8cb10-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="8cb10-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="8cb10-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8cb10-129">**di \_ lb**</span><span class="sxs-lookup"><span data-stu-id="8cb10-129">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="8cb10-130">\_DBLCLK LBN</span><span class="sxs-lookup"><span data-stu-id="8cb10-130">LBN\_DBLCLK</span></span>](lbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="8cb10-131">\_SELCANCEL LBN</span><span class="sxs-lookup"><span data-stu-id="8cb10-131">LBN\_SELCANCEL</span></span>](lbn-selcancel.md)
</dt> <dt>

<span data-ttu-id="8cb10-132">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="8cb10-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8cb10-133">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="8cb10-133">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

