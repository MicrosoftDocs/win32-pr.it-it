---
title: Codice di notifica EN_REQUESTRESIZE (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che il contenuto del controllo è più piccolo o maggiore delle dimensioni della finestra del controllo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- Controlli di Windows per il codice di notifica EN_REQUESTRESIZE
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120315"
---
# <a name="en_requestresize-notification-code"></a><span data-ttu-id="47740-105">\_Codice di notifica en REQUESTRESIZE</span><span class="sxs-lookup"><span data-stu-id="47740-105">EN\_REQUESTRESIZE notification code</span></span>

<span data-ttu-id="47740-106">Notifica alla finestra padre di un controllo Rich Edit che il contenuto del controllo è più piccolo o maggiore delle dimensioni della finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="47740-106">Notifies a rich edit control's parent window that the control's contents are either smaller or larger than the control's window size.</span></span> <span data-ttu-id="47740-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="47740-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="47740-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="47740-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47740-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="47740-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="47740-110">Struttura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) che riceve la dimensione richiesta.</span><span class="sxs-lookup"><span data-stu-id="47740-110">A [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) structure that receives the requested size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47740-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47740-111">Return value</span></span>

<span data-ttu-id="47740-112">Questo codice di notifica non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="47740-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47740-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="47740-113">Remarks</span></span>

<span data-ttu-id="47740-114">Per supportare il comportamento senza fondo di un controllo Rich Edit, la finestra padre deve ridimensionare il controllo quando riceve il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="47740-114">To support the bottomless behavior of a rich edit control, the parent window must resize the control when it receives this notification code.</span></span>

<span data-ttu-id="47740-115">Per ricevere \_ i codici di notifica en REQUESTRESIZE, specificare [**ENM \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="47740-115">To receive EN\_REQUESTRESIZE notification codes, specify [**ENM\_REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="47740-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47740-116">Requirements</span></span>



| <span data-ttu-id="47740-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="47740-117">Requirement</span></span> | <span data-ttu-id="47740-118">Valore</span><span class="sxs-lookup"><span data-stu-id="47740-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47740-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47740-119">Minimum supported client</span></span><br/> | <span data-ttu-id="47740-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="47740-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="47740-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47740-121">Minimum supported server</span></span><br/> | <span data-ttu-id="47740-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="47740-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="47740-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47740-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="47740-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="47740-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47740-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47740-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="47740-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="47740-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="47740-127">**REQRESIZE**</span><span class="sxs-lookup"><span data-stu-id="47740-127">**REQRESIZE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[<span data-ttu-id="47740-128">**\_notifica WM**</span><span class="sxs-lookup"><span data-stu-id="47740-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





