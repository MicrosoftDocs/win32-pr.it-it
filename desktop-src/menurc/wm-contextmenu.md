---
title: Messaggio WM_CONTEXTMENU (winuser. h)
description: Notifica a una finestra che l'utente ha fatto clic con il pulsante destro del mouse sulla finestra.
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- Menu del messaggio WM_CONTEXTMENU e altre risorse
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7764926709bfc8ab6aa95be330a9d45d38bc48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301482"
---
# <a name="wm_contextmenu-message"></a><span data-ttu-id="b1ab0-104">Messaggio del ContextMenu di WM \_</span><span class="sxs-lookup"><span data-stu-id="b1ab0-104">WM\_CONTEXTMENU message</span></span>

<span data-ttu-id="b1ab0-105">Notifica a una finestra che l'utente desidera visualizzare un menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-105">Notifies a window that the user desires a context menu to appear.</span></span>  <span data-ttu-id="b1ab0-106">È possibile che l'utente abbia fatto clic con il pulsante destro del mouse sulla finestra, ha premuto MAIUSC + F10 o ha premuto il tasto Applications (menu di scelta rapida) disponibile in alcune tastiere.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-106">The user may have clicked the right mouse button (right-clicked) in the window, pressed Shift+F10 or pressed the applications key (context menu key) available on some keyboards.</span></span>


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a><span data-ttu-id="b1ab0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1ab0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1ab0-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1ab0-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1ab0-109">Handle per la finestra in cui l'utente ha fatto clic con il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-109">A handle to the window in which the user right-clicked the mouse.</span></span> <span data-ttu-id="b1ab0-110">Può trattarsi di una finestra figlio della finestra che riceve il messaggio.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-110">This can be a child window of the window receiving the message.</span></span> <span data-ttu-id="b1ab0-111">Per ulteriori informazioni sull'elaborazione di questo messaggio, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-111">For more information about processing this message, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="b1ab0-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1ab0-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1ab0-113">La parola di ordine inferiore specifica la posizione orizzontale del cursore, in coordinate dello schermo, al momento del clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-113">The low-order word specifies the horizontal position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

<span data-ttu-id="b1ab0-114">La parola più ordinata specifica la posizione verticale del cursore, in coordinate dello schermo, al momento del clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-114">The high-order word specifies the vertical position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1ab0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1ab0-115">Return value</span></span>

<span data-ttu-id="b1ab0-116">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1ab0-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1ab0-117">Remarks</span></span>

<span data-ttu-id="b1ab0-118">Una finestra può elaborare questo messaggio visualizzando un menu di scelta rapida usando le funzioni [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) o [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="b1ab0-118">A window can process this message by displaying a shortcut menu using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) or [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) functions.</span></span> <span data-ttu-id="b1ab0-119">Per ottenere le posizioni orizzontali e verticali, usare il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-119">To obtain the horizontal and vertical positions, use the following code.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="b1ab0-120">Se una finestra non visualizza un menu di scelta rapida, deve passare questo messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="b1ab0-120">If a window does not display a shortcut menu it should pass this message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="b1ab0-121">Se una finestra è una finestra figlio, **DefWindowProc** invia il messaggio all'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-121">If a window is a child window, **DefWindowProc** sends the message to the parent.</span></span> <span data-ttu-id="b1ab0-122">In caso contrario, **DefWindowProc** Visualizza un menu di scelta rapida predefinito se la posizione specificata si trova nella didascalia della finestra.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-122">Otherwise, **DefWindowProc** displays a default shortcut menu if the specified position is in the window's caption.</span></span>

<span data-ttu-id="b1ab0-123">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera il messaggio **WM \_ ContextMenu** quando elabora il messaggio [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) o [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) o quando l'utente digita MAIUSC + F10.</span><span class="sxs-lookup"><span data-stu-id="b1ab0-123">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) generates the **WM\_CONTEXTMENU** message when it processes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message or when the user types SHIFT+F10.</span></span> <span data-ttu-id="b1ab0-124">Il messaggio **WM \_ ContextMenu** viene generato anche quando l'utente preme e rilascia la chiave [**delle \_ app VK**](/windows/desktop/inputdev/virtual-key-codes) .</span><span class="sxs-lookup"><span data-stu-id="b1ab0-124">The **WM\_CONTEXTMENU** message is also generated when the user presses and releases the [**VK\_APPS**](/windows/desktop/inputdev/virtual-key-codes) key.</span></span>

<span data-ttu-id="b1ab0-125">Se il menu di scelta rapida viene generato dalla tastiera, ad esempio se l'utente digita MAIUSC + F10, le coordinate x e y sono pari a-1 e l'applicazione deve visualizzare il menu di scelta rapida nella posizione della selezione corrente anziché in (xPos, yPos).</span><span class="sxs-lookup"><span data-stu-id="b1ab0-125">If the context menu is generated from the keyboard for example, if the user types SHIFT+F10 then the x- and y-coordinates are -1 and the application should display the context menu at the location of the current selection rather than at (xPos, yPos).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1ab0-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1ab0-126">Requirements</span></span>



| <span data-ttu-id="b1ab0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1ab0-127">Requirement</span></span> | <span data-ttu-id="b1ab0-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b1ab0-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ab0-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1ab0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b1ab0-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1ab0-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b1ab0-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1ab0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b1ab0-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1ab0-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b1ab0-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1ab0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1ab0-134"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1ab0-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1ab0-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1ab0-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1ab0-136">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b1ab0-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b1ab0-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="b1ab0-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="b1ab0-138">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="b1ab0-138">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="b1ab0-139">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="b1ab0-139">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="b1ab0-140">**TrackPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="b1ab0-140">**TrackPopupMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[<span data-ttu-id="b1ab0-141">**TrackPopupMenuEx**</span><span class="sxs-lookup"><span data-stu-id="b1ab0-141">**TrackPopupMenuEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[<span data-ttu-id="b1ab0-142">**\_NCRBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="b1ab0-142">**WM\_NCRBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[<span data-ttu-id="b1ab0-143">**\_RBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="b1ab0-143">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

<span data-ttu-id="b1ab0-144">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b1ab0-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b1ab0-145">Menu</span><span class="sxs-lookup"><span data-stu-id="b1ab0-145">Menus</span></span>](menus.md)
</dt> </dl>

 

