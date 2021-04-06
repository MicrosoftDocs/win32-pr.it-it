---
description: Inviato a una finestra la cui dimensione, posizione o posizione nella z order sta per essere modificata in seguito a una chiamata alla funzione SetWindowPos o a un'altra funzione di gestione della finestra.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: Messaggio WM_WINDOWPOSCHANGING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015a31aac31d38506d1798f83c8dd7f9aa646f85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758462"
---
# <a name="wm_windowposchanging-message"></a><span data-ttu-id="a996f-103">\_Messaggio WINDOWPOSCHANGING WM</span><span class="sxs-lookup"><span data-stu-id="a996f-103">WM\_WINDOWPOSCHANGING message</span></span>

<span data-ttu-id="a996f-104">Inviato a una finestra la cui dimensione, posizione o posizione nella z order sta per essere modificata in seguito a una chiamata alla funzione [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) o a un'altra funzione di gestione della finestra.</span><span class="sxs-lookup"><span data-stu-id="a996f-104">Sent to a window whose size, position, or place in the Z order is about to change as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="a996f-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a996f-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGING            0x0046
```



## <a name="parameters"></a><span data-ttu-id="a996f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a996f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a996f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a996f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a996f-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="a996f-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a996f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a996f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a996f-110">Puntatore a una struttura [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) che contiene informazioni sulle nuove dimensioni e posizione della finestra.</span><span class="sxs-lookup"><span data-stu-id="a996f-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a996f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a996f-111">Return value</span></span>

<span data-ttu-id="a996f-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="a996f-112">Type: **LRESULT**</span></span>

<span data-ttu-id="a996f-113">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="a996f-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a996f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a996f-114">Remarks</span></span>

<span data-ttu-id="a996f-115">Per una finestra con lo [**stile \_ WS Overlapped**](window-styles.md) o **WS \_ THICKFRAME** , la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia il messaggio [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) alla finestra.</span><span class="sxs-lookup"><span data-stu-id="a996f-115">For a window with the [**WS\_OVERLAPPED**](window-styles.md) or **WS\_THICKFRAME** style, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_GETMINMAXINFO**](wm-getminmaxinfo.md) message to the window.</span></span> <span data-ttu-id="a996f-116">Questa operazione viene eseguita per convalidare le nuove dimensioni e la nuova posizione della finestra e per applicare gli stili del client [cs \_ BYTEALIGNCLIENT](about-window-classes.md) e cs \_ BYTEALIGNWINDOW.</span><span class="sxs-lookup"><span data-stu-id="a996f-116">This is done to validate the new size and position of the window and to enforce the [CS\_BYTEALIGNCLIENT](about-window-classes.md) and CS\_BYTEALIGNWINDOW client styles.</span></span> <span data-ttu-id="a996f-117">Se non si passa il messaggio **WM \_ WINDOWPOSCHANGING** alla funzione **DefWindowProc** , un'applicazione può eseguire l'override di queste impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="a996f-117">By not passing the **WM\_WINDOWPOSCHANGING** message to the **DefWindowProc** function, an application can override these defaults.</span></span>

<span data-ttu-id="a996f-118">Durante l'elaborazione di questo messaggio, la modifica di uno dei valori di [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) influiscono sulla nuova dimensione, posizione o posizione della finestra nella z order.</span><span class="sxs-lookup"><span data-stu-id="a996f-118">While this message is being processed, modifying any of the values in [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) affects the window's new size, position, or place in the Z order.</span></span> <span data-ttu-id="a996f-119">Un'applicazione può impedire modifiche alla finestra impostando o deselezionando i bit appropriati nel membro **Flags** di **WINDOWPOS**.</span><span class="sxs-lookup"><span data-stu-id="a996f-119">An application can prevent changes to the window by setting or clearing the appropriate bits in the **flags** member of **WINDOWPOS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a996f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a996f-120">Requirements</span></span>



| <span data-ttu-id="a996f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a996f-121">Requirement</span></span> | <span data-ttu-id="a996f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a996f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a996f-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a996f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a996f-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a996f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a996f-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a996f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a996f-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a996f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a996f-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a996f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a996f-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a996f-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a996f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a996f-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="a996f-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a996f-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a996f-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="a996f-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="a996f-132">**EndDeferWindowPos**</span><span class="sxs-lookup"><span data-stu-id="a996f-132">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="a996f-133">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="a996f-133">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="a996f-134">**WINDOWPOS**</span><span class="sxs-lookup"><span data-stu-id="a996f-134">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="a996f-135">**\_GETMINMAXINFO WM**</span><span class="sxs-lookup"><span data-stu-id="a996f-135">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md)
</dt> <dt>

[<span data-ttu-id="a996f-136">**\_spostamento WM**</span><span class="sxs-lookup"><span data-stu-id="a996f-136">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="a996f-137">**\_dimensioni WM**</span><span class="sxs-lookup"><span data-stu-id="a996f-137">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="a996f-138">**\_WINDOWPOSCHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="a996f-138">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="a996f-139">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="a996f-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a996f-140">Windows</span><span class="sxs-lookup"><span data-stu-id="a996f-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
