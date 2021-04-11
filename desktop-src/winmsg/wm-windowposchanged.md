---
description: Inviato a una finestra la cui dimensione, posizione o posizione nella z order è cambiata in seguito a una chiamata alla funzione SetWindowPos o a un'altra funzione di gestione della finestra.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: Messaggio WM_WINDOWPOSCHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128958"
---
# <a name="wm_windowposchanged-message"></a><span data-ttu-id="c1600-103">\_Messaggio WINDOWPOSCHANGED WM</span><span class="sxs-lookup"><span data-stu-id="c1600-103">WM\_WINDOWPOSCHANGED message</span></span>

<span data-ttu-id="c1600-104">Inviato a una finestra la cui dimensione, posizione o posizione nella z order è cambiata in seguito a una chiamata alla funzione [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) o a un'altra funzione di gestione della finestra.</span><span class="sxs-lookup"><span data-stu-id="c1600-104">Sent to a window whose size, position, or place in the Z order has changed as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="c1600-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c1600-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGED             0x0047
```



## <a name="parameters"></a><span data-ttu-id="c1600-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1600-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1600-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1600-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1600-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="c1600-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c1600-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1600-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1600-110">Puntatore a una struttura [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) che contiene informazioni sulle nuove dimensioni e posizione della finestra.</span><span class="sxs-lookup"><span data-stu-id="c1600-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1600-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1600-111">Return value</span></span>

<span data-ttu-id="c1600-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c1600-112">Type: **LRESULT**</span></span>

<span data-ttu-id="c1600-113">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="c1600-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1600-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1600-114">Remarks</span></span>

<span data-ttu-id="c1600-115">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia i messaggi di [**\_ dimensioni WM**](wm-size.md) e di [**\_ spostamento WM**](wm-move.md) alla finestra.</span><span class="sxs-lookup"><span data-stu-id="c1600-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_SIZE**](wm-size.md) and [**WM\_MOVE**](wm-move.md) messages to the window.</span></span> <span data-ttu-id="c1600-116">I messaggi WM **\_ size** e **WM \_ Move** non vengono inviati se un'applicazione gestisce il messaggio **WM \_ WINDOWPOSCHANGED** senza chiamare **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="c1600-116">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span> <span data-ttu-id="c1600-117">È più efficiente eseguire un'elaborazione delle modifiche di spostamento o di ridimensionamento durante il messaggio **WM \_ WINDOWPOSCHANGED** senza chiamare **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="c1600-117">It is more efficient to perform any move or size change processing during the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1600-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1600-118">Requirements</span></span>



| <span data-ttu-id="c1600-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1600-119">Requirement</span></span> | <span data-ttu-id="c1600-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c1600-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1600-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1600-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c1600-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c1600-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c1600-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1600-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c1600-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c1600-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c1600-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1600-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1600-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1600-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1600-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1600-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1600-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c1600-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c1600-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c1600-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c1600-130">**EndDeferWindowPos**</span><span class="sxs-lookup"><span data-stu-id="c1600-130">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="c1600-131">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="c1600-131">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="c1600-132">**WINDOWPOS**</span><span class="sxs-lookup"><span data-stu-id="c1600-132">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="c1600-133">**\_spostamento WM**</span><span class="sxs-lookup"><span data-stu-id="c1600-133">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="c1600-134">**\_dimensioni WM**</span><span class="sxs-lookup"><span data-stu-id="c1600-134">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="c1600-135">**\_WINDOWPOSCHANGING WM**</span><span class="sxs-lookup"><span data-stu-id="c1600-135">**WM\_WINDOWPOSCHANGING**</span></span>](wm-windowposchanging.md)
</dt> <dt>

<span data-ttu-id="c1600-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c1600-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c1600-137">Windows</span><span class="sxs-lookup"><span data-stu-id="c1600-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
