---
description: Il \_ messaggio WM NCPAINT viene inviato a una finestra quando è necessario disegnare il frame.
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: Messaggio WM_NCPAINT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6c2e211f3dc1602821b0197d295f940606c262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880961"
---
# <a name="wm_ncpaint-message"></a><span data-ttu-id="32d38-103">\_Messaggio NCPAINT WM</span><span class="sxs-lookup"><span data-stu-id="32d38-103">WM\_NCPAINT message</span></span>

<span data-ttu-id="32d38-104">Il messaggio **WM \_ NCPAINT** viene inviato a una finestra quando è necessario disegnare il frame.</span><span class="sxs-lookup"><span data-stu-id="32d38-104">The **WM\_NCPAINT** message is sent to a window when its frame must be painted.</span></span>

<span data-ttu-id="32d38-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="32d38-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="32d38-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32d38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32d38-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32d38-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32d38-108">Handle per l'area di aggiornamento della finestra.</span><span class="sxs-lookup"><span data-stu-id="32d38-108">A handle to the update region of the window.</span></span> <span data-ttu-id="32d38-109">L'area di aggiornamento viene ritagliata nella cornice della finestra.</span><span class="sxs-lookup"><span data-stu-id="32d38-109">The update region is clipped to the window frame.</span></span>

</dd> <dt>

<span data-ttu-id="32d38-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32d38-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32d38-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="32d38-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32d38-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32d38-112">Return value</span></span>

<span data-ttu-id="32d38-113">Un'applicazione restituisce zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="32d38-113">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="32d38-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="32d38-114">Remarks</span></span>

<span data-ttu-id="32d38-115">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) disegna la cornice della finestra.</span><span class="sxs-lookup"><span data-stu-id="32d38-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function paints the window frame.</span></span>

<span data-ttu-id="32d38-116">Un'applicazione può intercettare il messaggio **WM \_ NCPAINT** e disegnare la cornice della finestra personalizzata.</span><span class="sxs-lookup"><span data-stu-id="32d38-116">An application can intercept the **WM\_NCPAINT** message and paint its own custom window frame.</span></span> <span data-ttu-id="32d38-117">L'area di ridimensionamento di una finestra è sempre rettangolare, anche se la forma del frame viene modificata.</span><span class="sxs-lookup"><span data-stu-id="32d38-117">The clipping region for a window is always rectangular, even if the shape of the frame is altered.</span></span>

<span data-ttu-id="32d38-118">Il valore *wParam* può essere passato a [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) come nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="32d38-118">The *wParam* value can be passed to [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) as in the following example.</span></span>


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



## <a name="requirements"></a><span data-ttu-id="32d38-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32d38-119">Requirements</span></span>



| <span data-ttu-id="32d38-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="32d38-120">Requirement</span></span> | <span data-ttu-id="32d38-121">Valore</span><span class="sxs-lookup"><span data-stu-id="32d38-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32d38-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32d38-122">Minimum supported client</span></span><br/> | <span data-ttu-id="32d38-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="32d38-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="32d38-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32d38-124">Minimum supported server</span></span><br/> | <span data-ttu-id="32d38-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="32d38-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="32d38-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32d38-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="32d38-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32d38-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32d38-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32d38-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32d38-129">Cenni preliminari su disegno e disegno</span><span class="sxs-lookup"><span data-stu-id="32d38-129">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="32d38-130">Disegno e creazione di messaggi</span><span class="sxs-lookup"><span data-stu-id="32d38-130">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="32d38-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="32d38-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="32d38-132">**GetWindowDC**</span><span class="sxs-lookup"><span data-stu-id="32d38-132">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="32d38-133">**\_disegno WM**</span><span class="sxs-lookup"><span data-stu-id="32d38-133">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> <dt>

[<span data-ttu-id="32d38-134">**GetDCEx**</span><span class="sxs-lookup"><span data-stu-id="32d38-134">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 
