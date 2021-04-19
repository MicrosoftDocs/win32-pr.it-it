---
title: Messaggio WM_NCHITTEST (winuser. h)
description: Inviato a una finestra per determinare quale parte della finestra corrisponde a una determinata coordinata dello schermo.
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- Input della tastiera e del mouse WM_NCHITTEST messaggio
topic_type:
- apiref
api_name:
- WM_NCHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf14e817831c099988e9fb3fee57ae0731ef621
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301422"
---
# <a name="wm_nchittest-message"></a><span data-ttu-id="d792c-104">\_Messaggio NCHITTEST WM</span><span class="sxs-lookup"><span data-stu-id="d792c-104">WM\_NCHITTEST message</span></span>

<span data-ttu-id="d792c-105">Inviato a una finestra per determinare quale parte della finestra corrisponde a una determinata coordinata dello schermo.</span><span class="sxs-lookup"><span data-stu-id="d792c-105">Sent to a window in order to determine what part of the window corresponds to a particular screen coordinate.</span></span> <span data-ttu-id="d792c-106">Questo può accadere, ad esempio, quando il cursore viene spostato, quando viene premuto o rilasciato un pulsante del mouse o in risposta a una chiamata a una funzione come [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint).</span><span class="sxs-lookup"><span data-stu-id="d792c-106">This can happen, for example, when the cursor moves, when a mouse button is pressed or released, or in response to a call to a function such as [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint).</span></span> <span data-ttu-id="d792c-107">Se il mouse non viene acquisito, il messaggio viene inviato alla finestra sotto il cursore.</span><span class="sxs-lookup"><span data-stu-id="d792c-107">If the mouse is not captured, the message is sent to the window beneath the cursor.</span></span> <span data-ttu-id="d792c-108">In caso contrario, il messaggio viene inviato alla finestra che ha acquisito il mouse.</span><span class="sxs-lookup"><span data-stu-id="d792c-108">Otherwise, the message is sent to the window that has captured the mouse.</span></span>

