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
# <a name="mouse-input-functions"></a>Funzione di input tramite mouse 


## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a><br/></td>
<td>Invia messaggi quando il puntatore del mouse esce da una finestra o si posiziona su una finestra per un periodo di tempo specificato. Questa funzione chiama <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent,</strong></a> se esistente, in caso contrario lo emula.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a><br/></td>
<td>Acquisisce il mouse e tiene traccia del suo movimento fino a quando l'utente rilascia il pulsante sinistro, preme ESC o sposta il mouse all'esterno del rettangolo di trascinamento attorno al punto specificato. La larghezza e l'altezza del <strong></strong> rettangolo di trascinamento vengono specificate dai valori SM_CXDRAG e <strong>SM_CYDRAG</strong> restituiti dalla <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>funzione GetSystemMetrics.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a><br/></td>
<td>Recupera un handle per la finestra (se presente) che ha acquisito il mouse. Solo una finestra alla volta può acquisire il mouse. questa finestra riceve l'input del mouse indipendentemente dal fatto che il cursore si trova all'interno dei bordi. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a><br/></td>
<td>Recupera l'ora corrente del doppio clic per il mouse. Un doppio clic è una serie di due clic del pulsante del mouse, il secondo che si verifica entro un periodo di tempo specificato dopo il primo. Il tempo di doppio clic è il numero massimo di millisecondi che possono verificarsi tra il primo e il secondo clic di un doppio clic. Il tempo massimo per il doppio clic è 5000 millisecondi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a><br/></td>
<td>Recupera una cronologia fino a 64 coordinate precedenti del mouse o della penna.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a><br/></td>
<td>La <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> sintetizza il movimento del mouse e i clic del pulsante.<br/>
<blockquote>
[!Note]<br />
Questa funzione è stata sostituita. In <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>alternativa, usare SendInput.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a><br/></td>
<td>Rilascia il mouse capture da una finestra nel thread corrente e ripristina la normale elaborazione dell'input del mouse. Una finestra che ha acquisito il mouse riceve tutto l'input del mouse, indipendentemente dalla posizione del cursore, tranne quando si fa clic su un pulsante del mouse mentre l'area sensibile del cursore si trova nella finestra di un altro thread. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a><br/></td>
<td>Imposta mouse capture sulla finestra specificata appartenente al thread corrente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a><br/></td>
<td>Imposta l'ora del doppio clic per il mouse. Un doppio clic è una serie di due clic di un pulsante del mouse, il secondo che si verifica entro un tempo specificato dopo il primo. Il tempo di doppio clic è il numero massimo di millisecondi che possono verificarsi tra il primo e il secondo clic di un doppio clic. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a><br/></td>
<td>Inverte o ripristina il significato dei pulsanti sinistro e destro del mouse. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a><br/></td>
<td>Invia messaggi quando il puntatore del mouse lascia una finestra o passa il puntatore del mouse su una finestra per un periodo di tempo specificato.<br/>
<blockquote>
[!Note]<br />
La <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> chiama <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent,</strong></a> se presente, in caso _TrackMouseEvent <strong>emula TrackMouseEvent</strong>. <strong></strong>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

