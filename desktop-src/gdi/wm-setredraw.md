---
description: Si invia il **WM_SETREDRAW** a una finestra per consentire il ridisegno delle modifiche in tale finestra o per impedire il ridisegno delle modifiche in tale finestra.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: WM_SETREDRAW messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1232833fc4465e2341541a0036af47fdd3b53393
ms.sourcegitcommit: e5d6fb49928cc8cea4ec77dce03b740d40076348
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/10/2021
ms.locfileid: "113593457"
---
# <a name="wm_setredraw-message"></a><span data-ttu-id="04f55-103">WM_SETREDRAW messaggio</span><span class="sxs-lookup"><span data-stu-id="04f55-103">WM_SETREDRAW message</span></span>

<span data-ttu-id="04f55-104">Si invia il **messaggio WM \_ SETREDRAW** a una finestra per consentire il ridisegno delle modifiche in tale finestra o per impedire il ridisegno delle modifiche in tale finestra.</span><span class="sxs-lookup"><span data-stu-id="04f55-104">You send the **WM\_SETREDRAW** message to a window to allow changes in that window to be redrawn, or to prevent changes in that window from being redrawn.</span></span>

<span data-ttu-id="04f55-105">Per inviare questo messaggio, chiamare la [**funzione SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="04f55-105">To send this message, call the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>

```C++
SendMessage(
  (HWND) hWnd,
  WM_SETREDRAW,
  (WPARAM) wParam,
  (LPARAM) lParam
);
```

## <a name="parameters"></a><span data-ttu-id="04f55-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04f55-106">Parameters</span></span>

`wParam`

<span data-ttu-id="04f55-107">Stato di ridisegno.</span><span class="sxs-lookup"><span data-stu-id="04f55-107">The redraw state.</span></span> <span data-ttu-id="04f55-108">Se questo parametro è **TRUE,** il contenuto può essere ridisegnato dopo una modifica.</span><span class="sxs-lookup"><span data-stu-id="04f55-108">If this parameter is **TRUE**, then the content can be redrawn after a change.</span></span> <span data-ttu-id="04f55-109">Se questo parametro è **FALSE,** il contenuto non può essere ridisegnato dopo una modifica.</span><span class="sxs-lookup"><span data-stu-id="04f55-109">If this parameter is **FALSE**, then the content can't be redrawn after a change.</span></span>

`lParam`

<span data-ttu-id="04f55-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="04f55-110">This parameter isn't used.</span></span>

## <a name="return-value"></a><span data-ttu-id="04f55-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04f55-111">Return value</span></span>

<span data-ttu-id="04f55-112">L'applicazione deve restituire 0 se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="04f55-112">Your application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="04f55-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="04f55-113">Remarks</span></span>

<span data-ttu-id="04f55-114">Questo messaggio può essere utile se l'applicazione deve aggiungere più elementi a una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="04f55-114">This message can be useful if your application must add several items to a list box.</span></span> <span data-ttu-id="04f55-115">L'applicazione può chiamare questo messaggio con *wParam* impostato su **FALSE,** aggiungere gli elementi e quindi chiamare nuovamente il messaggio con *wParam* impostato su **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="04f55-115">Your application can call this message with *wParam* set to **FALSE**, add the items, and then call the message again with *wParam* set to **TRUE**.</span></span> <span data-ttu-id="04f55-116">Infine, l'applicazione può chiamare [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, \_ RDW ERASE \| RDW \_ FRAME \| RDW \_ INVALIDATE \| RDW \_ ALLCHILDREN) per fare in modo che la casella di riepilogo venga ridisegnata.</span><span class="sxs-lookup"><span data-stu-id="04f55-116">Finally, your application can call [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, RDW\_ERASE \| RDW\_FRAME \| RDW\_INVALIDATE \| RDW\_ALLCHILDREN) to cause the list box to be repainted.</span></span>

> [!NOTE] 
> <span data-ttu-id="04f55-117">È consigliabile usare [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) con i flag specificati, anziché [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), perché il primo è necessario per alcuni controlli che hanno un'area non client o hanno stili di finestra che ne determinano l'applicazione a un'area non client ( ad esempio **WS_THICKFRAME**, **WS_BORDER** o **WS_EX_CLIENTEDGE**).</span><span class="sxs-lookup"><span data-stu-id="04f55-117">You should use [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) with the specified flags, instead of [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), because the former is necessary for some controls that have nonclient area of their own, or have window styles that cause them to be given a nonclient area (such as **WS_THICKFRAME**, **WS_BORDER**, or **WS_EX_CLIENTEDGE**).</span></span> <span data-ttu-id="04f55-118">Se il controllo non ha un'area non client, **RedrawWindow** con questi flag esegue solo l'invalidazione di **InvalidateRect.**</span><span class="sxs-lookup"><span data-stu-id="04f55-118">If the control does not have a nonclient area, then **RedrawWindow** with these flags will do only as much invalidation as **InvalidateRect** would.</span></span>

<span data-ttu-id="04f55-119">Il passaggio **WM_SETREDRAW** messaggio alla funzione **DefWindowProc** rimuove lo stile WS_VISIBLE dalla finestra quando *wParam* è impostato su **FALSE.** </span><span class="sxs-lookup"><span data-stu-id="04f55-119">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function removes the **WS_VISIBLE** style from the window when *wParam* is set to **FALSE**.</span></span> <span data-ttu-id="04f55-120">Anche se il contenuto della finestra rimane visibile sullo schermo, la [**funzione IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) restituisce **FALSE** quando viene chiamato su una finestra in questo stato.</span><span class="sxs-lookup"><span data-stu-id="04f55-120">Although the window content remains visible on screen, the [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) function returns **FALSE** when called on a window in this state.</span></span> 

<span data-ttu-id="04f55-121">Il **passaggio WM_SETREDRAW** messaggio alla funzione **DefWindowProc** aggiunge lo stile **WS_VISIBLE** alla finestra, se non impostato, quando *wParam* è impostato su **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="04f55-121">Passing a **WM_SETREDRAW** message to the **DefWindowProc** function adds the **WS_VISIBLE** style to the window, if not set, when *wParam* is set to **TRUE**.</span></span> <span data-ttu-id="04f55-122">Se l'applicazione invia **WM_SETREDRAW** messaggio con *wParam* impostato su TRUE su **una** finestra nascosta, la finestra diventa visibile.</span><span class="sxs-lookup"><span data-stu-id="04f55-122">If your application sends the **WM_SETREDRAW** message with *wParam* set to **TRUE** to a hidden window, then the window becomes visible.</span></span> 

<span data-ttu-id="04f55-123">**Windows 10 e versioni successive; Windows Server 2016 e versioni successive.**</span><span class="sxs-lookup"><span data-stu-id="04f55-123">**Windows 10 and later; Windows Server 2016 and later**.</span></span> <span data-ttu-id="04f55-124">Il sistema imposta una proprietà denominata *SysSetRedraw* in una finestra la cui routine della finestra passa WM_SETREDRAW **messaggi** a **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="04f55-124">The system sets a property named *SysSetRedraw* on a window whose window procedure passes **WM_SETREDRAW** messages to **DefWindowProc**.</span></span> <span data-ttu-id="04f55-125">È possibile usare la [**funzione GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) per ottenere il valore della proprietà quando è disponibile.</span><span class="sxs-lookup"><span data-stu-id="04f55-125">You can use the [**GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) function to get the property value when it's available.</span></span> <span data-ttu-id="04f55-126">**GetProp** restituisce un valore diverso da zero quando il ridisegno è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="04f55-126">**GetProp** returns a non-zero value when redraw is disabled.</span></span> <span data-ttu-id="04f55-127">**GetProp** restituirà zero quando il ridisegno è abilitato o quando la proprietà della finestra non esiste.</span><span class="sxs-lookup"><span data-stu-id="04f55-127">**GetProp** will return zero when redraw is enabled, or when the window property doesn't exist.</span></span> 

## <a name="requirements"></a><span data-ttu-id="04f55-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04f55-128">Requirements</span></span>

| <span data-ttu-id="04f55-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="04f55-129">Requirement</span></span> | <span data-ttu-id="04f55-130">Valore</span><span class="sxs-lookup"><span data-stu-id="04f55-130">Value</span></span> |
|-|-|
| <span data-ttu-id="04f55-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04f55-131">Minimum supported client</span></span> | <span data-ttu-id="04f55-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="04f55-132">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="04f55-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04f55-133">Minimum supported server</span></span> | <span data-ttu-id="04f55-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="04f55-134">Windows 2000 Server \[desktop apps only\]</span></span> |
| <span data-ttu-id="04f55-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04f55-135">Header</span></span> | <dl><span data-ttu-id="04f55-136"><dt>Winuser.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="04f55-136"><dt>Winuser.h (include Windows.h)</dt></span></span></dl> |

## <a name="see-also"></a><span data-ttu-id="04f55-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04f55-137">See also</span></span>

* [<span data-ttu-id="04f55-138">Panoramica del disegno e del disegno</span><span class="sxs-lookup"><span data-stu-id="04f55-138">Painting and drawing overview</span></span>](painting-and-drawing.md)
* [<span data-ttu-id="04f55-139">Disegnare e disegnare messaggi</span><span class="sxs-lookup"><span data-stu-id="04f55-139">Painting and drawing messages</span></span>](painting-and-drawing-messages.md)
* [<span data-ttu-id="04f55-140">RidisegnaWindow</span><span class="sxs-lookup"><span data-stu-id="04f55-140">RedrawWindow</span></span>](/windows/win32/api/Winuser/nf-winuser-redrawwindow)
