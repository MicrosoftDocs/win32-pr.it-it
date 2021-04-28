---
title: 'Funzione di input tramite mouse '
description: 'Funzione di input tramite mouse '
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a952a9ce90284f284b176c608228c0b852f5f4c8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112879"
---
# <a name="mouse-input-functions"></a><span data-ttu-id="73bd1-103">Funzione di input tramite mouse </span><span class="sxs-lookup"><span data-stu-id="73bd1-103">Mouse Input Functions</span></span>


## <a name="in-this-section"></a><span data-ttu-id="73bd1-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="73bd1-104">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73bd1-105">Argomento</span><span class="sxs-lookup"><span data-stu-id="73bd1-105">Topic</span></span></th>
<th><span data-ttu-id="73bd1-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73bd1-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73bd1-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="73bd1-107"><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="73bd1-108">Invia messaggi quando il puntatore del mouse esce da una finestra o si posiziona su una finestra per un periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="73bd1-108">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span> <span data-ttu-id="73bd1-109">Questa funzione chiama <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent,</strong></a> se esistente, in caso contrario lo emula.</span><span class="sxs-lookup"><span data-stu-id="73bd1-109">This function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise it emulates it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73bd1-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span><span class="sxs-lookup"><span data-stu-id="73bd1-110"><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a></span></span><br/></td>
<td><span data-ttu-id="73bd1-111">Acquisisce il mouse e tiene traccia del suo movimento fino a quando l'utente rilascia il pulsante sinistro, preme ESC o sposta il mouse all'esterno del rettangolo di trascinamento attorno al punto specificato.</span><span class="sxs-lookup"><span data-stu-id="73bd1-111">Captures the mouse and tracks its movement until the user releases the left button, presses the ESC key, or moves the mouse outside the drag rectangle around the specified point.</span></span> <span data-ttu-id="73bd1-112">La larghezza e l'altezza del <strong></strong> rettangolo di trascinamento vengono specificate dai valori SM_CXDRAG e <strong>SM_CYDRAG</strong> restituiti dalla <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>funzione GetSystemMetrics.</strong></a></span><span class="sxs-lookup"><span data-stu-id="73bd1-112">The width and height of the drag rectangle are specified by the <strong>SM_CXDRAG</strong> and <strong>SM_CYDRAG</strong> values returned by the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>GetSystemMetrics</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73bd1-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="73bd1-113"><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="73bd1-114">Recupera un handle per la finestra (se presente) che ha acquisito il mouse.</span><span class="sxs-lookup"><span data-stu-id="73bd1-114">Retrieves a handle to the window (if any) that has captured the mouse.</span></span> <span data-ttu-id="73bd1-115">Solo una finestra alla volta può acquisire il mouse. questa finestra riceve l'input del mouse indipendentemente dal fatto che il cursore si trova all'interno dei bordi.</span><span class="sxs-lookup"><span data-stu-id="73bd1-115">Only one window at a time can capture the mouse; this window receives mouse input whether or not the cursor is within its borders.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73bd1-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="73bd1-116"><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="73bd1-117">Recupera l'ora corrente del doppio clic per il mouse.</span><span class="sxs-lookup"><span data-stu-id="73bd1-117">Retrieves the current double-click time for the mouse.</span></span> <span data-ttu-id="73bd1-118">Un doppio clic è una serie di due clic del pulsante del mouse, il secondo che si verifica entro un periodo di tempo specificato dopo il primo.</span><span class="sxs-lookup"><span data-stu-id="73bd1-118">A double-click is a series of two clicks of the mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="73bd1-119">Il tempo di doppio clic è il numero massimo di millisecondi che possono verificarsi tra il primo e il secondo clic di un doppio clic.</span><span class="sxs-lookup"><span data-stu-id="73bd1-119">The double-click time is the maximum number of milliseconds that may occur between the first and second click of a double-click.</span></span> <span data-ttu-id="73bd1-120">Il tempo massimo per il doppio clic è 5000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="73bd1-120">The maximum double-click time is 5000 milliseconds.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73bd1-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="73bd1-121"><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="73bd1-122">Recupera una cronologia fino a 64 coordinate precedenti del mouse o della penna.</span><span class="sxs-lookup"><span data-stu-id="73bd1-122">Retrieves a history of up to 64 previous coordinates of the mouse or pen.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73bd1-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span><span class="sxs-lookup"><span data-stu-id="73bd1-123"><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a></span></span><br/></td>
<td><span data-ttu-id="73bd1-124">La <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> sintetizza il movimento del mouse e i clic del pulsante.</span><span class="sxs-lookup"><span data-stu-id="73bd1-124">The <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> function synthesizes mouse motion and button clicks.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="73bd1-125">Questa funzione è stata sostituita.</span><span class="sxs-lookup"><span data-stu-id="73bd1-125">This function has been superseded.</span></span> <span data-ttu-id="73bd1-126">In <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>alternativa, usare SendInput.</strong></a></span><span class="sxs-lookup"><span data-stu-id="73bd1-126">Use <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73bd1-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="73bd1-127"><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="73bd1-128">Rilascia il mouse capture da una finestra nel thread corrente e ripristina la normale elaborazione dell'input del mouse.</span><span class="sxs-lookup"><span data-stu-id="73bd1-128">Releases the mouse capture from a window in the current thread and restores normal mouse input processing.</span></span> <span data-ttu-id="73bd1-129">Una finestra che ha acquisito il mouse riceve tutto l'input del mouse, indipendentemente dalla posizione del cursore, tranne quando si fa clic su un pulsante del mouse mentre l'area sensibile del cursore si trova nella finestra di un altro thread.</span><span class="sxs-lookup"><span data-stu-id="73bd1-129">A window that has captured the mouse receives all mouse input, regardless of the position of the cursor, except when a mouse button is clicked while the cursor hot spot is in the window of another thread.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73bd1-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="73bd1-130"><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a></span></span><br/></td>
<td><span data-ttu-id="73bd1-131">Imposta mouse capture sulla finestra specificata appartenente al thread corrente.</span><span class="sxs-lookup"><span data-stu-id="73bd1-131">Sets the mouse capture to the specified window belonging to the current thread.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73bd1-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a></span><span class="sxs-lookup"><span data-stu-id="73bd1-132"><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a></span></span><br/></td>
<td><span data-ttu-id="73bd1-133">Imposta l'ora del doppio clic per il mouse.</span><span class="sxs-lookup"><span data-stu-id="73bd1-133">Sets the double-click time for the mouse.</span></span> <span data-ttu-id="73bd1-134">Un doppio clic è una serie di due clic di un pulsante del mouse, il secondo che si verifica entro un tempo specificato dopo il primo.</span><span class="sxs-lookup"><span data-stu-id="73bd1-134">A double-click is a series of two clicks of a mouse button, the second occurring within a specified time after the first.</span></span> <span data-ttu-id="73bd1-135">Il tempo di doppio clic è il numero massimo di millisecondi che possono verificarsi tra il primo e il secondo clic di un doppio clic.</span><span class="sxs-lookup"><span data-stu-id="73bd1-135">The double-click time is the maximum number of milliseconds that may occur between the first and second clicks of a double-click.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73bd1-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="73bd1-136"><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a></span></span><br/></td>
<td><span data-ttu-id="73bd1-137">Inverte o ripristina il significato dei pulsanti sinistro e destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="73bd1-137">Reverses or restores the meaning of the left and right mouse buttons.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73bd1-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span><span class="sxs-lookup"><span data-stu-id="73bd1-138"><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a></span></span><br/></td>
<td><span data-ttu-id="73bd1-139">Invia messaggi quando il puntatore del mouse lascia una finestra o passa il puntatore del mouse su una finestra per un periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="73bd1-139">Posts messages when the mouse pointer leaves a window or hovers over a window for a specified amount of time.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="73bd1-140">La <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> chiama <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent,</strong></a> se presente, in caso _TrackMouseEvent <strong>emula TrackMouseEvent</strong>. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="73bd1-140">The <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> function calls <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> if it exists, otherwise <strong>_TrackMouseEvent</strong> emulates <strong>TrackMouseEvent</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

