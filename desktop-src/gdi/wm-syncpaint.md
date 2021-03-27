---
description: Il \_ messaggio WM SYNCPAINT viene usato per sincronizzare il disegno evitando il collegamento di thread GUI indipendenti.
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: Messaggio WM_SYNCPAINT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994549"
---
# <a name="wm_syncpaint-message"></a><span data-ttu-id="dcc4a-103">\_Messaggio SYNCPAINT WM</span><span class="sxs-lookup"><span data-stu-id="dcc4a-103">WM\_SYNCPAINT message</span></span>

<span data-ttu-id="dcc4a-104">Il messaggio **WM \_ SYNCPAINT** viene usato per sincronizzare il disegno evitando il collegamento di thread GUI indipendenti.</span><span class="sxs-lookup"><span data-stu-id="dcc4a-104">The **WM\_SYNCPAINT** message is used to synchronize painting while avoiding linking independent GUI threads.</span></span>

<span data-ttu-id="dcc4a-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dcc4a-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="dcc4a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcc4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcc4a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dcc4a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dcc4a-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="dcc4a-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dcc4a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dcc4a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dcc4a-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="dcc4a-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcc4a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcc4a-111">Return value</span></span>

<span data-ttu-id="dcc4a-112">Un'applicazione restituisce zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="dcc4a-112">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcc4a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="dcc4a-113">Remarks</span></span>

<span data-ttu-id="dcc4a-114">Quando una finestra è stata nascosta, mostrata, spostata o ridimensionata, il sistema può determinare che è necessario inviare un messaggio **WM \_ SYNCPAINT** alle finestre di primo livello di altri thread.</span><span class="sxs-lookup"><span data-stu-id="dcc4a-114">When a window has been hidden, shown, moved, or sized, the system may determine that it is necessary to send a **WM\_SYNCPAINT** message to the top-level windows of other threads.</span></span> <span data-ttu-id="dcc4a-115">Le applicazioni devono passare **WM \_ SYNCPAINT** a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  per l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="dcc4a-115">Applications must pass **WM\_SYNCPAINT** to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  for processing.</span></span> <span data-ttu-id="dcc4a-116">La funzione **DefWindowProc** invierà un messaggio [**WM \_ NCPAINT**](wm-ncpaint.md) alla routine della finestra se la cornice della finestra deve essere disegnata e invierà un messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) se lo sfondo della finestra deve essere cancellato.</span><span class="sxs-lookup"><span data-stu-id="dcc4a-116">The **DefWindowProc** function will send a [**WM\_NCPAINT**](wm-ncpaint.md) message to the window procedure if the window frame must be painted and send a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message if the window background must be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcc4a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcc4a-117">Requirements</span></span>



| <span data-ttu-id="dcc4a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcc4a-118">Requirement</span></span> | <span data-ttu-id="dcc4a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="dcc4a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc4a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcc4a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dcc4a-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dcc4a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dcc4a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcc4a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dcc4a-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dcc4a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dcc4a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcc4a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcc4a-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dcc4a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcc4a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcc4a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc4a-127">Cenni preliminari su disegno e disegno</span><span class="sxs-lookup"><span data-stu-id="dcc4a-127">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="dcc4a-128">Disegno e creazione di messaggi</span><span class="sxs-lookup"><span data-stu-id="dcc4a-128">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="dcc4a-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="dcc4a-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="dcc4a-130">**GetDCEx**</span><span class="sxs-lookup"><span data-stu-id="dcc4a-130">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[<span data-ttu-id="dcc4a-131">**GetWindowDC**</span><span class="sxs-lookup"><span data-stu-id="dcc4a-131">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="dcc4a-132">**\_disegno WM**</span><span class="sxs-lookup"><span data-stu-id="dcc4a-132">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
