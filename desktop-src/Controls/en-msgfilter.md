---
title: Codice di notifica EN_MSGFILTER (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit una tastiera o un evento del mouse nel controllo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- Controlli di Windows per il codice di notifica EN_MSGFILTER
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40ddb3e9b1d5314e2e981b00f0e0ef8e22974242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119938"
---
# <a name="en_msgfilter-notification-code"></a><span data-ttu-id="e6a07-105">\_Codice di notifica en msgfilter</span><span class="sxs-lookup"><span data-stu-id="e6a07-105">EN\_MSGFILTER notification code</span></span>

<span data-ttu-id="e6a07-106">Notifica alla finestra padre di un controllo Rich Edit una tastiera o un evento del mouse nel controllo.</span><span class="sxs-lookup"><span data-stu-id="e6a07-106">Notifies a rich edit control's parent window of a keyboard or mouse event in the control.</span></span> <span data-ttu-id="e6a07-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e6a07-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e6a07-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6a07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6a07-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6a07-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6a07-110">Struttura [**msgfilter**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) contenente informazioni sulla tastiera o sul messaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="e6a07-110">A [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure containing information about the keyboard or mouse message.</span></span> <span data-ttu-id="e6a07-111">Se la finestra padre modifica questa struttura e restituisce un valore diverso da zero, il messaggio modificato viene elaborato anziché quello originale.</span><span class="sxs-lookup"><span data-stu-id="e6a07-111">If the parent window modifies this structure and returns a nonzero value, the modified message is processed instead of the original one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6a07-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6a07-112">Return value</span></span>

<span data-ttu-id="e6a07-113">Restituisce zero se il controllo deve elaborare l'evento della tastiera o del mouse.</span><span class="sxs-lookup"><span data-stu-id="e6a07-113">Return zero if the control should process the keyboard or mouse event.</span></span>

<span data-ttu-id="e6a07-114">Restituisce un valore diverso da zero se il controllo deve ignorare l'evento della tastiera o del mouse.</span><span class="sxs-lookup"><span data-stu-id="e6a07-114">Return nonzero if the control should ignore the keyboard or mouse event.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a07-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6a07-115">Remarks</span></span>

<span data-ttu-id="e6a07-116">Per ricevere i \_ codici di notifica en msgfilter per gli eventi, specificare uno o più dei flag seguenti nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="e6a07-116">To receive EN\_MSGFILTER notification codes for events, specify one or more of the following flags in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>



| <span data-ttu-id="e6a07-117">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="e6a07-117">Flag</span></span>                                                                             | <span data-ttu-id="e6a07-118">Significato</span><span class="sxs-lookup"><span data-stu-id="e6a07-118">Meaning</span></span>                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="e6a07-119">**ENM di \_ UNIformi**</span><span class="sxs-lookup"><span data-stu-id="e6a07-119">**ENM\_KEYEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)       | <span data-ttu-id="e6a07-120">Per ricevere i codici di notifica per gli eventi della tastiera.</span><span class="sxs-lookup"><span data-stu-id="e6a07-120">To receive notification codes for keyboard events.</span></span>     |
| [<span data-ttu-id="e6a07-121">**\_MOUSEEVENTS ENM**</span><span class="sxs-lookup"><span data-stu-id="e6a07-121">**ENM\_MOUSEEVENTS**</span></span>](rich-edit-control-event-mask-flags.md)   | <span data-ttu-id="e6a07-122">Per ricevere i codici di notifica per gli eventi del mouse.</span><span class="sxs-lookup"><span data-stu-id="e6a07-122">To receive notification codes for mouse events.</span></span>        |
| [<span data-ttu-id="e6a07-123">**\_SCROLLEVENTS ENM**</span><span class="sxs-lookup"><span data-stu-id="e6a07-123">**ENM\_SCROLLEVENTS**</span></span>](rich-edit-control-event-mask-flags.md) | <span data-ttu-id="e6a07-124">Per ricevere i codici di notifica per un evento della rotellina del mouse.</span><span class="sxs-lookup"><span data-stu-id="e6a07-124">To receive notification codes for a mouse wheel event.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e6a07-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6a07-125">Requirements</span></span>



| <span data-ttu-id="e6a07-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6a07-126">Requirement</span></span> | <span data-ttu-id="e6a07-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e6a07-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a07-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6a07-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a07-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6a07-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6a07-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6a07-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a07-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6a07-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6a07-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6a07-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6a07-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6a07-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6a07-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6a07-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6a07-135">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e6a07-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e6a07-136">**MSGFILTER**</span><span class="sxs-lookup"><span data-stu-id="e6a07-136">**MSGFILTER**</span></span>](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[<span data-ttu-id="e6a07-137">**\_notifica WM**</span><span class="sxs-lookup"><span data-stu-id="e6a07-137">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





