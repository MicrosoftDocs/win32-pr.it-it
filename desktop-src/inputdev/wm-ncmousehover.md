---
title: Messaggio WM_NCMOUSEHOVER (winuser. h)
description: Inserito in una finestra quando il cursore passa sull'area non client della finestra per il periodo di tempo specificato in una chiamata precedente a TrackMouseEvent.
ms.assetid: ca1afdc2-7884-445e-b9b7-4d7dd5dcea38
keywords:
- Input della tastiera e del mouse WM_NCMOUSEHOVER messaggio
topic_type:
- apiref
api_name:
- WM_NCMOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde2e70b04602de5936e945789007a6c5fea8542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048678"
---
# <a name="wm_ncmousehover-message"></a><span data-ttu-id="1d7eb-104">\_Messaggio NCMOUSEHOVER WM</span><span class="sxs-lookup"><span data-stu-id="1d7eb-104">WM\_NCMOUSEHOVER message</span></span>

<span data-ttu-id="1d7eb-105">Inserito in una finestra quando il cursore passa sull'area non client della finestra per il periodo di tempo specificato in una chiamata precedente a [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="1d7eb-105">Posted to a window when the cursor hovers over the nonclient area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="1d7eb-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1d7eb-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSEHOVER                 0x02A0
```



## <a name="parameters"></a><span data-ttu-id="1d7eb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d7eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d7eb-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1d7eb-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d7eb-109">Valore di hit test restituito dalla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) come risultato dell'elaborazione del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="1d7eb-109">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="1d7eb-110">Per un elenco dei valori di hit test, vedere **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="1d7eb-110">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="1d7eb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1d7eb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1d7eb-112">Struttura [**Points**](/previous-versions//dd162808(v=vs.85)) che contiene le coordinate x e y del cursore.</span><span class="sxs-lookup"><span data-stu-id="1d7eb-112">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="1d7eb-113">Le coordinate sono relative all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="1d7eb-113">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d7eb-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d7eb-114">Return value</span></span>

<span data-ttu-id="1d7eb-115">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="1d7eb-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d7eb-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d7eb-116">Remarks</span></span>

<span data-ttu-id="1d7eb-117">Il rilevamento del passaggio del mouse si interrompe quando viene generato questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="1d7eb-117">Hover tracking stops when this message is generated.</span></span> <span data-ttu-id="1d7eb-118">Se è necessario tenere traccia del comportamento del passaggio del mouse, l'applicazione deve chiamare nuovamente [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) .</span><span class="sxs-lookup"><span data-stu-id="1d7eb-118">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="1d7eb-119">È anche possibile usare le macro [**get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre i valori delle coordinate X e Y da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="1d7eb-119">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="1d7eb-120">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="1d7eb-120">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="1d7eb-121">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="1d7eb-121">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d7eb-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d7eb-122">Requirements</span></span>



| <span data-ttu-id="1d7eb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d7eb-123">Requirement</span></span> | <span data-ttu-id="1d7eb-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1d7eb-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d7eb-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d7eb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1d7eb-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d7eb-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1d7eb-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d7eb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1d7eb-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d7eb-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1d7eb-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d7eb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d7eb-130"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d7eb-130"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d7eb-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d7eb-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d7eb-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1d7eb-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1d7eb-133">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="1d7eb-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="1d7eb-134">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="1d7eb-134">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="1d7eb-135">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="1d7eb-135">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="1d7eb-136">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="1d7eb-136">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="1d7eb-137">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="1d7eb-137">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="1d7eb-138">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="1d7eb-138">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="1d7eb-139">**\_MOUSEHOVER WM**</span><span class="sxs-lookup"><span data-stu-id="1d7eb-139">**WM\_MOUSEHOVER**</span></span>](wm-mousehover.md)
</dt> <dt>

<span data-ttu-id="1d7eb-140">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1d7eb-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1d7eb-141">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="1d7eb-141">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="1d7eb-142">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="1d7eb-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1d7eb-143">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="1d7eb-143">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="1d7eb-144">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d7eb-144">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

