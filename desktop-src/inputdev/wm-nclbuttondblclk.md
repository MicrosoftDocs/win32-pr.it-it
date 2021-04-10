---
title: Messaggio WM_NCLBUTTONDBLCLK (winuser. h)
description: Inviato quando l'utente fa doppio clic con il pulsante sinistro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.
ms.assetid: fc655631-64d0-4cc5-b85e-25d274182994
keywords:
- Input della tastiera e del mouse WM_NCLBUTTONDBLCLK messaggio
topic_type:
- apiref
api_name:
- WM_NCLBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db66edcb3b1645c6c34c72e35df53afc516dafc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119503"
---
# <a name="wm_nclbuttondblclk-message"></a><span data-ttu-id="2390e-106">\_Messaggio NCLBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="2390e-106">WM\_NCLBUTTONDBLCLK message</span></span>

<span data-ttu-id="2390e-107">Inviato quando l'utente fa doppio clic con il pulsante sinistro del mouse mentre il cursore si trova all'interno dell'area non client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="2390e-107">Posted when the user double-clicks the left mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="2390e-108">Questo messaggio viene inserito nella finestra che contiene il cursore.</span><span class="sxs-lookup"><span data-stu-id="2390e-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="2390e-109">Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.</span><span class="sxs-lookup"><span data-stu-id="2390e-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="2390e-110">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2390e-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCLBUTTONDBLCLK              0x00A3
```



## <a name="parameters"></a><span data-ttu-id="2390e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="2390e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2390e-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2390e-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2390e-113">Valore di hit test restituito dalla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) come risultato dell'elaborazione del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="2390e-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="2390e-114">Per un elenco dei valori di hit test, vedere **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="2390e-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="2390e-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2390e-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2390e-116">Struttura [**Points**](/previous-versions//dd162808(v=vs.85)) che contiene le coordinate x e y del cursore.</span><span class="sxs-lookup"><span data-stu-id="2390e-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="2390e-117">Le coordinate sono relative all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="2390e-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2390e-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2390e-118">Return value</span></span>

<span data-ttu-id="2390e-119">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="2390e-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2390e-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="2390e-120">Remarks</span></span>

<span data-ttu-id="2390e-121">È anche possibile usare le macro [**get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre i valori delle coordinate X e Y da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2390e-121">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="2390e-122">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="2390e-122">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="2390e-123">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="2390e-123">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="2390e-124">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) verifica il punto specificato per individuare la posizione del cursore ed esegue l'azione appropriata.</span><span class="sxs-lookup"><span data-stu-id="2390e-124">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to find out the location of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="2390e-125">Se appropriato, **DefWindowProc** invia il messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) alla finestra.</span><span class="sxs-lookup"><span data-stu-id="2390e-125">If appropriate, **DefWindowProc** sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="2390e-126">Una finestra non deve avere lo stile **cs \_ DBLCLKS** per ricevere i messaggi **WM \_ NCLBUTTONDBLCLK** .</span><span class="sxs-lookup"><span data-stu-id="2390e-126">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCLBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="2390e-127">Il sistema genera un messaggio **WM \_ NCLBUTTONDBLCLK** quando l'utente preme, rilascia e preme di nuovo il pulsante sinistro del mouse nel limite di tempo doppio clic del sistema.</span><span class="sxs-lookup"><span data-stu-id="2390e-127">The system generates a **WM\_NCLBUTTONDBLCLK** message when the user presses, releases, and again presses the left mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="2390e-128">Se si fa doppio clic con il pulsante sinistro del mouse, vengono effettivamente generati quattro messaggi: [**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM \_ NCLBUTTONUP**](wm-nclbuttonup.md), **WM \_ NCLBUTTONDBLCLK** e **WM \_ NCLBUTTONUP** .</span><span class="sxs-lookup"><span data-stu-id="2390e-128">Double-clicking the left mouse button actually generates four messages: [**WM\_NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM\_NCLBUTTONUP**](wm-nclbuttonup.md), **WM\_NCLBUTTONDBLCLK**, and **WM\_NCLBUTTONUP** again.</span></span>

## <a name="requirements"></a><span data-ttu-id="2390e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2390e-129">Requirements</span></span>



| <span data-ttu-id="2390e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2390e-130">Requirement</span></span> | <span data-ttu-id="2390e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2390e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2390e-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2390e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2390e-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2390e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2390e-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2390e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2390e-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2390e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2390e-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2390e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2390e-137"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2390e-137"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2390e-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2390e-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="2390e-139">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2390e-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2390e-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2390e-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="2390e-141">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="2390e-141">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="2390e-142">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="2390e-142">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="2390e-143">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="2390e-143">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="2390e-144">**\_NCLBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="2390e-144">**WM\_NCLBUTTONDOWN**</span></span>](wm-nclbuttondown.md)
</dt> <dt>

[<span data-ttu-id="2390e-145">**\_NCLBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="2390e-145">**WM\_NCLBUTTONUP**</span></span>](wm-nclbuttonup.md)
</dt> <dt>

[<span data-ttu-id="2390e-146">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="2390e-146">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="2390e-147">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="2390e-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2390e-148">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="2390e-148">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="2390e-149">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="2390e-149">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2390e-150">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="2390e-150">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="2390e-151">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2390e-151">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

