---
title: Codice di notifica EN_PROTECTED (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che l'utente sta eseguendo un'azione che modifica un intervallo di testo protetto. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- Controlli di Windows per il codice di notifica EN_PROTECTED
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476978"
---
# <a name="en_protected-notification-code"></a><span data-ttu-id="738f0-105">\_Codice di notifica protetto da it</span><span class="sxs-lookup"><span data-stu-id="738f0-105">EN\_PROTECTED notification code</span></span>

<span data-ttu-id="738f0-106">Notifica alla finestra padre di un controllo Rich Edit che l'utente sta eseguendo un'azione che modifica un intervallo di testo protetto.</span><span class="sxs-lookup"><span data-stu-id="738f0-106">Notifies a rich edit control's parent window that the user is taking an action that would change a protected range of text.</span></span> <span data-ttu-id="738f0-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="738f0-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="738f0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="738f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="738f0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="738f0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="738f0-110">Struttura [**protetta**](/windows/desktop/api/Richedit/ns-richedit-enprotected) contenente le informazioni sul messaggio che ha attivato il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="738f0-110">An [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure containing information about the message that triggered the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="738f0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="738f0-111">Return value</span></span>

<span data-ttu-id="738f0-112">Restituisce zero per consentire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="738f0-112">Return zero to allow the operation.</span></span>

<span data-ttu-id="738f0-113">Restituisce un valore diverso da zero per impedire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="738f0-113">Return a nonzero value to prevent the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="738f0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="738f0-114">Remarks</span></span>

<span data-ttu-id="738f0-115">Se viene restituito zero e i membri **msg**, **wParam** e **lParam** della struttura [**protetta**](/windows/desktop/api/Richedit/ns-richedit-enprotected) vengono modificati, il controllo elabora il messaggio modificato anziché il messaggio originale.</span><span class="sxs-lookup"><span data-stu-id="738f0-115">If zero is returned and the **msg**, **wParam**, and **lParam** members of the [**ENPROTECTED**](/windows/desktop/api/Richedit/ns-richedit-enprotected) structure are changed, the control processes the revised message instead of the original message.</span></span>

<span data-ttu-id="738f0-116">Per ricevere \_ i codici di notifica protetti it, specificare [**ENM \_ protected**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="738f0-116">To receive EN\_PROTECTED notification codes, specify [**ENM\_PROTECTED**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="738f0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="738f0-117">Requirements</span></span>



| <span data-ttu-id="738f0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="738f0-118">Requirement</span></span> | <span data-ttu-id="738f0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="738f0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="738f0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="738f0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="738f0-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="738f0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="738f0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="738f0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="738f0-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="738f0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="738f0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="738f0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="738f0-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="738f0-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="738f0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="738f0-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="738f0-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="738f0-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="738f0-128">**PROTETTO**</span><span class="sxs-lookup"><span data-stu-id="738f0-128">**ENPROTECTED**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[<span data-ttu-id="738f0-129">**\_notifica WM**</span><span class="sxs-lookup"><span data-stu-id="738f0-129">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





