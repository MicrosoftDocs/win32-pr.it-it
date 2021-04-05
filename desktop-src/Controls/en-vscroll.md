---
title: Codice di notifica EN_VSCROLL (winuser. h)
description: Inviato quando l'utente fa clic sulla barra di scorrimento verticale di un controllo di modifica o quando l'utente scorre la rotellina del mouse sul controllo di modifica.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- Controlli di Windows per il codice di notifica EN_VSCROLL
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1f99b9ea05d037b5c00562a24bda1e434ce08d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874570"
---
# <a name="en_vscroll-notification-code"></a><span data-ttu-id="7da25-104">\_Codice di notifica en VSCROLL</span><span class="sxs-lookup"><span data-stu-id="7da25-104">EN\_VSCROLL notification code</span></span>

<span data-ttu-id="7da25-105">Inviato quando l'utente fa clic sulla barra di scorrimento verticale di un controllo di modifica o quando l'utente scorre la rotellina del mouse sul controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="7da25-105">Sent when the user clicks an edit control's vertical scroll bar or when the user scrolls the mouse wheel over the edit control.</span></span> <span data-ttu-id="7da25-106">La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="7da25-106">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="7da25-107">La finestra padre riceve una notifica prima che lo schermo venga aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7da25-107">The parent window is notified before the screen is updated.</span></span>


```C++
EN_VSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="7da25-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7da25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7da25-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7da25-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7da25-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="7da25-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="7da25-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="7da25-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="7da25-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7da25-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7da25-113">Handle per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="7da25-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7da25-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7da25-114">Remarks</span></span>

<span data-ttu-id="7da25-115">Questo messaggio viene inviato per gli eventi del mouse seguenti sulla barra di scorrimento verticale: facendo clic su un pulsante freccia o facendo clic tra il pulsante freccia e il cursore.</span><span class="sxs-lookup"><span data-stu-id="7da25-115">This message is sent for the following mouse events on the vertical scroll bar: clicking either arrow button or clicking between the arrow button and the thumb.</span></span> <span data-ttu-id="7da25-116">Tuttavia, il messaggio non viene inviato quando si fa clic sul mouse della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="7da25-116">However, the message is not sent when clicking the scroll bar mouse itself.</span></span> <span data-ttu-id="7da25-117">Il messaggio viene inviato anche quando un evento della tastiera causa una modifica nell'area di visualizzazione del controllo di modifica, ad esempio, premendo HOME, fine, PGSU, PGGIÙ, freccia su o freccia giù.</span><span class="sxs-lookup"><span data-stu-id="7da25-117">The message is also sent when a keyboard event causes a change in the view area of the edit control, for example, pressing HOME, END, PAGE UP, PAGE DOWN, UP ARROW, or DOWN ARROW.</span></span>

<span data-ttu-id="7da25-118">La rotellina del mouse è un mouse con una rotellina centrale che scorre.</span><span class="sxs-lookup"><span data-stu-id="7da25-118">The mouse wheel is a mouse that has a center wheel that scrolls.</span></span> <span data-ttu-id="7da25-119">Per ulteriori informazioni, vedere la sezione "rotellina del mouse" in [informazioni sull'input del mouse](/windows/desktop/inputdev/about-mouse-input).</span><span class="sxs-lookup"><span data-stu-id="7da25-119">For more information, see "The Mouse Wheel" in [About Mouse Input](/windows/desktop/inputdev/about-mouse-input).</span></span>

<span data-ttu-id="7da25-120">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="7da25-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="7da25-121">Per ricevere \_ i codici di notifica en VSCROLL, specificare [**ENM \_ Scroll**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="7da25-121">To receive EN\_VSCROLL notification codes, specify [**ENM\_SCROLL**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="7da25-122">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="7da25-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7da25-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7da25-123">Requirements</span></span>



| <span data-ttu-id="7da25-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7da25-124">Requirement</span></span> | <span data-ttu-id="7da25-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7da25-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da25-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7da25-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7da25-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7da25-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7da25-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7da25-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7da25-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7da25-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7da25-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7da25-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7da25-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7da25-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7da25-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7da25-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="7da25-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7da25-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7da25-134">EN \_ HSCROLL</span><span class="sxs-lookup"><span data-stu-id="7da25-134">EN\_HSCROLL</span></span>](en-hscroll.md)
</dt> <dt>

<span data-ttu-id="7da25-135">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7da25-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7da25-136">Uso di controlli di modifica</span><span class="sxs-lookup"><span data-stu-id="7da25-136">Using Edit Controls</span></span>](using-edit-controls.md)
</dt> <dt>

<span data-ttu-id="7da25-137">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="7da25-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="7da25-138">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="7da25-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

