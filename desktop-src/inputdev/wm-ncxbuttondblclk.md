---
title: Messaggio WM_NCXBUTTONDBLCLK (winuser. h)
description: Inviato quando l'utente fa doppio clic sul primo o sul secondo pulsante X mentre il cursore si trova nell'area non client di una finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.
ms.assetid: 8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef
keywords:
- Input della tastiera e del mouse WM_NCXBUTTONDBLCLK messaggio
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1455f6d6c2fa40f34bbfbe00e0c7a30daa52f375
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302392"
---
# <a name="wm_ncxbuttondblclk-message"></a><span data-ttu-id="f8050-106">\_Messaggio NCXBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="f8050-106">WM\_NCXBUTTONDBLCLK message</span></span>

<span data-ttu-id="f8050-107">Inviato quando l'utente fa doppio clic sul primo o sul secondo pulsante X mentre il cursore si trova nell'area non client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="f8050-107">Posted when the user double-clicks the first or second X button while the cursor is in the nonclient area of a window.</span></span> <span data-ttu-id="f8050-108">Questo messaggio viene inserito nella finestra che contiene il cursore.</span><span class="sxs-lookup"><span data-stu-id="f8050-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="f8050-109">Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.</span><span class="sxs-lookup"><span data-stu-id="f8050-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="f8050-110">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f8050-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCXBUTTONDBLCLK              0x00AD
```



## <a name="parameters"></a><span data-ttu-id="f8050-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8050-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8050-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8050-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8050-113">La parola di ordine inferiore specifica il valore di hit test restituito dalla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dall'elaborazione del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="f8050-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function from processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="f8050-114">Per un elenco dei valori di hit test, vedere **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="f8050-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="f8050-115">La parola più ordinata indica il pulsante su cui è stato fatto doppio clic.</span><span class="sxs-lookup"><span data-stu-id="f8050-115">The high-order word indicates which button was double-clicked.</span></span> <span data-ttu-id="f8050-116">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f8050-116">It can be one of the following values.</span></span>



| <span data-ttu-id="f8050-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f8050-117">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="f8050-118">Significato</span><span class="sxs-lookup"><span data-stu-id="f8050-118">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="f8050-119"><dt></dt> <dt>0x0001</dt> XBUTTON1</span><span class="sxs-lookup"><span data-stu-id="f8050-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="f8050-120">È stato fatto doppio clic sul primo pulsante X.</span><span class="sxs-lookup"><span data-stu-id="f8050-120">The first X button was double-clicked..</span></span><br/> |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="f8050-121"><dt></dt> <dt>0x0002</dt> XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="f8050-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="f8050-122">È stato fatto doppio clic sul secondo pulsante X.</span><span class="sxs-lookup"><span data-stu-id="f8050-122">The second X button was double-clicked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f8050-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8050-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8050-124">Puntatore a una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) che contiene le coordinate x e y del cursore.</span><span class="sxs-lookup"><span data-stu-id="f8050-124">A pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="f8050-125">Le coordinate sono relative all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="f8050-125">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8050-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8050-126">Return value</span></span>

<span data-ttu-id="f8050-127">Se un'applicazione elabora il messaggio, deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="f8050-127">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="f8050-128">Per ulteriori informazioni sull'elaborazione del valore restituito, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="f8050-128">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8050-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8050-129">Remarks</span></span>

<span data-ttu-id="f8050-130">Usare il codice seguente per ottenere le informazioni nel parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f8050-130">Use the following code to get the information in the *wParam* parameter.</span></span>


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



<span data-ttu-id="f8050-131">È anche possibile usare il codice seguente per ottenere le coordinate x e y da *lParam*:</span><span class="sxs-lookup"><span data-stu-id="f8050-131">You can also use the following code to get the x- and y-coordinates from *lParam*:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="f8050-132">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="f8050-132">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="f8050-133">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="f8050-133">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="f8050-134">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) testa il punto specificato per ottenere la posizione del cursore ed esegue l'azione appropriata.</span><span class="sxs-lookup"><span data-stu-id="f8050-134">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to get the position of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="f8050-135">Se appropriato, invia il messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) alla finestra.</span><span class="sxs-lookup"><span data-stu-id="f8050-135">If appropriate, it sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="f8050-136">Una finestra non deve avere lo stile **cs \_ DBLCLKS** per ricevere i messaggi **WM \_ NCXBUTTONDBLCLK** .</span><span class="sxs-lookup"><span data-stu-id="f8050-136">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCXBUTTONDBLCLK** messages.</span></span> <span data-ttu-id="f8050-137">Il sistema genera un messaggio **WM \_ NCXBUTTONDBLCLK** quando l'utente preme, rilascia e preme di nuovo un pulsante X entro il limite di tempo doppio clic del sistema.</span><span class="sxs-lookup"><span data-stu-id="f8050-137">The system generates a **WM\_NCXBUTTONDBLCLK** message when the user presses, releases, and again presses an X button within the system's double-click time limit.</span></span> <span data-ttu-id="f8050-138">Facendo doppio clic su uno di questi pulsanti vengono effettivamente generati quattro messaggi: [**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md), [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md), **WM \_ NCXBUTTONDBLCLK** e **WM \_ NCXBUTTONUP** .</span><span class="sxs-lookup"><span data-stu-id="f8050-138">Double-clicking one of these buttons actually generates four messages: [**WM\_NCXBUTTONDOWN**](wm-ncxbuttondown.md), [**WM\_NCXBUTTONUP**](wm-ncxbuttonup.md), **WM\_NCXBUTTONDBLCLK**, and **WM\_NCXBUTTONUP** again.</span></span>

<span data-ttu-id="f8050-139">A differenza dei [**messaggi \_ WM NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md), [**WM \_ NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md)e [**WM \_ NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md) , un'applicazione deve restituire **true** da questo messaggio se viene elaborata.</span><span class="sxs-lookup"><span data-stu-id="f8050-139">Unlike the [**WM\_NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md), [**WM\_NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md), and [**WM\_NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="f8050-140">In questo modo si consentirà il software che simula questo messaggio nei sistemi Windows precedenti a Windows 2000 per determinare se la routine della finestra ha elaborato il messaggio o chiamato [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per elaborarlo.</span><span class="sxs-lookup"><span data-stu-id="f8050-140">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8050-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8050-141">Requirements</span></span>



| <span data-ttu-id="f8050-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8050-142">Requirement</span></span> | <span data-ttu-id="f8050-143">Valore</span><span class="sxs-lookup"><span data-stu-id="f8050-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8050-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8050-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f8050-145">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f8050-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8050-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8050-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f8050-147">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f8050-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8050-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8050-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8050-149"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f8050-149"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8050-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8050-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8050-151">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f8050-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f8050-152">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="f8050-152">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="f8050-153">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="f8050-153">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="f8050-154">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="f8050-154">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="f8050-155">**\_NCHITTEST WM**</span><span class="sxs-lookup"><span data-stu-id="f8050-155">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="f8050-156">**\_NCXBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="f8050-156">**WM\_NCXBUTTONDOWN**</span></span>](wm-ncxbuttondown.md)
</dt> <dt>

[<span data-ttu-id="f8050-157">**\_NCXBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="f8050-157">**WM\_NCXBUTTONUP**</span></span>](wm-ncxbuttonup.md)
</dt> <dt>

[<span data-ttu-id="f8050-158">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="f8050-158">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="f8050-159">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="f8050-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f8050-160">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="f8050-160">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="f8050-161">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="f8050-161">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f8050-162">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="f8050-162">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="f8050-163">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8050-163">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

