---
title: Codice di notifica EN_OLEOPFAILED (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che un'azione dell'utente su un oggetto Component Object Model (COM) ha avuto esito negativo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- Controlli di Windows per il codice di notifica EN_OLEOPFAILED
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 139c51642c8cb6d5efd369cf6b373068604439b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873901"
---
# <a name="en_oleopfailed-notification-code"></a><span data-ttu-id="ce00d-105">\_Codice di notifica en OLEOPFAILED</span><span class="sxs-lookup"><span data-stu-id="ce00d-105">EN\_OLEOPFAILED notification code</span></span>

<span data-ttu-id="ce00d-106">Notifica alla finestra padre di un controllo Rich Edit che un'azione dell'utente su un oggetto Component Object Model (COM) ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ce00d-106">Notifies a rich edit control's parent window that a user action on a Component Object Model (COM) object has failed.</span></span> <span data-ttu-id="ce00d-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ce00d-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ce00d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce00d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce00d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce00d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce00d-110">Struttura [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) che contiene informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="ce00d-110">An [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) structure that contains information about the failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce00d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce00d-111">Return value</span></span>

<span data-ttu-id="ce00d-112">Questo codice di notifica restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="ce00d-112">This notification code returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce00d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce00d-113">Remarks</span></span>

<span data-ttu-id="ce00d-114">La finestra padre otterrà sempre un messaggio [**di \_ notifica WM**](wm-notify.md) per questo evento, ma non richiede una maschera di notifica inviata con [**em \_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="ce00d-114">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce00d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce00d-115">Requirements</span></span>



| <span data-ttu-id="ce00d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce00d-116">Requirement</span></span> | <span data-ttu-id="ce00d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ce00d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce00d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce00d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ce00d-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce00d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce00d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce00d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ce00d-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ce00d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce00d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce00d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce00d-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce00d-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce00d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce00d-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="ce00d-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ce00d-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ce00d-126">**ENOLEOPFAILED**</span><span class="sxs-lookup"><span data-stu-id="ce00d-126">**ENOLEOPFAILED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 





