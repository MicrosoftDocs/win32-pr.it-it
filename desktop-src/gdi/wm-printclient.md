---
description: Il \_ messaggio WM PRINTCLIENT viene inviato a una finestra per richiedere che disegni la propria area client nel contesto di dispositivo specificato, in genere in un contesto di dispositivo stampante.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: Messaggio WM_PRINTCLIENT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52aca68695964a35ab9a2c4e309cd71c2e9f7eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980279"
---
# <a name="wm_printclient-message"></a><span data-ttu-id="276b0-103">\_Messaggio PRINTCLIENT WM</span><span class="sxs-lookup"><span data-stu-id="276b0-103">WM\_PRINTCLIENT message</span></span>

<span data-ttu-id="276b0-104">Il messaggio **WM \_ PRINTCLIENT** viene inviato a una finestra per richiedere che disegni la propria area client nel contesto di dispositivo specificato, in genere in un contesto di dispositivo stampante.</span><span class="sxs-lookup"><span data-stu-id="276b0-104">The **WM\_PRINTCLIENT** message is sent to a window to request that it draw its client area in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="276b0-105">A differenza di [**WM \_ Print**](wm-print.md), **WM \_ PRINTCLIENT** non viene elaborato da [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="276b0-105">Unlike [**WM\_PRINT**](wm-print.md), **WM\_PRINTCLIENT** is not processed by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="276b0-106">Una finestra deve elaborare il messaggio **WM \_ PRINTCLIENT** tramite una funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) definita dall'applicazione affinché venga utilizzata correttamente.</span><span class="sxs-lookup"><span data-stu-id="276b0-106">A window should process the **WM\_PRINTCLIENT** message through an application-defined [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function for it to be used properly.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="276b0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="276b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="276b0-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="276b0-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="276b0-109">Handle per il contesto di dispositivo da creare.</span><span class="sxs-lookup"><span data-stu-id="276b0-109">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="276b0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="276b0-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="276b0-111">Opzioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="276b0-111">The drawing options.</span></span> <span data-ttu-id="276b0-112">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="276b0-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="276b0-113">Valore</span><span class="sxs-lookup"><span data-stu-id="276b0-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="276b0-114">Significato</span><span class="sxs-lookup"><span data-stu-id="276b0-114">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="276b0-115"><dt>**\_CHECKVISIBLE PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="276b0-115"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="276b0-116">Disegna la finestra solo se è visibile.</span><span class="sxs-lookup"><span data-stu-id="276b0-116">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="276b0-117"><dt>**\_elementi figlio PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="276b0-117"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="276b0-118">Disegna tutte le finestre figlio visibili.</span><span class="sxs-lookup"><span data-stu-id="276b0-118">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="276b0-119"><dt>**\_client PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="276b0-119"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="276b0-120">Disegna l'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="276b0-120">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="276b0-121"><dt>**\_ERASEBKGND PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="276b0-121"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="276b0-122">Cancella lo sfondo prima di disegnare la finestra.</span><span class="sxs-lookup"><span data-stu-id="276b0-122">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="276b0-123"><dt>**non \_ client PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="276b0-123"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="276b0-124">Disegna l'area non client della finestra.</span><span class="sxs-lookup"><span data-stu-id="276b0-124">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="276b0-125"><dt>**\_Proprietà PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="276b0-125"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="276b0-126">Disegna tutte le finestre di proprietà.</span><span class="sxs-lookup"><span data-stu-id="276b0-126">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="276b0-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="276b0-127">Remarks</span></span>

<span data-ttu-id="276b0-128">Una finestra può elaborare questo messaggio in modo molto simile a [**WM \_ Paint**](./wm-paint.md), ad eccezione del fatto che non è necessario chiamare [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) (viene fornito un contesto di dispositivo) e la finestra deve disegnare l'intera area client anziché solo l'area non valida.</span><span class="sxs-lookup"><span data-stu-id="276b0-128">A window can process this message in much the same manner as [**WM\_PAINT**](./wm-paint.md), except that [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) need not be called (a device context is provided), and the window should draw its entire client area rather than just the invalid region.</span></span>

<span data-ttu-id="276b0-129">Windows che può essere utilizzato in qualsiasi punto del sistema, ad esempio i controlli, deve elaborare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="276b0-129">Windows that can be used anywhere in the system, such as controls, should process this message.</span></span> <span data-ttu-id="276b0-130">È probabilmente utile per altre finestre elaborare anche questo messaggio perché è relativamente semplice da implementare.</span><span class="sxs-lookup"><span data-stu-id="276b0-130">It is probably worthwhile for other windows to process this message as well because it is relatively easy to implement.</span></span>

<span data-ttu-id="276b0-131">La funzione [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) richiede che la finestra animata implementi il messaggio **WM \_ PRINTCLIENT** .</span><span class="sxs-lookup"><span data-stu-id="276b0-131">The [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) function requires that the window being animated implements the **WM\_PRINTCLIENT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="276b0-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="276b0-132">Requirements</span></span>



| <span data-ttu-id="276b0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="276b0-133">Requirement</span></span> | <span data-ttu-id="276b0-134">Valore</span><span class="sxs-lookup"><span data-stu-id="276b0-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="276b0-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="276b0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="276b0-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="276b0-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="276b0-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="276b0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="276b0-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="276b0-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="276b0-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="276b0-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="276b0-140"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="276b0-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="276b0-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="276b0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="276b0-142">Cenni preliminari su disegno e disegno</span><span class="sxs-lookup"><span data-stu-id="276b0-142">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="276b0-143">Disegno e creazione di messaggi</span><span class="sxs-lookup"><span data-stu-id="276b0-143">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="276b0-144">**AnimateWindow**</span><span class="sxs-lookup"><span data-stu-id="276b0-144">**AnimateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[<span data-ttu-id="276b0-145">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="276b0-145">**BeginPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="276b0-146">**EndPaint**</span><span class="sxs-lookup"><span data-stu-id="276b0-146">**EndPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[<span data-ttu-id="276b0-147">**\_disegno WM**</span><span class="sxs-lookup"><span data-stu-id="276b0-147">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
