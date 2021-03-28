---
description: Il \_ messaggio WM DISPLAYCHANGE viene inviato a tutte le finestre quando la risoluzione dello schermo è cambiata.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: Messaggio WM_DISPLAYCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227136"
---
# <a name="wm_displaychange-message"></a><span data-ttu-id="488e2-103">\_Messaggio DISPLAYCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="488e2-103">WM\_DISPLAYCHANGE message</span></span>

<span data-ttu-id="488e2-104">Il messaggio **WM \_ DISPLAYCHANGE** viene inviato a tutte le finestre quando la risoluzione dello schermo è cambiata.</span><span class="sxs-lookup"><span data-stu-id="488e2-104">The **WM\_DISPLAYCHANGE** message is sent to all windows when the display resolution has changed.</span></span>

<span data-ttu-id="488e2-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="488e2-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="488e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="488e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="488e2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="488e2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="488e2-108">Nuova profondità dell'immagine dello schermo, in bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="488e2-108">The new image depth of the display, in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="488e2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="488e2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="488e2-110">La parola di ordine inferiore specifica la risoluzione orizzontale dello schermo.</span><span class="sxs-lookup"><span data-stu-id="488e2-110">The low-order word specifies the horizontal resolution of the screen.</span></span>

<span data-ttu-id="488e2-111">La parola di ordine superiore specifica la risoluzione verticale dello schermo.</span><span class="sxs-lookup"><span data-stu-id="488e2-111">The high-order word specifies the vertical resolution of the screen.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="488e2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="488e2-112">Remarks</span></span>

<span data-ttu-id="488e2-113">Questo messaggio viene inviato solo alle finestre di primo livello.</span><span class="sxs-lookup"><span data-stu-id="488e2-113">This message is only sent to top-level windows.</span></span> <span data-ttu-id="488e2-114">Per tutte le altre finestre pubblicate.</span><span class="sxs-lookup"><span data-stu-id="488e2-114">For all other windows it is posted.</span></span>

## <a name="requirements"></a><span data-ttu-id="488e2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="488e2-115">Requirements</span></span>



| <span data-ttu-id="488e2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="488e2-116">Requirement</span></span> | <span data-ttu-id="488e2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="488e2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="488e2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="488e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="488e2-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="488e2-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="488e2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="488e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="488e2-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="488e2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="488e2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="488e2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="488e2-123"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="488e2-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="488e2-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="488e2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="488e2-125">Cenni preliminari su disegno e disegno</span><span class="sxs-lookup"><span data-stu-id="488e2-125">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="488e2-126">Disegno e creazione di messaggi</span><span class="sxs-lookup"><span data-stu-id="488e2-126">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

<span data-ttu-id="488e2-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="488e2-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="488e2-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="488e2-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

 
