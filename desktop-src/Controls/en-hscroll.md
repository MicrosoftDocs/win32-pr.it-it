---
title: Codice di notifica EN_HSCROLL (winuser. h)
description: Inviato quando l'utente fa clic sulla barra di scorrimento orizzontale di un controllo di modifica. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un \_ messaggio di comando WM. La finestra padre riceve una notifica prima che lo schermo venga aggiornato.
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- Controlli di Windows per il codice di notifica EN_HSCROLL
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f90f6e781409419e39390e64251506b4cc915a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874026"
---
# <a name="en_hscroll-notification-code"></a><span data-ttu-id="77552-106">\_Codice di notifica en HSCROLL</span><span class="sxs-lookup"><span data-stu-id="77552-106">EN\_HSCROLL notification code</span></span>

<span data-ttu-id="77552-107">Inviato quando l'utente fa clic sulla barra di scorrimento orizzontale di un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="77552-107">Sent when the user clicks an edit control's horizontal scroll bar.</span></span> <span data-ttu-id="77552-108">La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="77552-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="77552-109">La finestra padre riceve una notifica prima che lo schermo venga aggiornato.</span><span class="sxs-lookup"><span data-stu-id="77552-109">The parent window is notified before the screen is updated.</span></span>


```C++
EN_HSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="77552-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="77552-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77552-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77552-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77552-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="77552-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="77552-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="77552-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="77552-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77552-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77552-115">Handle per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="77552-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77552-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="77552-116">Remarks</span></span>

<span data-ttu-id="77552-117">Questo codice di notifica viene inviato per gli eventi del mouse seguenti sulla barra di scorrimento orizzontale: facendo clic su un pulsante freccia o facendo clic tra il pulsante freccia e il cursore.</span><span class="sxs-lookup"><span data-stu-id="77552-117">This notification code is sent for the following mouse events on the horizontal scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="77552-118">Tuttavia, il codice di notifica non viene inviato quando si fa clic sul cursore della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="77552-118">However, the notification code is not sent when clicking the scroll bar thumb itself.</span></span> <span data-ttu-id="77552-119">Il codice di notifica viene inviato anche quando un evento della tastiera causa una modifica nell'area di visualizzazione del controllo di modifica, ad esempio premendo HOME, fine, freccia sinistra o freccia destra.</span><span class="sxs-lookup"><span data-stu-id="77552-119">The notification code is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, LEFT ARROW, or RIGHT ARROW.</span></span>

<span data-ttu-id="77552-120">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="77552-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="77552-121">Per ricevere i codici di notifica **en \_ HSCROLL** , specificare [**ENM \_ Scroll**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="77552-121">To receive **EN\_HSCROLL** notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="77552-122">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="77552-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77552-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77552-123">Requirements</span></span>



| <span data-ttu-id="77552-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="77552-124">Requirement</span></span> | <span data-ttu-id="77552-125">Valore</span><span class="sxs-lookup"><span data-stu-id="77552-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77552-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77552-126">Minimum supported client</span></span><br/> | <span data-ttu-id="77552-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77552-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="77552-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77552-128">Minimum supported server</span></span><br/> | <span data-ttu-id="77552-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77552-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="77552-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77552-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="77552-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77552-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77552-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77552-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="77552-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="77552-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="77552-134">EN \_ VSCROLL</span><span class="sxs-lookup"><span data-stu-id="77552-134">EN\_VSCROLL</span></span>](en-vscroll.md)
</dt> <dt>

<span data-ttu-id="77552-135">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="77552-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="77552-136">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="77552-136">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

