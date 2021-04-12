---
description: Inviato quando lo sfondo della finestra deve essere cancellato (ad esempio, quando una finestra viene ridimensionata). Il messaggio viene inviato per preparare una parte invalidata di una finestra per il disegno.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: Messaggio WM_ERASEBKGND (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232463"
---
# <a name="wm_erasebkgnd-message"></a><span data-ttu-id="5aef1-104">\_Messaggio ERASEBKGND WM</span><span class="sxs-lookup"><span data-stu-id="5aef1-104">WM\_ERASEBKGND message</span></span>

<span data-ttu-id="5aef1-105">Inviato quando lo sfondo della finestra deve essere cancellato (ad esempio, quando una finestra viene ridimensionata).</span><span class="sxs-lookup"><span data-stu-id="5aef1-105">Sent when the window background must be erased (for example, when a window is resized).</span></span> <span data-ttu-id="5aef1-106">Il messaggio viene inviato per preparare una parte invalidata di una finestra per il disegno.</span><span class="sxs-lookup"><span data-stu-id="5aef1-106">The message is sent to prepare an invalidated portion of a window for painting.</span></span>


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a><span data-ttu-id="5aef1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5aef1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aef1-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5aef1-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5aef1-109">Handle per il contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5aef1-109">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="5aef1-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5aef1-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5aef1-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="5aef1-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aef1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5aef1-112">Return value</span></span>

<span data-ttu-id="5aef1-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5aef1-113">Type: **LRESULT**</span></span>

<span data-ttu-id="5aef1-114">Un'applicazione deve restituire un valore diverso da zero se cancella lo sfondo; in caso contrario, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="5aef1-114">An application should return nonzero if it erases the background; otherwise, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aef1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5aef1-115">Remarks</span></span>

<span data-ttu-id="5aef1-116">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Cancella lo sfondo utilizzando il pennello di sfondo della classe specificato dal membro **HbrBackground** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) .</span><span class="sxs-lookup"><span data-stu-id="5aef1-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function erases the background by using the class background brush specified by the **hbrBackground** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure.</span></span> <span data-ttu-id="5aef1-117">Se **hbrBackground** è **null**, l'applicazione deve elaborare il messaggio **WM \_ ERASEBKGND** e cancellare lo sfondo.</span><span class="sxs-lookup"><span data-stu-id="5aef1-117">If **hbrBackground** is **NULL**, the application should process the **WM\_ERASEBKGND** message and erase the background.</span></span>

<span data-ttu-id="5aef1-118">Un'applicazione deve restituire un valore diverso da zero in risposta a **WM \_ ERASEBKGND** se elabora il messaggio e cancella lo sfondo. ciò indica che non è necessaria alcuna ulteriore cancellazione.</span><span class="sxs-lookup"><span data-stu-id="5aef1-118">An application should return nonzero in response to **WM\_ERASEBKGND** if it processes the message and erases the background; this indicates that no further erasing is required.</span></span> <span data-ttu-id="5aef1-119">Se l'applicazione restituisce zero, la finestra rimarrà contrassegnata per la cancellazione.</span><span class="sxs-lookup"><span data-stu-id="5aef1-119">If the application returns zero, the window will remain marked for erasing.</span></span> <span data-ttu-id="5aef1-120">In genere, ciò indica che il membro **fErase** della struttura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) sarà **true**.</span><span class="sxs-lookup"><span data-stu-id="5aef1-120">(Typically, this indicates that the **fErase** member of the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure will be **TRUE**.)</span></span>

## <a name="requirements"></a><span data-ttu-id="5aef1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5aef1-121">Requirements</span></span>



| <span data-ttu-id="5aef1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aef1-122">Requirement</span></span> | <span data-ttu-id="5aef1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5aef1-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aef1-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5aef1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5aef1-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5aef1-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5aef1-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5aef1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5aef1-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5aef1-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5aef1-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5aef1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5aef1-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5aef1-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aef1-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5aef1-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="5aef1-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="5aef1-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5aef1-132">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5aef1-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="5aef1-133">**WNDCLASS**</span><span class="sxs-lookup"><span data-stu-id="5aef1-133">**WNDCLASS**</span></span>](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

<span data-ttu-id="5aef1-134">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="5aef1-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5aef1-135">Icone</span><span class="sxs-lookup"><span data-stu-id="5aef1-135">Icons</span></span>](../menurc/icons.md)
</dt> <dt>

<span data-ttu-id="5aef1-136">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="5aef1-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5aef1-137">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="5aef1-137">**BeginPaint**</span></span>](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="5aef1-138">**PAINTSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="5aef1-138">**PAINTSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
