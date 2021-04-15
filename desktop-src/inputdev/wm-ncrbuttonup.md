---
title: Messaggio WM_NCRBUTTONUP (winuser. h)
description: Inviato quando l'utente rilascia il pulsante destro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.
ms.assetid: dc77c235-9e57-4051-b197-bd7ee7535a6f
keywords:
- Input della tastiera e del mouse WM_NCRBUTTONUP messaggio
topic_type:
- apiref
api_name:
- WM_NCRBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5fb977e442b2af312f9267576c622ddd35022fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477956"
---
# <a name="wm_ncrbuttonup-message"></a><span data-ttu-id="077c6-106">\_Messaggio NCRBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="077c6-106">WM\_NCRBUTTONUP message</span></span>

<span data-ttu-id="077c6-107">Inviato quando l'utente rilascia il pulsante destro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="077c6-107">Posted when the user releases the right mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="077c6-108">Questo messaggio viene inserito nella finestra che contiene il cursore.</span><span class="sxs-lookup"><span data-stu-id="077c6-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="077c6-109">Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.</span><span class="sxs-lookup"><span data-stu-id="077c6-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="077c6-110">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="077c6-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCRBUTTONUP                  0x00A5
```



## <a name="parameters"></a><span data-ttu-id="077c6-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="077c6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="077c6-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="077c6-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="077c6-113">Valore di hit test restituito dalla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) come risultato dell'elaborazione del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="077c6-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="077c6-114">Per un elenco dei valori di hit test, vedere **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="077c6-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="077c6-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="077c6-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="077c6-116">Struttura [**Points**](/previous-versions//dd162808(v=vs.85)) che contiene le coordinate x e y del cursore.</span><span class="sxs-lookup"><span data-stu-id="077c6-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="077c6-117">Le coordinate sono relative all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="077c6-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="077c6-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="077c6-118">Return value</span></span>

<span data-ttu-id="077c6-119">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="077c6-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="077c6-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="077c6-120">Remarks</span></span>

<span data-ttu-id="077c6-121">È anche possibile usare le macro [**get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre i valori delle coordinate X e Y da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="077c6-121">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="077c6-122">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="077c6-122">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="077c6-123">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="077c6-123">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="077c6-124">Se è appropriato, il sistema invia il messaggio [**\_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) alla finestra.</span><span class="sxs-lookup"><span data-stu-id="077c6-124">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="077c6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="077c6-125">Requirements</span></span>



| <span data-ttu-id="077c6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="077c6-126">Requirement</span></span> | <span data-ttu-id="077c6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="077c6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="077c6-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="077c6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="077c6-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="077c6-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="077c6-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="077c6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="077c6-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="077c6-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="077c6-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="077c6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="077c6-133"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="077c6-133"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="077c6-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="077c6-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="077c6-135">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="077c6-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="077c6-136">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="077c6-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="077c6-137">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="077c6-137">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="077c6-138">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="077c6-138">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="077c6-139">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="077c6-139">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="077c6-140">**\_NCRBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="077c6-140">**WM\_NCRBUTTONDBLCLK**</span></span>](wm-ncrbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="077c6-141">**\_NCRBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="077c6-141">**WM\_NCRBUTTONDOWN**</span></span>](wm-ncrbuttondown.md)
</dt> <dt>

[<span data-ttu-id="077c6-142">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="077c6-142">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="077c6-143">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="077c6-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="077c6-144">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="077c6-144">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="077c6-145">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="077c6-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="077c6-146">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="077c6-146">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="077c6-147">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="077c6-147">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

