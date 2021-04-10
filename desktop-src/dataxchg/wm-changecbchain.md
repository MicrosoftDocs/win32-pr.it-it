---
title: Messaggio WM_CHANGECBCHAIN (winuser. h)
description: Inviato alla prima finestra nella catena del visualizzatore degli Appunti quando una finestra viene rimossa dalla catena. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- Scambio di dati del messaggio WM_CHANGECBCHAIN
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab91640320e3659d0e9fb130f5c773ccbb7c4e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120043"
---
# <a name="wm_changecbchain-message"></a><span data-ttu-id="a6a2b-105">\_Messaggio CHANGECBCHAIN WM</span><span class="sxs-lookup"><span data-stu-id="a6a2b-105">WM\_CHANGECBCHAIN message</span></span>

<span data-ttu-id="a6a2b-106">Inviato alla prima finestra nella catena del visualizzatore degli Appunti quando una finestra viene rimossa dalla catena.</span><span class="sxs-lookup"><span data-stu-id="a6a2b-106">Sent to the first window in the clipboard viewer chain when a window is being removed from the chain.</span></span>

<span data-ttu-id="a6a2b-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a6a2b-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a><span data-ttu-id="a6a2b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6a2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a2b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6a2b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6a2b-110">Handle per la finestra da rimuovere dalla catena del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="a6a2b-110">A handle to the window being removed from the clipboard viewer chain.</span></span>

</dd> <dt>

<span data-ttu-id="a6a2b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6a2b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6a2b-112">Handle per la finestra successiva nella catena che segue la finestra da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a6a2b-112">A handle to the next window in the chain following the window being removed.</span></span> <span data-ttu-id="a6a2b-113">Questo parametro è **null** se la finestra da rimuovere è l'ultima finestra nella catena.</span><span class="sxs-lookup"><span data-stu-id="a6a2b-113">This parameter is **NULL** if the window being removed is the last window in the chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a2b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6a2b-114">Return value</span></span>

<span data-ttu-id="a6a2b-115">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="a6a2b-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6a2b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6a2b-116">Remarks</span></span>

<span data-ttu-id="a6a2b-117">Ogni finestra del visualizzatore degli Appunti Salva l'handle nella finestra successiva della catena del visualizzatore degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="a6a2b-117">Each clipboard viewer window saves the handle to the next window in the clipboard viewer chain.</span></span> <span data-ttu-id="a6a2b-118">Inizialmente, questo handle è il valore restituito della funzione [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .</span><span class="sxs-lookup"><span data-stu-id="a6a2b-118">Initially, this handle is the return value of the [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) function.</span></span>

<span data-ttu-id="a6a2b-119">Quando una finestra del visualizzatore degli Appunti riceve il messaggio **WM \_ CHANGECBCHAIN** , deve chiamare la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per passare il messaggio alla finestra successiva della catena, a meno che la finestra successiva non sia la finestra da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a6a2b-119">When a clipboard viewer window receives the **WM\_CHANGECBCHAIN** message, it should call the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to pass the message to the next window in the chain, unless the next window is the window being removed.</span></span> <span data-ttu-id="a6a2b-120">In questo caso, il visualizzatore degli Appunti deve salvare l'handle specificato dal parametro *lParam* come finestra successiva nella catena.</span><span class="sxs-lookup"><span data-stu-id="a6a2b-120">In this case, the clipboard viewer should save the handle specified by the *lParam* parameter as the next window in the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a2b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6a2b-121">Requirements</span></span>



| <span data-ttu-id="a6a2b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6a2b-122">Requirement</span></span> | <span data-ttu-id="a6a2b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a6a2b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a2b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6a2b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a6a2b-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a6a2b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a6a2b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6a2b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a6a2b-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a6a2b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a6a2b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6a2b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6a2b-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6a2b-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6a2b-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6a2b-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="a6a2b-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a6a2b-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a6a2b-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="a6a2b-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="a6a2b-133">**SetClipboardViewer**</span><span class="sxs-lookup"><span data-stu-id="a6a2b-133">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

<span data-ttu-id="a6a2b-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a6a2b-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a6a2b-135">Appunti</span><span class="sxs-lookup"><span data-stu-id="a6a2b-135">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

