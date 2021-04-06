---
title: Messaggio WM_NCXBUTTONUP (winuser. h)
description: Inviato quando l'utente rilascia il primo o il secondo pulsante X mentre il cursore si trova nell'area non client di una finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.
ms.assetid: 07ab5d4e-9912-4867-9146-8abc5addc15d
keywords:
- Input della tastiera e del mouse WM_NCXBUTTONUP messaggio
topic_type:
- apiref
api_name:
- WM_NCXBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6330849a433787dd09fad536f005d91f60376013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742346"
---
# <a name="wm_ncxbuttonup-message"></a><span data-ttu-id="486ab-106">\_Messaggio NCXBUTTONUP WM</span><span class="sxs-lookup"><span data-stu-id="486ab-106">WM\_NCXBUTTONUP message</span></span>

<span data-ttu-id="486ab-107">Inviato quando l'utente rilascia il primo o il secondo pulsante X mentre il cursore si trova nell'area non client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="486ab-107">Posted when the user releases the first or second X button while the cursor is in the nonclient area of a window.</span></span> <span data-ttu-id="486ab-108">Questo messaggio viene inserito nella finestra che contiene il cursore.</span><span class="sxs-lookup"><span data-stu-id="486ab-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="486ab-109">Se una finestra ha acquisito il mouse, questo messaggio *non* viene inviato.</span><span class="sxs-lookup"><span data-stu-id="486ab-109">If a window has captured the mouse, this message is *not* posted.</span></span>

<span data-ttu-id="486ab-110">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="486ab-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCXBUTTONUP                  0x00AC
```



## <a name="parameters"></a><span data-ttu-id="486ab-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="486ab-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="486ab-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="486ab-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="486ab-113">La parola di ordine inferiore specifica il valore di hit test restituito dalla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dall'elaborazione del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="486ab-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function from processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="486ab-114">Per un elenco dei valori di hit test, vedere **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="486ab-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="486ab-115">La parola più ordinata indica quale pulsante è stato rilasciato.</span><span class="sxs-lookup"><span data-stu-id="486ab-115">The high-order word indicates which button was released.</span></span> <span data-ttu-id="486ab-116">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="486ab-116">It can be one of the following values.</span></span>



| <span data-ttu-id="486ab-117">Valore</span><span class="sxs-lookup"><span data-stu-id="486ab-117">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="486ab-118">Significato</span><span class="sxs-lookup"><span data-stu-id="486ab-118">Meaning</span></span>                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="486ab-119"><dt></dt> <dt>0x0001</dt> XBUTTON1</span><span class="sxs-lookup"><span data-stu-id="486ab-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="486ab-120">Il primo pulsante X è stato rilasciato.</span><span class="sxs-lookup"><span data-stu-id="486ab-120">The first X button was released.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="486ab-121"><dt></dt> <dt>0x0002</dt> XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="486ab-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="486ab-122">Il secondo pulsante X è stato rilasciato.</span><span class="sxs-lookup"><span data-stu-id="486ab-122">The second X button was released.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="486ab-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="486ab-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="486ab-124">Puntatore a una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) che contiene le coordinate x e y del cursore.</span><span class="sxs-lookup"><span data-stu-id="486ab-124">A pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="486ab-125">Le coordinate sono relative all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="486ab-125">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="486ab-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="486ab-126">Return value</span></span>

<span data-ttu-id="486ab-127">Se un'applicazione elabora il messaggio, deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="486ab-127">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="486ab-128">Per ulteriori informazioni sull'elaborazione del valore restituito, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="486ab-128">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="486ab-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="486ab-129">Remarks</span></span>

<span data-ttu-id="486ab-130">Usare il codice seguente per ottenere le informazioni nel parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="486ab-130">Use the following code to get the information in the *wParam* parameter.</span></span>


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



<span data-ttu-id="486ab-131">È anche possibile usare il codice seguente per ottenere le coordinate x e y da *lParam*:</span><span class="sxs-lookup"><span data-stu-id="486ab-131">You can also use the following code to get the x- and y-coordinates from *lParam*:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="486ab-132">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="486ab-132">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="486ab-133">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="486ab-133">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="486ab-134">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) testa il punto specificato per ottenere la posizione del cursore ed esegue l'azione appropriata.</span><span class="sxs-lookup"><span data-stu-id="486ab-134">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to get the position of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="486ab-135">Se appropriato, invia il messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) alla finestra.</span><span class="sxs-lookup"><span data-stu-id="486ab-135">If appropriate, it sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="486ab-136">A differenza dei [**messaggi \_ WM NCLBUTTONUP**](wm-nclbuttonup.md), [**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md)e [**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md) , un'applicazione deve restituire **true** da questo messaggio se viene elaborata.</span><span class="sxs-lookup"><span data-stu-id="486ab-136">Unlike the [**WM\_NCLBUTTONUP**](wm-nclbuttonup.md), [**WM\_NCMBUTTONUP**](wm-ncmbuttonup.md), and [**WM\_NCRBUTTONUP**](wm-ncrbuttonup.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="486ab-137">In questo modo si consentirà il software che simula questo messaggio nei sistemi Windows precedenti a Windows 2000 per determinare se la routine della finestra ha elaborato il messaggio o chiamato [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per elaborarlo.</span><span class="sxs-lookup"><span data-stu-id="486ab-137">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="486ab-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="486ab-138">Requirements</span></span>



| <span data-ttu-id="486ab-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="486ab-139">Requirement</span></span> | <span data-ttu-id="486ab-140">Valore</span><span class="sxs-lookup"><span data-stu-id="486ab-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="486ab-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="486ab-141">Minimum supported client</span></span><br/> | <span data-ttu-id="486ab-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="486ab-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="486ab-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="486ab-143">Minimum supported server</span></span><br/> | <span data-ttu-id="486ab-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="486ab-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="486ab-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="486ab-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="486ab-146"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="486ab-146"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="486ab-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="486ab-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="486ab-148">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="486ab-148">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="486ab-149">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="486ab-149">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="486ab-150">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="486ab-150">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="486ab-151">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="486ab-151">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="486ab-152">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="486ab-152">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="486ab-153">**\_NCXBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="486ab-153">**WM\_NCXBUTTONDBLCLK**</span></span>](wm-ncxbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="486ab-154">**\_NCXBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="486ab-154">**WM\_NCXBUTTONDOWN**</span></span>](wm-ncxbuttondown.md)
</dt> <dt>

[<span data-ttu-id="486ab-155">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="486ab-155">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="486ab-156">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="486ab-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="486ab-157">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="486ab-157">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="486ab-158">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="486ab-158">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="486ab-159">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="486ab-159">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="486ab-160">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="486ab-160">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

