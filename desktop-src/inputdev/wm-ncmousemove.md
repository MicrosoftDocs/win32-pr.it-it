---
title: Messaggio WM_NCMOUSEMOVE (winuser. h)
description: Inserito in una finestra quando il cursore viene spostato all'interno dell'area non client della finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.
ms.assetid: 49c7cde9-701c-4821-8d16-31ca3c016ed4
keywords:
- Input della tastiera e del mouse WM_NCMOUSEMOVE messaggio
topic_type:
- apiref
api_name:
- WM_NCMOUSEMOVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65461d2e84b6185b95ac05c071f31df680450e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479180"
---
# <a name="wm_ncmousemove-message"></a><span data-ttu-id="10900-106">\_Messaggio NCMOUSEMOVE WM</span><span class="sxs-lookup"><span data-stu-id="10900-106">WM\_NCMOUSEMOVE message</span></span>

<span data-ttu-id="10900-107">Inserito in una finestra quando il cursore viene spostato all'interno dell'area non client della finestra.</span><span class="sxs-lookup"><span data-stu-id="10900-107">Posted to a window when the cursor is moved within the nonclient area of the window.</span></span> <span data-ttu-id="10900-108">Questo messaggio viene inserito nella finestra che contiene il cursore.</span><span class="sxs-lookup"><span data-stu-id="10900-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="10900-109">Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.</span><span class="sxs-lookup"><span data-stu-id="10900-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="10900-110">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="10900-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSEMOVE                  0x00A0
```



## <a name="parameters"></a><span data-ttu-id="10900-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="10900-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10900-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10900-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10900-113">Valore di hit test restituito dalla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) come risultato dell'elaborazione del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="10900-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="10900-114">Per un elenco dei valori di hit test, vedere **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="10900-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="10900-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10900-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10900-116">Struttura [**Points**](/previous-versions//dd162808(v=vs.85)) che contiene le coordinate x e y del cursore.</span><span class="sxs-lookup"><span data-stu-id="10900-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="10900-117">Le coordinate sono relative all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="10900-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10900-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10900-118">Return value</span></span>

<span data-ttu-id="10900-119">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="10900-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="10900-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="10900-120">Remarks</span></span>

<span data-ttu-id="10900-121">Se è appropriato, il sistema invia il messaggio [**\_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) alla finestra.</span><span class="sxs-lookup"><span data-stu-id="10900-121">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="10900-122">È anche possibile usare le macro [**get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre i valori delle coordinate X e Y da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="10900-122">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="10900-123">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="10900-123">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="10900-124">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="10900-124">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="10900-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10900-125">Requirements</span></span>



| <span data-ttu-id="10900-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="10900-126">Requirement</span></span> | <span data-ttu-id="10900-127">Valore</span><span class="sxs-lookup"><span data-stu-id="10900-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10900-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10900-128">Minimum supported client</span></span><br/> | <span data-ttu-id="10900-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="10900-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="10900-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10900-130">Minimum supported server</span></span><br/> | <span data-ttu-id="10900-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="10900-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="10900-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10900-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="10900-133"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10900-133"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10900-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10900-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="10900-135">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="10900-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="10900-136">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="10900-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="10900-137">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="10900-137">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="10900-138">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="10900-138">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="10900-139">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="10900-139">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="10900-140">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="10900-140">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="10900-141">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="10900-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="10900-142">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="10900-142">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="10900-143">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="10900-143">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="10900-144">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="10900-144">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="10900-145">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10900-145">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

