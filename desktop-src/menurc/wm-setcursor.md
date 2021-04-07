---
title: Messaggio WM_SETCURSOR (winuser. h)
description: Inviato a una finestra se il mouse determina lo spostamento del cursore all'interno di una finestra e l'input del mouse non viene acquisito.
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- Menu del messaggio WM_SETCURSOR e altre risorse
topic_type:
- apiref
api_name:
- WM_SETCURSOR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e941919b447659e67fdcdd9e4e5f4ff2630f8bf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048452"
---
# <a name="wm_setcursor-message"></a><span data-ttu-id="9b000-104">\_Messaggio di cursore WM</span><span class="sxs-lookup"><span data-stu-id="9b000-104">WM\_SETCURSOR message</span></span>

<span data-ttu-id="9b000-105">Inviato a una finestra se il mouse determina lo spostamento del cursore all'interno di una finestra e l'input del mouse non viene acquisito.</span><span class="sxs-lookup"><span data-stu-id="9b000-105">Sent to a window if the mouse causes the cursor to move within a window and mouse input is not captured.</span></span>


```C++
#define WM_SETCURSOR                    0x0020
```



## <a name="parameters"></a><span data-ttu-id="9b000-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b000-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b000-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b000-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b000-108">Handle per la finestra che contiene il cursore.</span><span class="sxs-lookup"><span data-stu-id="9b000-108">A handle to the window that contains the cursor.</span></span>

</dd> <dt>

<span data-ttu-id="9b000-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b000-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b000-110">La parola di ordine inferiore di *lParam* specifica il risultato dell'hit test per la posizione del cursore.</span><span class="sxs-lookup"><span data-stu-id="9b000-110">The low-order word of *lParam* specifies the hit-test result for the cursor position.</span></span> <span data-ttu-id="9b000-111">Per i valori possibili, vedere i valori restituiti per [WM_NCHITTEST](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="9b000-111">See the return values for [WM_NCHITTEST](../inputdev/wm-nchittest.md) for possible values.</span></span>

<span data-ttu-id="9b000-112">La parola più ordinata di *lParam* specifica il messaggio della finestra del mouse che ha generato l'evento, ad esempio [WM_MOUSEMOVE](../inputdev/wm-mousemove.md).</span><span class="sxs-lookup"><span data-stu-id="9b000-112">The high-order word of *lParam* specifies the mouse window message which triggered this event, such as [WM_MOUSEMOVE](../inputdev/wm-mousemove.md).</span></span> <span data-ttu-id="9b000-113">Quando la finestra entra in modalità menu, questo valore è zero.</span><span class="sxs-lookup"><span data-stu-id="9b000-113">When the window enters menu mode, this value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b000-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b000-114">Return value</span></span>

<span data-ttu-id="9b000-115">Se un'applicazione elabora il messaggio, deve restituire **true** per arrestare l'ulteriore elaborazione o **false** per continuare.</span><span class="sxs-lookup"><span data-stu-id="9b000-115">If an application processes this message, it should return **TRUE** to halt further processing or **FALSE** to continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b000-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b000-116">Remarks</span></span>

<span data-ttu-id="9b000-117">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) passa il messaggio del **\_ cursore WM** a una finestra padre prima dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="9b000-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) function passes the **WM\_SETCURSOR** message to a parent window before processing.</span></span> <span data-ttu-id="9b000-118">Se la finestra padre restituisce **true**, l'ulteriore elaborazione viene interrotta.</span><span class="sxs-lookup"><span data-stu-id="9b000-118">If the parent window returns **TRUE**, further processing is halted.</span></span> <span data-ttu-id="9b000-119">Se si passa il messaggio alla finestra padre di una finestra, il controllo della finestra padre viene posizionato sull'impostazione del cursore in una finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="9b000-119">Passing the message to a window's parent window gives the parent window control over the cursor's setting in a child window.</span></span> <span data-ttu-id="9b000-120">La funzione **DefWindowProc** utilizza inoltre questo messaggio per impostare il cursore su una freccia se non è presente nell'area client o sul cursore della classe registrata se si trova nell'area client.</span><span class="sxs-lookup"><span data-stu-id="9b000-120">The **DefWindowProc** function also uses this message to set the cursor to an arrow if it is not in the client area, or to the registered class cursor if it is in the client area.</span></span> <span data-ttu-id="9b000-121">Se la parola di ordine inferiore del parametro *lParam* è **HTERROR** e la parola più significativa di *lParam* specifica che uno dei pulsanti del mouse è premuto, **DefWindowProc** chiama la funzione [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) .</span><span class="sxs-lookup"><span data-stu-id="9b000-121">If the low-order word of the *lParam* parameter is **HTERROR** and the high-order word of *lParam* specifies that one of the mouse buttons is pressed, **DefWindowProc** calls the [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b000-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b000-122">Requirements</span></span>



| <span data-ttu-id="9b000-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b000-123">Requirement</span></span> | <span data-ttu-id="9b000-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9b000-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b000-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b000-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9b000-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9b000-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9b000-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b000-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9b000-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9b000-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9b000-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b000-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b000-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b000-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b000-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b000-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="9b000-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="9b000-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9b000-133">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="9b000-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

<span data-ttu-id="9b000-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9b000-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9b000-135">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9b000-135">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9b000-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="9b000-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9b000-137">Cursori</span><span class="sxs-lookup"><span data-stu-id="9b000-137">Cursors</span></span>](cursors.md)
</dt> </dl>

 

