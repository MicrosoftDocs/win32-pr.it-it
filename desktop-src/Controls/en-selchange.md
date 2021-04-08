---
title: Codice di notifica EN_SELCHANGE (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che la selezione corrente è stata modificata. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- Controlli di Windows per il codice di notifica EN_SELCHANGE
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79dfcf951f88fa1e10f4723bd9843421f0e20ae5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743031"
---
# <a name="en_selchange-notification-code"></a><span data-ttu-id="b4171-105">\_Codice di notifica en SelChange</span><span class="sxs-lookup"><span data-stu-id="b4171-105">EN\_SELCHANGE notification code</span></span>

<span data-ttu-id="b4171-106">Notifica alla finestra padre di un controllo Rich Edit che la selezione corrente è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="b4171-106">Notifies a rich edit control's parent window that the current selection has changed.</span></span> <span data-ttu-id="b4171-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b4171-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="b4171-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4171-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4171-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4171-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4171-110">Struttura [**selChange**](/windows/desktop/api/Richedit/ns-richedit-selchange) che riceve informazioni sulla selezione.</span><span class="sxs-lookup"><span data-stu-id="b4171-110">A [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4171-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4171-111">Return value</span></span>

<span data-ttu-id="b4171-112">Questo codice di notifica non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="b4171-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4171-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4171-113">Remarks</span></span>

<span data-ttu-id="b4171-114">Per ricevere \_ i codici di notifica en SelChange, specificare [**ENM \_ selChange**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="b4171-114">To receive EN\_SELCHANGE notification codes, specify [**ENM\_SELCHANGE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="b4171-115">Questo codice di notifica viene inviato quando viene modificata la posizione del punto di inserimento e non è selezionato alcun testo (la selezione è vuota).</span><span class="sxs-lookup"><span data-stu-id="b4171-115">This notification code is sent when the caret position changes and no text is selected (the selection is empty).</span></span> <span data-ttu-id="b4171-116">La posizione del punto di inserimento può variare quando l'utente fa clic con il mouse, digita o preme un tasto di direzione.</span><span class="sxs-lookup"><span data-stu-id="b4171-116">The caret position can change when the user clicks the mouse, types, or presses an arrow key.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4171-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4171-117">Requirements</span></span>



| <span data-ttu-id="b4171-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4171-118">Requirement</span></span> | <span data-ttu-id="b4171-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b4171-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4171-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4171-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b4171-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4171-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4171-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4171-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b4171-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4171-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4171-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4171-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4171-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4171-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4171-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4171-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b4171-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b4171-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b4171-128">**SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="b4171-128">**SELCHANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[<span data-ttu-id="b4171-129">**\_notifica WM**</span><span class="sxs-lookup"><span data-stu-id="b4171-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





