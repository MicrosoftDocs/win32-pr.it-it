---
title: Codice di notifica EN_CORRECTTEXT (RichEdit. h)
description: Notifica a una finestra padre di un controllo Rich Edit che \_ si è verificato un gesto Syv corretto, assegnando alla finestra padre la possibilità di annullare la correzione del testo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- Controlli di Windows per il codice di notifica EN_CORRECTTEXT
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d1339513a94967ab60bdab2b9ee39172b19e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119087"
---
# <a name="en_correcttext-notification-code"></a><span data-ttu-id="78aad-105">\_Codice di notifica en CORRECTTEXT</span><span class="sxs-lookup"><span data-stu-id="78aad-105">EN\_CORRECTTEXT notification code</span></span>

<span data-ttu-id="78aad-106">Notifica a una finestra padre di un controllo Rich Edit che \_ si è verificato un gesto Syv corretto, assegnando alla finestra padre la possibilità di annullare la correzione del testo.</span><span class="sxs-lookup"><span data-stu-id="78aad-106">Notifies a rich edit control parent window that a SYV\_CORRECT gesture occurred, giving the parent window a chance to cancel correcting the text.</span></span> <span data-ttu-id="78aad-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="78aad-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="78aad-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="78aad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78aad-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78aad-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78aad-110">Struttura [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) che specifica la selezione da correggere.</span><span class="sxs-lookup"><span data-stu-id="78aad-110">An [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) structure specifying the selection to be corrected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78aad-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78aad-111">Return value</span></span>

<span data-ttu-id="78aad-112">Restituisce zero per ignorare l'azione.</span><span class="sxs-lookup"><span data-stu-id="78aad-112">Return zero to ignore the action.</span></span>

<span data-ttu-id="78aad-113">Restituisce un valore diverso da zero per elaborare l'azione.</span><span class="sxs-lookup"><span data-stu-id="78aad-113">Returns a nonzero value to process the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="78aad-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="78aad-114">Remarks</span></span>

<span data-ttu-id="78aad-115">Questo codice di notifica viene inviato solo se sono disponibili funzionalità di penna.</span><span class="sxs-lookup"><span data-stu-id="78aad-115">This notification code is sent only if pen capabilities are available.</span></span>

<span data-ttu-id="78aad-116">Per ricevere \_ i codici di notifica en CORRECTTEXT, specificare [**ENM \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="78aad-116">To receive EN\_CORRECTTEXT notification codes, specify [**ENM\_CORRECTTEXT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="78aad-117">Il \_ codice di notifica en CORRECTTEXT è supportato solo in Rich Edit version 1,0.</span><span class="sxs-lookup"><span data-stu-id="78aad-117">The EN\_CORRECTTEXT notification code is only supported in rich edit version 1.0.</span></span> <span data-ttu-id="78aad-118">Non è supportata nelle versioni successive di Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="78aad-118">It is not supported in later versions of rich edit.</span></span> <span data-ttu-id="78aad-119">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="78aad-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="78aad-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78aad-120">Requirements</span></span>



| <span data-ttu-id="78aad-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="78aad-121">Requirement</span></span> | <span data-ttu-id="78aad-122">Valore</span><span class="sxs-lookup"><span data-stu-id="78aad-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78aad-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78aad-123">Minimum supported client</span></span><br/> | <span data-ttu-id="78aad-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78aad-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78aad-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78aad-125">Minimum supported server</span></span><br/> | <span data-ttu-id="78aad-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78aad-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78aad-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78aad-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="78aad-128"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="78aad-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78aad-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78aad-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="78aad-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="78aad-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="78aad-131">**ENCORRECTTEXT**</span><span class="sxs-lookup"><span data-stu-id="78aad-131">**ENCORRECTTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





