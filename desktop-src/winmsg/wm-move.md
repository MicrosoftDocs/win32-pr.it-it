---
description: Inviato dopo lo spostamento di una finestra.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: Messaggio WM_MOVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56004ec47266a50bf2ac82a828b9046c84a8ebfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312371"
---
# <a name="wm_move-message"></a><span data-ttu-id="896cc-103">\_Messaggio di spostamento WM</span><span class="sxs-lookup"><span data-stu-id="896cc-103">WM\_MOVE message</span></span>

<span data-ttu-id="896cc-104">Inviato dopo lo spostamento di una finestra.</span><span class="sxs-lookup"><span data-stu-id="896cc-104">Sent after a window has been moved.</span></span>

<span data-ttu-id="896cc-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="896cc-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a><span data-ttu-id="896cc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="896cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="896cc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="896cc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="896cc-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="896cc-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="896cc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="896cc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="896cc-110">Coordinate x e y dell'angolo superiore sinistro dell'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="896cc-110">The x and y coordinates of the upper-left corner of the client area of the window.</span></span> <span data-ttu-id="896cc-111">La parola di ordine inferiore contiene la coordinata x mentre la parola più significativa contiene la coordinata y.</span><span class="sxs-lookup"><span data-stu-id="896cc-111">The low-order word contains the x-coordinate while the high-order word contains the y coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="896cc-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="896cc-112">Return value</span></span>

<span data-ttu-id="896cc-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="896cc-113">Type: **LRESULT**</span></span>

<span data-ttu-id="896cc-114">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="896cc-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="896cc-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="896cc-115">Remarks</span></span>

<span data-ttu-id="896cc-116">I parametri vengono specificati nelle coordinate dello schermo per le finestre sovrapposte e popup e nelle coordinate padre-client per le finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="896cc-116">The parameters are given in screen coordinates for overlapped and pop-up windows and in parent-client coordinates for child windows.</span></span>

<span data-ttu-id="896cc-117">Nell'esempio seguente viene illustrato come ottenere la posizione dal parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="896cc-117">The following example demonstrates how to obtain the position from the *lParam* parameter.</span></span>


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



<span data-ttu-id="896cc-118">È anche possibile usare la macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) per convertire il parametro *lParam* in una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="896cc-118">You can also use the [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) macro to convert the *lParam* parameter to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure.</span></span>

<span data-ttu-id="896cc-119">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia i messaggi di **\_ dimensioni WM** e di **\_ spostamento WM** quando elabora il messaggio [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="896cc-119">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="896cc-120">I messaggi WM **\_ size** e **WM \_ Move** non vengono inviati se un'applicazione gestisce il messaggio **WM \_ WINDOWPOSCHANGED** senza chiamare **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="896cc-120">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="896cc-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="896cc-121">Requirements</span></span>



| <span data-ttu-id="896cc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="896cc-122">Requirement</span></span> | <span data-ttu-id="896cc-123">Valore</span><span class="sxs-lookup"><span data-stu-id="896cc-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="896cc-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="896cc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="896cc-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="896cc-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="896cc-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="896cc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="896cc-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="896cc-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="896cc-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="896cc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="896cc-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="896cc-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="896cc-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="896cc-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="896cc-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="896cc-131">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="896cc-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="896cc-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="896cc-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="896cc-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="896cc-134">**\_WINDOWPOSCHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="896cc-134">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="896cc-135">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="896cc-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="896cc-136">Windows</span><span class="sxs-lookup"><span data-stu-id="896cc-136">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="896cc-137">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="896cc-137">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="896cc-138">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="896cc-138">**MAKEPOINTS**</span></span>](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="896cc-139">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="896cc-139">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

 
