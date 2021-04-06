---
title: Codice di notifica EN_CHANGE (winuser. h)
description: Inviato quando l'utente ha effettuato un'azione che potrebbe aver modificato il testo in un controllo di modifica.
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- Controlli di Windows per il codice di notifica EN_CHANGE
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ef26d1ec4f8ec1dc93e54d46b88c4fe7cc872b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873585"
---
# <a name="en_change-notification-code"></a><span data-ttu-id="b8ef9-104">\_Modifica del codice di notifica</span><span class="sxs-lookup"><span data-stu-id="b8ef9-104">EN\_CHANGE notification code</span></span>

<span data-ttu-id="b8ef9-105">Inviato quando l'utente ha effettuato un'azione che potrebbe aver modificato il testo in un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-105">Sent when the user has taken an action that may have altered text in an edit control.</span></span> <span data-ttu-id="b8ef9-106">A differenza del codice di notifica di [ \_ aggiornamento en](en-update.md) , questo codice di notifica viene inviato dopo l'aggiornamento dello schermo da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-106">Unlike the [EN\_UPDATE](en-update.md) notification code, this notification code is sent after the system updates the screen.</span></span> <span data-ttu-id="b8ef9-107">La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="b8ef9-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_CHANGE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="b8ef9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8ef9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8ef9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8ef9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8ef9-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="b8ef9-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="b8ef9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8ef9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8ef9-113">Handle per il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-113">A handle to the edit control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8ef9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8ef9-114">Remarks</span></span>

<span data-ttu-id="b8ef9-115">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-115">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="b8ef9-116">Per ricevere \_ i codici di notifica delle modifiche, specificare la [**\_ modifica ENM**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="b8ef9-116">To receive EN\_CHANGE notification codes, specify [**ENM\_CHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="b8ef9-117">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="b8ef9-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="b8ef9-118">Il \_ codice di notifica delle modifiche it non viene inviato quando si usa lo stile [**\_ multiriga es**](edit-control-styles.md) e il testo viene inviato tramite il testo [**WM \_**](/windows/desktop/winmsg/wm-settext).</span><span class="sxs-lookup"><span data-stu-id="b8ef9-118">The EN\_CHANGE notification code is not sent when the [**ES\_MULTILINE**](edit-control-styles.md) style is used and the text is sent through [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ef9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8ef9-119">Requirements</span></span>



| <span data-ttu-id="b8ef9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8ef9-120">Requirement</span></span> | <span data-ttu-id="b8ef9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b8ef9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ef9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8ef9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ef9-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8ef9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b8ef9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8ef9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ef9-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8ef9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b8ef9-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8ef9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8ef9-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8ef9-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8ef9-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8ef9-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="b8ef9-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b8ef9-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b8ef9-130">\_aggiornamento en</span><span class="sxs-lookup"><span data-stu-id="b8ef9-130">EN\_UPDATE</span></span>](en-update.md)
</dt> <dt>

<span data-ttu-id="b8ef9-131">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="b8ef9-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b8ef9-132">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="b8ef9-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

