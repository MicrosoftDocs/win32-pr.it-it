---
title: Messaggio WM_DRAWCLIPBOARD (winuser. h)
description: Inviato alla prima finestra nella catena del visualizzatore degli Appunti quando il contenuto degli Appunti viene modificato. Ciò consente a una finestra del visualizzatore degli Appunti di visualizzare il nuovo contenuto degli Appunti. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- Scambio di dati del messaggio WM_DRAWCLIPBOARD
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5ee6f6893375e2604cb39247745fc2758ce8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301598"
---
# <a name="wm_drawclipboard-message"></a><span data-ttu-id="23352-106">\_Messaggio DRAWCLIPBOARD WM</span><span class="sxs-lookup"><span data-stu-id="23352-106">WM\_DRAWCLIPBOARD message</span></span>

<span data-ttu-id="23352-107">Inviato alla prima finestra nella catena del visualizzatore degli Appunti quando il contenuto degli Appunti viene modificato.</span><span class="sxs-lookup"><span data-stu-id="23352-107">Sent to the first window in the clipboard viewer chain when the content of the clipboard changes.</span></span> <span data-ttu-id="23352-108">Ciò consente a una finestra del visualizzatore degli Appunti di visualizzare il nuovo contenuto degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="23352-108">This enables a clipboard viewer window to display the new content of the clipboard.</span></span>

<span data-ttu-id="23352-109">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="23352-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DRAWCLIPBOARD                0x0308
```



## <a name="parameters"></a><span data-ttu-id="23352-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="23352-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23352-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23352-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23352-112">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="23352-112">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="23352-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23352-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23352-114">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="23352-114">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23352-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="23352-115">Remarks</span></span>

<span data-ttu-id="23352-116">Questo messaggio viene ricevuto solo dalle finestre del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="23352-116">Only clipboard viewer windows receive this message.</span></span> <span data-ttu-id="23352-117">Si tratta di finestre che sono state aggiunte alla catena del visualizzatore degli Appunti tramite la funzione [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="23352-117">These are windows that have been added to the clipboard viewer chain by using the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="23352-118">Ogni finestra che riceve il messaggio **WM \_ DRAWCLIPBOARD** deve chiamare la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per passare il messaggio alla finestra successiva nella catena del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="23352-118">Each window that receives the **WM\_DRAWCLIPBOARD** message must call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message on to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="23352-119">L'handle per la finestra successiva nella catena viene restituito da [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)e può cambiare in risposta a un messaggio [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .</span><span class="sxs-lookup"><span data-stu-id="23352-119">The handle to the next window in the chain is returned by [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer), and may change in response to a [**WM\_CHANGECBCHAIN**](wm-changecbchain.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="23352-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23352-120">Requirements</span></span>



| <span data-ttu-id="23352-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="23352-121">Requirement</span></span> | <span data-ttu-id="23352-122">Valore</span><span class="sxs-lookup"><span data-stu-id="23352-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23352-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23352-123">Minimum supported client</span></span><br/> | <span data-ttu-id="23352-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="23352-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="23352-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23352-125">Minimum supported server</span></span><br/> | <span data-ttu-id="23352-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="23352-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="23352-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23352-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="23352-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23352-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23352-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23352-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="23352-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="23352-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="23352-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="23352-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="23352-132">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="23352-132">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[<span data-ttu-id="23352-133">**\_CHANGECBCHAIN WM**</span><span class="sxs-lookup"><span data-stu-id="23352-133">**WM\_CHANGECBCHAIN**</span></span>](wm-changecbchain.md)
</dt> <dt>

<span data-ttu-id="23352-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="23352-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="23352-135">Appunti</span><span class="sxs-lookup"><span data-stu-id="23352-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

