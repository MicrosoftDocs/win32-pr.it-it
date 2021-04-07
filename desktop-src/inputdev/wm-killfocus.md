---
title: Messaggio WM_KILLFOCUS (winuser. h)
description: Inviato a una finestra immediatamente prima che perda lo stato attivo della tastiera.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- Input della tastiera e del mouse WM_KILLFOCUS messaggio
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e3bba54f2cdb500ba2ba691ffd30419d5beff1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048227"
---
# <a name="wm_killfocus-message"></a><span data-ttu-id="a9d30-104">\_Messaggio KILLFOCUS WM</span><span class="sxs-lookup"><span data-stu-id="a9d30-104">WM\_KILLFOCUS message</span></span>

<span data-ttu-id="a9d30-105">Inviato a una finestra immediatamente prima che perda lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="a9d30-105">Sent to a window immediately before it loses the keyboard focus.</span></span>


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a><span data-ttu-id="a9d30-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9d30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9d30-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9d30-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9d30-108">Handle per la finestra che riceve lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="a9d30-108">A handle to the window that receives the keyboard focus.</span></span> <span data-ttu-id="a9d30-109">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a9d30-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9d30-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9d30-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9d30-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="a9d30-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9d30-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9d30-112">Return value</span></span>

<span data-ttu-id="a9d30-113">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a9d30-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9d30-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9d30-114">Remarks</span></span>

<span data-ttu-id="a9d30-115">Se in un'applicazione viene visualizzato un accento circonflesso, il punto di inserimento deve essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="a9d30-115">If an application is displaying a caret, the caret should be destroyed at this point.</span></span>

<span data-ttu-id="a9d30-116">Durante l'elaborazione di questo messaggio, non eseguire chiamate di funzione che visualizzano o attivano una finestra.</span><span class="sxs-lookup"><span data-stu-id="a9d30-116">While processing this message, do not make any function calls that display or activate a window.</span></span> <span data-ttu-id="a9d30-117">In questo modo il thread genera il controllo e può causare l'interruzione della risposta dei messaggi da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a9d30-117">This causes the thread to yield control and can cause the application to stop responding to messages.</span></span> <span data-ttu-id="a9d30-118">Per ulteriori informazioni, vedere [deadlock dei messaggi](/windows/desktop/winmsg/about-messages-and-message-queues).</span><span class="sxs-lookup"><span data-stu-id="a9d30-118">For more information, see [Message Deadlocks](/windows/desktop/winmsg/about-messages-and-message-queues).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d30-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9d30-119">Requirements</span></span>



| <span data-ttu-id="a9d30-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9d30-120">Requirement</span></span> | <span data-ttu-id="a9d30-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a9d30-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d30-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9d30-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a9d30-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9d30-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a9d30-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9d30-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a9d30-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9d30-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9d30-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9d30-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9d30-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9d30-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d30-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9d30-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="a9d30-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a9d30-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a9d30-130">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="a9d30-130">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="a9d30-131">**\_stato attivo WM**</span><span class="sxs-lookup"><span data-stu-id="a9d30-131">**WM\_SETFOCUS**</span></span>](wm-setfocus.md)
</dt> <dt>

<span data-ttu-id="a9d30-132">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a9d30-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a9d30-133">Input da tastiera</span><span class="sxs-lookup"><span data-stu-id="a9d30-133">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

