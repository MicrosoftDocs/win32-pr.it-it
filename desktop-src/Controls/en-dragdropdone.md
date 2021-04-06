---
title: Codice di notifica EN_DRAGDROPDONE (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che l'operazione di trascinamento della selezione è stata completata. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 3c8b95cc-86ef-4aec-b551-11dca50ea5c5
keywords:
- Controlli di Windows per il codice di notifica EN_DRAGDROPDONE
topic_type:
- apiref
api_name:
- EN_DRAGDROPDONE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10b6718122791bcc862866fbaf17ed43e8bfd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963807"
---
# <a name="en_dragdropdone-notification-code"></a><span data-ttu-id="9ab37-105">\_Codice di notifica en DRAGDROPDONE</span><span class="sxs-lookup"><span data-stu-id="9ab37-105">EN\_DRAGDROPDONE notification code</span></span>

<span data-ttu-id="9ab37-106">Notifica alla finestra padre di un controllo Rich Edit che l'operazione di trascinamento della selezione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="9ab37-106">Notifies a rich edit control's parent window that the drag-and-drop operation has completed.</span></span> <span data-ttu-id="9ab37-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab37-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_DRAGDROPDONE

    pnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9ab37-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ab37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ab37-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ab37-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ab37-110">Struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="9ab37-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ab37-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ab37-111">Return value</span></span>

<span data-ttu-id="9ab37-112">Questo codice di notifica non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="9ab37-112">This notification code does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ab37-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ab37-113">Remarks</span></span>

<span data-ttu-id="9ab37-114">Per ricevere un \_ codice di notifica en DRAGDROPDONE, specificare il flag [**ENM \_ DRAGDROPDONE**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il [**messaggio \_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab37-114">To receive an EN\_DRAGDROPDONE notification code, specify the [**ENM\_DRAGDROPDONE**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ab37-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ab37-115">Requirements</span></span>



| <span data-ttu-id="9ab37-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ab37-116">Requirement</span></span> | <span data-ttu-id="9ab37-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9ab37-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab37-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ab37-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9ab37-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ab37-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ab37-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ab37-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9ab37-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ab37-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ab37-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ab37-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ab37-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ab37-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ab37-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ab37-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ab37-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="9ab37-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9ab37-126">**\_SETEVENTMASK em**</span><span class="sxs-lookup"><span data-stu-id="9ab37-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> </dl>

 

 





