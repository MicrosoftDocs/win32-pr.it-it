---
title: Codice di notifica EN_MAXTEXT (winuser. h)
description: Inviato quando l'inserimento di testo corrente supera il numero di caratteri specificato per il controllo di modifica.
ms.assetid: b03835d6-d06f-415a-97f2-d2b62b17e175
keywords:
- Controlli di Windows per il codice di notifica EN_MAXTEXT
topic_type:
- apiref
api_name:
- EN_MAXTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 454b48fb232f2225696efacc44d54660d3a83185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518658"
---
# <a name="en_maxtext-notification-code"></a><span data-ttu-id="54ae4-104">\_Codice di notifica en MAXTEXT</span><span class="sxs-lookup"><span data-stu-id="54ae4-104">EN\_MAXTEXT notification code</span></span>

<span data-ttu-id="54ae4-105">Inviato quando l'inserimento di testo corrente supera il numero di caratteri specificato per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="54ae4-105">Sent when the current text insertion has exceeded the specified number of characters for the edit control.</span></span> <span data-ttu-id="54ae4-106">L'inserimento del testo è stato troncato.</span><span class="sxs-lookup"><span data-stu-id="54ae4-106">The text insertion has been truncated.</span></span>

<span data-ttu-id="54ae4-107">Questo codice di notifica viene inviato anche quando un controllo di modifica non ha lo stile [**es \_ AUTOHSCROLL**](edit-control-styles.md) e il numero di caratteri da inserire supera la larghezza del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="54ae4-107">This notification code is also sent when an edit control does not have the [**ES\_AUTOHSCROLL**](edit-control-styles.md) style and the number of characters to be inserted would exceed the width of the edit control.</span></span>

<span data-ttu-id="54ae4-108">Questo codice di notifica viene inviato anche quando un controllo di modifica non ha lo stile [**es \_ AUTOVSCROLL**](edit-control-styles.md) e il numero totale di righe risultante da un inserimento di testo supera l'altezza del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="54ae4-108">This notification code is also sent when an edit control does not have the [**ES\_AUTOVSCROLL**](edit-control-styles.md) style and the total number of lines resulting from a text insertion would exceed the height of the edit control.</span></span>

<span data-ttu-id="54ae4-109">La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="54ae4-109">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_MAXTEXT

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="54ae4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="54ae4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54ae4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54ae4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54ae4-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="54ae4-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="54ae4-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="54ae4-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="54ae4-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54ae4-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54ae4-115">Handle per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="54ae4-115">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54ae4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="54ae4-116">Remarks</span></span>

<span data-ttu-id="54ae4-117">La finestra padre riceve sempre un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) per questo evento, ma non richiede una maschera di notifica inviata con [**em \_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="54ae4-117">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="54ae4-118">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="54ae4-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="54ae4-119">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="54ae4-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54ae4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54ae4-120">Requirements</span></span>



| <span data-ttu-id="54ae4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="54ae4-121">Requirement</span></span> | <span data-ttu-id="54ae4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="54ae4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54ae4-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54ae4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="54ae4-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54ae4-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="54ae4-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54ae4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="54ae4-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="54ae4-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="54ae4-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54ae4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="54ae4-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54ae4-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54ae4-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54ae4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54ae4-130">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="54ae4-130">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