<span data-ttu-id="d792c-109">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d792c-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCHITTEST                    0x0084
```



## <a name="parameters"></a><span data-ttu-id="d792c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d792c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d792c-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d792c-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d792c-112">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="d792c-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d792c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d792c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d792c-114">La parola di ordine inferiore specifica la coordinata x del cursore.</span><span class="sxs-lookup"><span data-stu-id="d792c-114">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="d792c-115">La coordinata è relativa all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="d792c-115">The coordinate is relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="d792c-116">La parola di ordine superiore specifica la coordinata y del cursore.</span><span class="sxs-lookup"><span data-stu-id="d792c-116">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="d792c-117">La coordinata è relativa all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="d792c-117">The coordinate is relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d792c-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d792c-118">Return value</span></span>

<span data-ttu-id="d792c-119">Il valore restituito della funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) è uno dei valori seguenti, che indica la posizione dell'area sensibile del cursore.</span><span class="sxs-lookup"><span data-stu-id="d792c-119">The return value of the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function is one of the following values, indicating the position of the cursor hot spot.</span></span>



| <span data-ttu-id="d792c-120">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="d792c-120">Return code/value</span></span>                                                                                                                                    | <span data-ttu-id="d792c-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d792c-121">Description</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d792c-122"><dt>**HTBORDER**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-122"><dt>**HTBORDER**</dt> <dt>18</dt></span></span> </dl>      | <span data-ttu-id="d792c-123">Nel bordo di una finestra che non dispone di un bordo di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="d792c-123">In the border of a window that does not have a sizing border.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="d792c-124"><dt>**HTBOTTOM**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-124"><dt>**HTBOTTOM**</dt> <dt>15</dt></span></span> </dl>      | <span data-ttu-id="d792c-125">Nel bordo inferiore orizzontale di una finestra ridimensionabile (l'utente può fare clic sul mouse per ridimensionare la finestra verticalmente).</span><span class="sxs-lookup"><span data-stu-id="d792c-125">In the lower-horizontal border of a resizable window (the user can click the mouse to resize the window vertically).</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="d792c-126"><dt>**HTBOTTOMLEFT**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-126"><dt>**HTBOTTOMLEFT**</dt> <dt>16</dt></span></span> </dl>  | <span data-ttu-id="d792c-127">Nell'angolo inferiore sinistro di un bordo di una finestra ridimensionabile (l'utente può fare clic sul mouse per ridimensionare la finestra in diagonale).</span><span class="sxs-lookup"><span data-stu-id="d792c-127">In the lower-left corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="d792c-128"><dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-128"><dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt></span></span> </dl> | <span data-ttu-id="d792c-129">Nell'angolo in basso a destra di un bordo di una finestra ridimensionabile (l'utente può fare clic sul mouse per ridimensionare la finestra in diagonale).</span><span class="sxs-lookup"><span data-stu-id="d792c-129">In the lower-right corner of a border of a resizable window (the user can click the mouse to resize the window diagonally).</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="d792c-130"><dt>**HTCAPTION**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-130"><dt>**HTCAPTION**</dt> <dt>2</dt></span></span> </dl>      | <span data-ttu-id="d792c-131">In una barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="d792c-131">In a title bar.</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="d792c-132"><dt>**HTCLIENT**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-132"><dt>**HTCLIENT**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="d792c-133">In un'area client.</span><span class="sxs-lookup"><span data-stu-id="d792c-133">In a client area.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="d792c-134"><dt>**HTCLOSE**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-134"><dt>**HTCLOSE**</dt> <dt>20</dt></span></span> </dl>       | <span data-ttu-id="d792c-135">In un pulsante **Chiudi** .</span><span class="sxs-lookup"><span data-stu-id="d792c-135">In a **Close** button.</span></span><br/>                                                                                                                                                                                  |
| <dl> <span data-ttu-id="d792c-136"><dt>**HTERROR**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-136"><dt>**HTERROR**</dt> <dt>-2</dt></span></span> </dl>       | <span data-ttu-id="d792c-137">Sullo sfondo dello schermo o su una linea di divisione tra le finestre (uguale a **HTNOWHERE**, con la differenza che la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera un segnale acustico di sistema per indicare un errore).</span><span class="sxs-lookup"><span data-stu-id="d792c-137">On the screen background or on a dividing line between windows (same as **HTNOWHERE**, except that the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function produces a system beep to indicate an error).</span></span><br/> |
| <dl> <span data-ttu-id="d792c-138"><dt>**HTGROWBOX**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-138"><dt>**HTGROWBOX**</dt> <dt>4</dt></span></span> </dl>      | <span data-ttu-id="d792c-139">In una casella delle dimensioni (uguale a **HTSIZE**).</span><span class="sxs-lookup"><span data-stu-id="d792c-139">In a size box (same as **HTSIZE**).</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="d792c-140"><dt>**HTHELP**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-140"><dt>**HTHELP**</dt> <dt>21</dt></span></span> </dl>        | <span data-ttu-id="d792c-141">In un pulsante della **Guida** .</span><span class="sxs-lookup"><span data-stu-id="d792c-141">In a **Help** button.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="d792c-142"><dt>**HTHSCROLL**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-142"><dt>**HTHSCROLL**</dt> <dt>6</dt></span></span> </dl>      | <span data-ttu-id="d792c-143">In una barra di scorrimento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="d792c-143">In a horizontal scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="d792c-144"><dt>**HTLEFT**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-144"><dt>**HTLEFT**</dt> <dt>10</dt></span></span> </dl>        | <span data-ttu-id="d792c-145">Sul bordo sinistro di una finestra ridimensionabile (l'utente può fare clic sul mouse per ridimensionare la finestra orizzontalmente).</span><span class="sxs-lookup"><span data-stu-id="d792c-145">In the left border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="d792c-146"><dt>**HTMENU**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-146"><dt>**HTMENU**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="d792c-147">In un menu.</span><span class="sxs-lookup"><span data-stu-id="d792c-147">In a menu.</span></span><br/>                                                                                                                                                                                              |
| <dl> <span data-ttu-id="d792c-148"><dt>**HTMAXBUTTON**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-148"><dt>**HTMAXBUTTON**</dt> <dt>9</dt></span></span> </dl>    | <span data-ttu-id="d792c-149">In un pulsante **Ingrandisci** .</span><span class="sxs-lookup"><span data-stu-id="d792c-149">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="d792c-150"><dt>**HTMINBUTTON**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-150"><dt>**HTMINBUTTON**</dt> <dt>8</dt></span></span> </dl>    | <span data-ttu-id="d792c-151">In un pulsante **Riduci a icona** .</span><span class="sxs-lookup"><span data-stu-id="d792c-151">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="d792c-152"><dt>**HTNOWHERE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-152"><dt>**HTNOWHERE**</dt> <dt>0</dt></span></span> </dl>      | <span data-ttu-id="d792c-153">Sullo sfondo dello schermo o su una linea di divisione tra le finestre.</span><span class="sxs-lookup"><span data-stu-id="d792c-153">On the screen background or on a dividing line between windows.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="d792c-154"><dt>**HTREDUCE**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-154"><dt>**HTREDUCE**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="d792c-155">In un pulsante **Riduci a icona** .</span><span class="sxs-lookup"><span data-stu-id="d792c-155">In a **Minimize** button.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="d792c-156"><dt>**HTRIGHT**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-156"><dt>**HTRIGHT**</dt> <dt>11</dt></span></span> </dl>       | <span data-ttu-id="d792c-157">Sul bordo destro di una finestra ridimensionabile (l'utente può fare clic sul mouse per ridimensionare la finestra orizzontalmente).</span><span class="sxs-lookup"><span data-stu-id="d792c-157">In the right border of a resizable window (the user can click the mouse to resize the window horizontally).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="d792c-158"><dt>**HTSIZE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-158"><dt>**HTSIZE**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="d792c-159">In una casella delle dimensioni (uguale a **HTGROWBOX**).</span><span class="sxs-lookup"><span data-stu-id="d792c-159">In a size box (same as **HTGROWBOX**).</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="d792c-160"><dt>**HTSYSMENU**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-160"><dt>**HTSYSMENU**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="d792c-161">In un menu finestra o in un pulsante **Chiudi** in una finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="d792c-161">In a window menu or in a **Close** button in a child window.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="d792c-162"><dt>**HTTOP**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-162"><dt>**HTTOP**</dt> <dt>12</dt></span></span> </dl>         | <span data-ttu-id="d792c-163">Nel bordo superiore orizzontale di una finestra.</span><span class="sxs-lookup"><span data-stu-id="d792c-163">In the upper-horizontal border of a window.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="d792c-164"><dt>**HTTOPLEFT**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-164"><dt>**HTTOPLEFT**</dt> <dt>13</dt></span></span> </dl>     | <span data-ttu-id="d792c-165">Nell'angolo superiore sinistro del bordo di una finestra.</span><span class="sxs-lookup"><span data-stu-id="d792c-165">In the upper-left corner of a window border.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="d792c-166"><dt>**HTTOPRIGHT**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-166"><dt>**HTTOPRIGHT**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="d792c-167">Nell'angolo superiore destro del bordo di una finestra.</span><span class="sxs-lookup"><span data-stu-id="d792c-167">In the upper-right corner of a window border.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="d792c-168"><dt>**HTTRANSPARENT**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-168"><dt>**HTTRANSPARENT**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="d792c-169">In una finestra attualmente coperta da un'altra finestra nello stesso thread (il messaggio verrà inviato alle finestre sottostanti nello stesso thread fino a quando uno di essi non restituisce un codice non **HTTRANSPARENT**).</span><span class="sxs-lookup"><span data-stu-id="d792c-169">In a window currently covered by another window in the same thread (the message will be sent to underlying windows in the same thread until one of them returns a code that is not **HTTRANSPARENT**).</span></span><br/>  |
| <dl> <span data-ttu-id="d792c-170"><dt>**HTVSCROLL**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-170"><dt>**HTVSCROLL**</dt> <dt>7</dt></span></span> </dl>      | <span data-ttu-id="d792c-171">Sulla barra di scorrimento verticale.</span><span class="sxs-lookup"><span data-stu-id="d792c-171">In the vertical scroll bar.</span></span><br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="d792c-172"><dt>**HTZOOM**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-172"><dt>**HTZOOM**</dt> <dt>9</dt></span></span> </dl>         | <span data-ttu-id="d792c-173">In un pulsante **Ingrandisci** .</span><span class="sxs-lookup"><span data-stu-id="d792c-173">In a **Maximize** button.</span></span><br/>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="d792c-174">Commenti</span><span class="sxs-lookup"><span data-stu-id="d792c-174">Remarks</span></span>

<span data-ttu-id="d792c-175">Usare il codice seguente per ottenere la posizione orizzontale e verticale:</span><span class="sxs-lookup"><span data-stu-id="d792c-175">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="d792c-176">Come indicato in precedenza, la coordinata x è **nell'ordine inferiore** del valore restituito. la coordinata y si trova nell'ordine **breve** (entrambi rappresentano valori *firmati* perché possono assumere valori negativi nei sistemi con più monitoraggi).</span><span class="sxs-lookup"><span data-stu-id="d792c-176">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="d792c-177">Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) dal valore restituito.</span><span class="sxs-lookup"><span data-stu-id="d792c-177">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="d792c-178">Per estrarre la coordinata x o y, è anche possibile usare la macro [**get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="d792c-178">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d792c-179">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="d792c-179">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="d792c-180">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="d792c-180">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="d792c-181">**Windows Vista:** Quando si creano frame personalizzati che includono i pulsanti della didascalia standard, questo messaggio deve essere prima passato alla funzione [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) .</span><span class="sxs-lookup"><span data-stu-id="d792c-181">**Windows Vista:** When creating custom frames that include the standard caption buttons, this message should first be passed to the [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) function.</span></span> <span data-ttu-id="d792c-182">Ciò consente all'Gestione finestre desktop (DWM) di fornire hit testing per i pulsanti didascalie.</span><span class="sxs-lookup"><span data-stu-id="d792c-182">This enables the Desktop Window Manager (DWM) to provide hit-testing for the captions buttons.</span></span> <span data-ttu-id="d792c-183">Se **DwmDefWindowProc** non gestisce il messaggio, potrebbe essere necessaria un'ulteriore elaborazione di **WM \_ NCHITTEST** .</span><span class="sxs-lookup"><span data-stu-id="d792c-183">If **DwmDefWindowProc** does not handle the message, further processing of **WM\_NCHITTEST** may be needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d792c-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d792c-184">Requirements</span></span>



| <span data-ttu-id="d792c-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="d792c-185">Requirement</span></span> | <span data-ttu-id="d792c-186">Valore</span><span class="sxs-lookup"><span data-stu-id="d792c-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d792c-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d792c-187">Minimum supported client</span></span><br/> | <span data-ttu-id="d792c-188">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d792c-188">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d792c-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d792c-189">Minimum supported server</span></span><br/> | <span data-ttu-id="d792c-190">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d792c-190">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d792c-191">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d792c-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="d792c-192"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d792c-192"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d792c-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d792c-193">See also</span></span>

<dl> <dt>

<span data-ttu-id="d792c-194">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d792c-194">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d792c-195">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="d792c-195">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="d792c-196">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="d792c-196">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="d792c-197">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="d792c-197">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

<span data-ttu-id="d792c-198">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d792c-198">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d792c-199">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="d792c-199">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="d792c-200">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="d792c-200">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d792c-201">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="d792c-201">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="d792c-202">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d792c-202">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

