---
title: Codice di notifica EN_SETFOCUS (winuser. h)
description: Inviato quando un controllo di modifica riceve lo stato attivo della tastiera. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un \_ messaggio di comando WM.
ms.assetid: 482d2afa-4e21-4f3f-bdf4-6966b34cc3c4
keywords:
- Controlli di Windows per il codice di notifica EN_SETFOCUS
topic_type:
- apiref
api_name:
- EN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cb96482f0e42669658dde3a39637e3c2311619
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743034"
---
# <a name="en_setfocus-notification-code"></a><span data-ttu-id="b2c1c-105">\_Codice di notifica di SetFocus</span><span class="sxs-lookup"><span data-stu-id="b2c1c-105">EN\_SETFOCUS notification code</span></span>

<span data-ttu-id="b2c1c-106">Inviato quando un controllo di modifica riceve lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="b2c1c-106">Sent when an edit control receives the keyboard focus.</span></span> <span data-ttu-id="b2c1c-107">La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="b2c1c-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="b2c1c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2c1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2c1c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2c1c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2c1c-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="b2c1c-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="b2c1c-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="b2c1c-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="b2c1c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2c1c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2c1c-113">Handle per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="b2c1c-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2c1c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2c1c-114">Remarks</span></span>

<span data-ttu-id="b2c1c-115">La finestra padre riceve sempre un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) per questo evento, ma non richiede una maschera di notifica inviata con [**em \_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="b2c1c-115">The parent window always receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

<span data-ttu-id="b2c1c-116">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b2c1c-116">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="b2c1c-117">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="b2c1c-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2c1c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2c1c-118">Requirements</span></span>



| <span data-ttu-id="b2c1c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2c1c-119">Requirement</span></span> | <span data-ttu-id="b2c1c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b2c1c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2c1c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2c1c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b2c1c-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2c1c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b2c1c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2c1c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b2c1c-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2c1c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b2c1c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2c1c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2c1c-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2c1c-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2c1c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2c1c-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2c1c-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b2c1c-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b2c1c-129">EN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="b2c1c-129">EN\_KILLFOCUS</span></span>](en-killfocus.md)
</dt> <dt>

<span data-ttu-id="b2c1c-130">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="b2c1c-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b2c1c-131">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="b2c1c-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

