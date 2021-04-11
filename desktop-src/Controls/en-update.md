---
title: Codice di notifica EN_UPDATE (winuser. h)
description: Inviato quando un controllo di modifica sta per essere ridisegnato.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- Controlli di Windows per il codice di notifica EN_UPDATE
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b045efcfb5d50cb2a85c9ae230e215263aa2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121018"
---
# <a name="en_update-notification-code"></a><span data-ttu-id="eeec2-104">\_Codice di notifica dell'aggiornamento en</span><span class="sxs-lookup"><span data-stu-id="eeec2-104">EN\_UPDATE notification code</span></span>

<span data-ttu-id="eeec2-105">Inviato quando un controllo di modifica sta per essere ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="eeec2-105">Sent when an edit control is about to redraw itself.</span></span> <span data-ttu-id="eeec2-106">Questo codice di notifica viene inviato dopo che il controllo ha formattato il testo, ma prima di visualizzare il testo.</span><span class="sxs-lookup"><span data-stu-id="eeec2-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="eeec2-107">In questo modo è possibile ridimensionare la finestra di controllo di modifica, se necessario.</span><span class="sxs-lookup"><span data-stu-id="eeec2-107">This makes it possible to resize the edit control window, if necessary.</span></span> <span data-ttu-id="eeec2-108">La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="eeec2-108">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_UPDATE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="eeec2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="eeec2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeec2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eeec2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eeec2-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="eeec2-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="eeec2-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="eeec2-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="eeec2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eeec2-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eeec2-114">Handle per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="eeec2-114">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eeec2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="eeec2-115">Remarks</span></span>

<span data-ttu-id="eeec2-116">**Modifica dettagliata 1,0:** Per ricevere \_ i codici di notifica degli aggiornamenti, specificare l' [**\_ aggiornamento di ENM**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="eeec2-116">**Rich Edit 1.0:** To receive EN\_UPDATE notification codes, specify [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="eeec2-117">**Rich Edit 2,0 e versioni successive:** Il flag di [**\_ aggiornamento ENM**](rich-edit-control-event-mask-flags.md) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="eeec2-117">**Rich Edit 2.0 and later:** The [**ENM\_UPDATE**](rich-edit-control-event-mask-flags.md) flag is ignored.</span></span> <span data-ttu-id="eeec2-118">Il \_ codice di notifica dell'aggiornamento it viene sempre ricevuto.</span><span class="sxs-lookup"><span data-stu-id="eeec2-118">The EN\_UPDATE notification code is always received.</span></span> <span data-ttu-id="eeec2-119">Tuttavia, quando Microsoft Rich Edit 3,0 emula Microsoft Rich Edit 1,0, per ricevere \_ i codici di notifica di aggiornamento en, è necessario specificare l' **\_ aggiornamento di ENM** nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="eeec2-119">However, when Microsoft Rich Edit 3.0 emulates Microsoft Rich Edit 1.0, to receive EN\_UPDATE notification codes you must specify **ENM\_UPDATE** in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="eeec2-120">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="eeec2-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eeec2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eeec2-121">Requirements</span></span>



| <span data-ttu-id="eeec2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeec2-122">Requirement</span></span> | <span data-ttu-id="eeec2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="eeec2-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeec2-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eeec2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eeec2-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eeec2-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="eeec2-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eeec2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eeec2-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eeec2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="eeec2-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eeec2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeec2-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eeec2-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeec2-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eeec2-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="eeec2-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="eeec2-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eeec2-132">\_modifica en</span><span class="sxs-lookup"><span data-stu-id="eeec2-132">EN\_CHANGE</span></span>](en-change.md)
</dt> <dt>

<span data-ttu-id="eeec2-133">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="eeec2-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="eeec2-134">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="eeec2-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

