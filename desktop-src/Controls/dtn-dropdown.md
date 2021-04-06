---
title: Codice di notifica DTN_DROPDOWN (COMmctrl. h)
description: Inviato da un controllo di selezione data e ora (DTP) quando l'utente attiva il calendario mensile a discesa. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- Controlli di Windows per il codice di notifica DTN_DROPDOWN
topic_type:
- apiref
api_name:
- DTN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101a25a8e2da09b9f4065a54fcff9896690adbb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874165"
---
# <a name="dtn_dropdown-notification-code"></a><span data-ttu-id="bc058-105">\_Codice di notifica a discesa DTN</span><span class="sxs-lookup"><span data-stu-id="bc058-105">DTN\_DROPDOWN notification code</span></span>

<span data-ttu-id="bc058-106">Inviato da un controllo di selezione data e ora (DTP) quando l'utente attiva il calendario mensile a discesa.</span><span class="sxs-lookup"><span data-stu-id="bc058-106">Sent by a date and time picker (DTP) control when the user activates the drop-down month calendar.</span></span> <span data-ttu-id="bc058-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bc058-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a><span data-ttu-id="bc058-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc058-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc058-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc058-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc058-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenente informazioni sulla notifica.</span><span class="sxs-lookup"><span data-stu-id="bc058-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc058-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc058-111">Return value</span></span>

<span data-ttu-id="bc058-112">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="bc058-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc058-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc058-113">Remarks</span></span>

<span data-ttu-id="bc058-114">Un'attività che il gestore di notifiche potrebbe dover eseguire è personalizzare il controllo del calendario a discesa month.</span><span class="sxs-lookup"><span data-stu-id="bc058-114">One task that your notification handler may need to perform is to customize the dropdown month-calendar control.</span></span> <span data-ttu-id="bc058-115">Ad esempio, se non si desidera "Vai a oggi", è necessario impostare lo stile [**MCS \_ notoday**](month-calendar-control-styles.md)  del controllo.</span><span class="sxs-lookup"><span data-stu-id="bc058-115">For instance, if you do not want "Go To Today," you need to set the control's [**MCS\_NOTODAY**](month-calendar-control-styles.md)  style.</span></span> <span data-ttu-id="bc058-116">Per recuperare un handle per il controllo di calendario mensile, inviare il controllo DTP a un messaggio [**\_ GETMONTHCAL DTM**](dtm-getmonthcal.md) .</span><span class="sxs-lookup"><span data-stu-id="bc058-116">To retrieve a handle to the month-calendar control, send the DTP control a [**DTM\_GETMONTHCAL**](dtm-getmonthcal.md) message.</span></span> <span data-ttu-id="bc058-117">È quindi possibile usare questo handle e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per impostare lo stile del calendario mensile desiderato.</span><span class="sxs-lookup"><span data-stu-id="bc058-117">You can then use this handle and [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) to set the desired month-calendar style.</span></span>

<span data-ttu-id="bc058-118">I controlli DTP non gestiscono un controllo calendario mensile figlio statico.</span><span class="sxs-lookup"><span data-stu-id="bc058-118">DTP controls do not maintain a static child month calendar control.</span></span> <span data-ttu-id="bc058-119">Il controllo DTP crea un nuovo controllo di calendario mensile prima di inviare il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="bc058-119">The DTP control creates a new month calendar control before sending this notification code.</span></span> <span data-ttu-id="bc058-120">Inoltre, il controllo DTP Elimina il controllo figlio quando non è attivo (visibile).</span><span class="sxs-lookup"><span data-stu-id="bc058-120">Additionally, the DTP control destroys the child control when it is not active (visible).</span></span> <span data-ttu-id="bc058-121">Quindi, l'applicazione non deve basarsi su un handle di finestra statico per il calendario mensile figlio del controllo.</span><span class="sxs-lookup"><span data-stu-id="bc058-121">So your application must not rely on a static window handle to the control's child month calendar.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc058-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc058-122">Requirements</span></span>



| <span data-ttu-id="bc058-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc058-123">Requirement</span></span> | <span data-ttu-id="bc058-124">Valore</span><span class="sxs-lookup"><span data-stu-id="bc058-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc058-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc058-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bc058-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bc058-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc058-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc058-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bc058-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bc058-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc058-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc058-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc058-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc058-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc058-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc058-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc058-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="bc058-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bc058-133">primo piano DTN \_</span><span class="sxs-lookup"><span data-stu-id="bc058-133">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> <dt>

[<span data-ttu-id="bc058-134">**\_GETMONTHCAL DTM**</span><span class="sxs-lookup"><span data-stu-id="bc058-134">**DTM\_GETMONTHCAL**</span></span>](dtm-getmonthcal.md)
</dt> </dl>

 

