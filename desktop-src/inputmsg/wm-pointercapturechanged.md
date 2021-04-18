---
title: Messaggio WM_POINTERCAPTURECHANGED
description: Inviato a una finestra che sta perdendo l'acquisizione di un puntatore di input.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERCAPTURECHANGED
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302385"
---
# <a name="wm_pointercapturechanged-message"></a><span data-ttu-id="b409e-104">Messaggio WM_POINTERCAPTURECHANGED</span><span class="sxs-lookup"><span data-stu-id="b409e-104">WM_POINTERCAPTURECHANGED message</span></span>

<span data-ttu-id="b409e-105">Inviato a una finestra che sta perdendo l'acquisizione di un puntatore di input.</span><span class="sxs-lookup"><span data-stu-id="b409e-105">Sent to a window that is losing capture of an input pointer.</span></span>

<span data-ttu-id="b409e-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b409e-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a><span data-ttu-id="b409e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b409e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b409e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b409e-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b409e-109">Contiene informazioni sul puntatore di input che viene perso.</span><span class="sxs-lookup"><span data-stu-id="b409e-109">Contains information about the input pointer that is being lost.</span></span> <span data-ttu-id="b409e-110">Usare [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) per ottenere l'ID del puntatore.</span><span class="sxs-lookup"><span data-stu-id="b409e-110">Use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to get the pointer ID.</span></span>

</dd> <dt>

<span data-ttu-id="b409e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b409e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b409e-112">Contiene un handle per la finestra che sta acquisendo il puntatore di input.</span><span class="sxs-lookup"><span data-stu-id="b409e-112">Contains a handle to the window that is capturing the input pointer.</span></span> <span data-ttu-id="b409e-113">Questo valore può essere NULL se il puntatore non viene più acquisito dalla finestra.</span><span class="sxs-lookup"><span data-stu-id="b409e-113">This value can be NULL if the pointer is no longer being captured by the window.</span></span>

<span data-ttu-id="b409e-114">Se questo messaggio viene generato dall'elaborazione interna, il valore può essere l'handle della finestra che riceve il messaggio.</span><span class="sxs-lookup"><span data-stu-id="b409e-114">If this message is generated from internal processing, the value can be the handle of the window receiving the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b409e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b409e-115">Return value</span></span>

<span data-ttu-id="b409e-116">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="b409e-116">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="b409e-117">Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="b409e-117">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="b409e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b409e-118">Remarks</span></span>

<span data-ttu-id="b409e-119">Una finestra deve usare questa notifica per arrestare l'elaborazione dei messaggi successivi e per avviare le operazioni di pulizia necessarie per la perdita del puntatore.</span><span class="sxs-lookup"><span data-stu-id="b409e-119">A window should use this notification to stop processing subsequent messages and initiate any cleanup required for the pointer being lost.</span></span> <span data-ttu-id="b409e-120">Anche l'elaborazione dei movimenti associati al puntatore deve essere terminata (ad esempio chiamando [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) e i contatti rimanenti vengono nuovamente associati alla finestra.</span><span class="sxs-lookup"><span data-stu-id="b409e-120">Processing of gestures associated with the pointer should also be terminated (for example, by calling [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) and remaining contacts re-associated with the window.</span></span>

<span data-ttu-id="b409e-121">In genere, se una finestra riceve la notifica **WM_POINTERCAPTURECHANGED** , non vengono ricevute notifiche successive relative al puntatore di input.</span><span class="sxs-lookup"><span data-stu-id="b409e-121">Typically, if a window receives the **WM_POINTERCAPTURECHANGED** notification, no subsequent notifications related to the input pointer are received.</span></span> <span data-ttu-id="b409e-122">Per questo motivo, non dipendere da notifiche associate, ad esempio [**WM_POINTERENTER**](wm-pointerenter.md) e [**WM_POINTERLEAVE**](wm-pointerleave.md).</span><span class="sxs-lookup"><span data-stu-id="b409e-122">Because of this, do not depend on paired notifications such as [**WM_POINTERENTER**](wm-pointerenter.md) and [**WM_POINTERLEAVE**](wm-pointerleave.md).</span></span>

<span data-ttu-id="b409e-123">**WM_POINTERCAPTURECHANGED** non include i dati [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="b409e-123">**WM_POINTERCAPTURECHANGED** does not include [**POINTER_INFO**](/previous-versions/windows/desktop/api) data.</span></span> <span data-ttu-id="b409e-124">Oltre al flag di [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) impostato, i dati restituiti da [**GetPointerInfo**](/previous-versions/windows/desktop/api) (o qualsiasi variante) sono identici a quelli restituiti prima della notifica.</span><span class="sxs-lookup"><span data-stu-id="b409e-124">Other than the [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) flag being set, the data returned by [**GetPointerInfo**](/previous-versions/windows/desktop/api) (or any variant) is identical to that returned prior to the notification.</span></span>

<span data-ttu-id="b409e-125">Se l'applicazione non elabora questa notifica, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) può generare uno o più messaggi di [**WM_GESTURE**](../wintouch/wm-gesture.md) o, se non viene riconosciuto un movimento, **DefWindowProc** può generare un input del mouse.</span><span class="sxs-lookup"><span data-stu-id="b409e-125">If the application does not process this notification, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages or, if a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="b409e-126">Se un'applicazione usa selettivamente un input del puntatore e passa il resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), il comportamento risultante non è definito.</span><span class="sxs-lookup"><span data-stu-id="b409e-126">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="b409e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b409e-127">Requirements</span></span>



| <span data-ttu-id="b409e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b409e-128">Requirement</span></span> | <span data-ttu-id="b409e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b409e-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b409e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b409e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b409e-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b409e-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="b409e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b409e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b409e-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b409e-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b409e-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b409e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b409e-135"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b409e-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b409e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b409e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b409e-137">Messaggi</span><span class="sxs-lookup"><span data-stu-id="b409e-137">Messages</span></span>](messages.md)
</dt> </dl>

 

