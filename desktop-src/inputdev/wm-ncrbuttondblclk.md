---
title: Messaggio WM_NCRBUTTONDBLCLK (winuser. h)
description: Inviato quando l'utente fa doppio clic con il pulsante destro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.
ms.assetid: 20d62b05-07de-49da-b160-29fa1f5067fa
keywords:
- Input della tastiera e del mouse WM_NCRBUTTONDBLCLK messaggio
topic_type:
- apiref
api_name:
- WM_NCRBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee33d9b31f99a00181427c9a715df792d95fe55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518328"
---
# <a name="wm_ncrbuttondblclk-message"></a><span data-ttu-id="784e6-106">\_Messaggio NCRBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="784e6-106">WM\_NCRBUTTONDBLCLK message</span></span>

<span data-ttu-id="784e6-107">Inviato quando l'utente fa doppio clic con il pulsante destro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="784e6-107">Posted when the user double-clicks the right mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="784e6-108">Questo messaggio viene inserito nella finestra che contiene il cursore.</span><span class="sxs-lookup"><span data-stu-id="784e6-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="784e6-109">Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.</span><span class="sxs-lookup"><span data-stu-id="784e6-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="784e6-110">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="784e6-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCRBUTTONDBLCLK              0x00A6
```



## <a name="parameters"></a><span data-ttu-id="784e6-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="784e6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="784e6-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="784e6-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="784e6-113">Valore di hit test restituito dalla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) come risultato dell'elaborazione del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="784e6-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="784e6-114">Per un elenco dei valori di hit test, vedere **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="784e6-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="784e6-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="784e6-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="784e6-116">Struttura [**Points**](/previous-versions//dd162808(v=vs.85)) che contiene le coordinate x e y del cursore.</span><span class="sxs-lookup"><span data-stu-id="784e6-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="784e6-117">Le coordinate sono relative all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="784e6-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="784e6-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="784e6-118">Return value</span></span>

<span data-ttu-id="784e6-119">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="784e6-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="784e6-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="784e6-120">Remarks</span></span>

<span data-ttu-id="784e6-121">Una finestra non deve avere lo stile **cs \_ DBLCLKS** per ricevere i messaggi **WM \_ NCRBUTTONDBLCLK** .</span><span class="sxs-lookup"><span data-stu-id="784e6-121">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCRBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="784e6-122">Il sistema genera un messaggio **WM \_ NCRBUTTONDBLCLK** quando l'utente preme, rilascia e preme di nuovo il pulsante destro del mouse nel limite di tempo doppio clic del sistema.</span><span class="sxs-lookup"><span data-stu-id="784e6-122">The system generates a **WM\_NCRBUTTONDBLCLK** message when the user presses, releases, and again presses the right mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="784e6-123">Se si fa doppio clic con il pulsante destro del mouse, vengono effettivamente generati quattro messaggi: [**WM \_ NCRBUTTONDOWN**](wm-ncrbuttondown.md), [**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md), **WM \_ NCRBUTTONDBLCLK** e **WM \_ NCRBUTTONUP** .</span><span class="sxs-lookup"><span data-stu-id="784e6-123">Double-clicking the right mouse button actually generates four messages: [**WM\_NCRBUTTONDOWN**](wm-ncrbuttondown.md), [**WM\_NCRBUTTONUP**](wm-ncrbuttonup.md), **WM\_NCRBUTTONDBLCLK**, and **WM\_NCRBUTTONUP** again.</span></span>

<span data-ttu-id="784e6-124">È anche possibile usare le macro [**get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre i valori delle coordinate X e Y da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="784e6-124">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="784e6-125">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="784e6-125">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="784e6-126">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="784e6-126">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="784e6-127">Se è appropriato, il sistema invia il messaggio [**\_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) alla finestra.</span><span class="sxs-lookup"><span data-stu-id="784e6-127">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="784e6-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="784e6-128">Requirements</span></span>



| <span data-ttu-id="784e6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="784e6-129">Requirement</span></span> | <span data-ttu-id="784e6-130">Valore</span><span class="sxs-lookup"><span data-stu-id="784e6-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="784e6-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="784e6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="784e6-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="784e6-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="784e6-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="784e6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="784e6-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="784e6-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="784e6-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="784e6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="784e6-136"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="784e6-136"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="784e6-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="784e6-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="784e6-138">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="784e6-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="784e6-139">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="784e6-139">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="784e6-140">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="784e6-140">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="784e6-141">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="784e6-141">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="784e6-142">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="784e6-142">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="784e6-143">**\_NCRBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="784e6-143">**WM\_NCRBUTTONDOWN**</span></span>](wm-ncrbuttondown.md)
</dt> <dt>

[<span data-ttu-id="784e6-144">**\_NCRBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="784e6-144">**WM\_NCRBUTTONUP**</span></span>](wm-ncrbuttonup.md)
</dt> <dt>

[<span data-ttu-id="784e6-145">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="784e6-145">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="784e6-146">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="784e6-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="784e6-147">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="784e6-147">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="784e6-148">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="784e6-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="784e6-149">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="784e6-149">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="784e6-150">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="784e6-150">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

