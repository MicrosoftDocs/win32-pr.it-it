---
title: Messaggi
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le notifiche e i messaggi di input specifici del puntatore.
ms.assetid: 65F4DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3e143990c65daad306ef6f743d25ef4e0cca8001
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399006"
---
# <a name="messages"></a>Messaggi

Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le [notifiche e i messaggi di input](messages-and-notifications-portal.md)specifici del puntatore.

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
<td>[<strong>DM_POINTERHITTEST</strong>] (dm-pointerhittest.md)<br/></td>
<td>Inviato a una finestra, quando viene rilevato per la prima volta l'input del puntatore, per determinare la destinazione di input più probabile per la [manipolazione diretta](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal). <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERDOWN</strong>] (wm-ncpointerdown.md)<br/></td>
<td>Inviato quando un puntatore fa contatto sull'area non client di una finestra. Il messaggio è destinato alla finestra su cui il puntatore crea il contatto. Il puntatore viene acquisito in modo implicito nella finestra in modo che la finestra continui a ricevere l'input per il puntatore finché non interrompe il contatto. <br/> Se una finestra ha acquisito questo puntatore, questo messaggio non viene inviato. Viene invece pubblicato un [<strong>WM_POINTERDOWN</strong>] (WM-PointerDown.MD) nella finestra che ha acquisito il puntatore. <br/>
<blockquote>
[!Important]<br />
Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_NCPOINTERUP</strong>] (wm-ncpointerup.md)<br/></td>
<td>Inviato quando un puntatore che ha effettuato il contatto sull'area non client di una finestra interrompe il contatto. Il messaggio è destinato alla finestra su cui il puntatore fa riferimento e il puntatore è, a quel punto, acquisito in modo implicito nella finestra, in modo che la finestra continui a ricevere l'input per il puntatore finché non interrompe il contatto, inclusa la notifica [<strong>WM_NCPOINTERUP</strong>] (WM-ncpointerup.MD). <br/> Se una finestra ha acquisito questo puntatore, questo messaggio non viene inviato. Viene invece pubblicato un [<strong>WM_POINTERUP</strong>] (WM-pointerUp.MD) nella finestra che ha acquisito il puntatore. <br/>
<blockquote>
[!Important]<br />
Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERUPDATE</strong>] (wm-ncpointerupdate.md)<br/></td>
<td>Inviato per fornire un aggiornamento su un puntatore che ha effettuato il contatto sull'area non client di una finestra o quando un contatto non acquisito in sospeso passa sull'area non client di una finestra. Mentre il puntatore è posizionato al passaggio del mouse, il messaggio viene indirizzato a qualsiasi finestra su cui si trova il puntatore. Mentre il puntatore è in contatto con la superficie, il puntatore viene acquisito in modo implicito nella finestra su cui il puntatore ha effettuato il contatto e tale finestra continua a ricevere l'input per il puntatore finché non interrompe il contatto. <br/> Se una finestra ha acquisito questo puntatore, questo messaggio non viene inviato. Viene invece pubblicato un [<strong>WM_POINTERUPDATE</strong>] (WM-pointerupdate.MD) nella finestra che ha acquisito il puntatore.<br/>
<blockquote>
[!Important]<br />
Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_PARENTNOTIFY</strong>] (wm-parentnotify.md)<br/></td>
<td>Inviato a una finestra quando si verifica un'azione significativa in una finestra discendente. Questo messaggio è ora esteso per includere l'evento [<strong>WM_POINTERDOWN</strong>] (WM-PointerDown.MD). Quando viene creata la finestra figlio, il sistema invia [<strong>WM_PARENTNOTIFY</strong>] (/Previous-Versions/Windows/Desktop/inputmsg/WM-parentnotify) appena prima della funzione [<strong>CreateWindow</strong>] (/Windows/Win32/API/winuser/NF-winuser-createwindowa) o [<strong>CreateWindowEx</strong>] (/Windows/Win32/API/winuser/NF-winuser-CreateWindowExA) che crea la finestra restituisce. Quando la finestra figlio viene distrutta, il sistema invia il messaggio prima che venga eseguita un'elaborazione per eliminare la finestra.<br/> Una finestra riceve questo messaggio tramite la relativa funzione [<strong>WindowProc</strong>] (/Previous-Versions/Windows/desktop/legacy/ms633573 (v = vs. 85)). <br/>
<blockquote>
[!Important]<br />
Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERACTIVATE</strong>] (wm-pointeractivate.md)<br/></td>
<td>Inviato a una finestra inattiva quando un puntatore primario genera [<strong>WM_POINTERDOWN</strong>] (WM-PointerDown.MD) sulla finestra. Finché il messaggio rimane non gestito, viene spostata verso l'alto nella catena della finestra padre fino a raggiungere la finestra di primo livello. Le applicazioni possono rispondere a questo messaggio per specificare se desiderano essere attivate.<br/> Una finestra riceve questo messaggio tramite la relativa funzione [<strong>WindowProc</strong>] (/Previous-Versions/Windows/desktop/legacy/ms633573 (v = vs. 85)). <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERCAPTURECHANGED</strong>] (wm-pointercapturechanged.md)<br/></td>
<td>Inviato a una finestra che sta perdendo l'acquisizione di un puntatore di input.<br/> Una finestra riceve questo messaggio tramite la relativa funzione [<strong>WindowProc</strong>] (/Previous-Versions/Windows/desktop/legacy/ms633573 (v = vs. 85)).<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICECHANGE</strong>] (wm-pointerdevicechange.md)<br/></td>
<td>Inviato a una finestra quando viene apportata una modifica alle impostazioni di un monitoraggio a cui è collegato un digitalizzatore. Questo messaggio contiene informazioni sul ridimensionamento della modalità di visualizzazione. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDEVICEINRANGE</strong>] (wm-pointerdeviceinrange.md)<br/></td>
<td>Inviato a una finestra quando viene rilevato un dispositivo puntatore nell'intervallo di un digitalizzatore di input. Questo messaggio contiene informazioni relative al dispositivo e alla relativa prossimità. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICEOUTOFRANGE</strong>] (wm-pointerdeviceoutofrange.md)<br/></td>
<td>Inviato a una finestra quando un dispositivo puntatore ha ripartito l'intervallo di un digitalizzatore di input. Questo messaggio contiene informazioni relative al dispositivo e alla relativa prossimità. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md)<br/></td>
<td>Inviato quando un puntatore fa contatto sull'area client di una finestra. Questo messaggio di input è destinato alla finestra su cui il puntatore fa riferimento e il puntatore viene acquisito in modo implicito nella finestra, in modo che la finestra continui a ricevere l'input per il puntatore finché non interrompe il contatto. <br/> Una finestra riceve questo messaggio tramite la relativa funzione [<strong>WindowProc</strong>] (/Previous-Versions/Windows/desktop/legacy/ms633573 (v = vs. 85)).<br/>
<blockquote>
[!Important]<br />
Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERENTER</strong>] (wm-pointerenter.md)<br/></td>
<td>Inviato a una finestra quando un nuovo puntatore entra nell'intervallo di rilevamento sulla finestra (hover) o quando un puntatore esistente si sposta all'interno dei limiti della finestra. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERLEAVE</strong>] (wm-pointerleave.md)<br/></td>
<td>Inviato a una finestra quando un puntatore lascia un intervallo di rilevamento sulla finestra (hover) o quando un puntatore si sposta all'esterno dei limiti della finestra. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDAWAY</strong>] (wm-pointerroutedaway.md)<br/></td>
<td>Si verifica nel processo che riceve l'input quando l'input del puntatore viene indirizzato a un altro processo.<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERROUTEDRELEASED</strong>] (wm-pointerroutedreleased.md)<br/></td>
<td>Inviato a tutti i processi (configurati per il concatenamento tra processi tramite [<strong>AddContentWithCrossProcessChaining</strong>] (/Windows/Win32/API/directmanipulation/NF-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) e che non gestisce attualmente l'input del puntatore) associati a un ID puntatore specifico, quando viene ricevuto un messaggio [<strong>WM_POINTERUP</strong>] (WM-pointerUp.MD) nel processo corrente. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDTO</strong>] (wm-pointerroutedto.md)<br/></td>
<td>Inviato quando l'input del puntatore in corso, per un ID puntatore esistente, esegue la transizione da un processo a un altro tra i contenuti configurati per il concatenamento tra processi ([<strong>AddContentWithCrossProcessChaining</strong>] (/Windows/Win32/API/directmanipulation/NF-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERUP</strong>] (wm-pointerup.md)<br/></td>
<td>Inviato quando un puntatore che ha effettuato il contatto sull'area client di una finestra interrompe il contatto. Questo messaggio di input è destinato alla finestra su cui il puntatore fa riferimento e il puntatore è, a quel punto, acquisito in modo implicito nella finestra, in modo che la finestra continui a ricevere messaggi di input, inclusa la notifica [<strong>WM_POINTERUP</strong>] (WM-pointerUp.MD) per il puntatore finché non interrompe il contatto. <br/> Una finestra riceve questo messaggio tramite la relativa funzione [<strong>WindowProc</strong>] (/Previous-Versions/Windows/desktop/legacy/ms633573 (v = vs. 85)). <br/>
<blockquote>
[!Important]<br />
Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERUPDATE</strong>] (wm-pointerupdate.md)<br/></td>
<td>Inviato per fornire un aggiornamento su un puntatore che ha effettuato il contatto sull'area client di una finestra o su un puntatore non acquisito posizionato al passaggio del mouse sull'area client di una finestra. Mentre il puntatore è posizionato al passaggio del mouse, il messaggio viene indirizzato a qualsiasi finestra su cui si trova il puntatore. Mentre il puntatore è in contatto con la superficie, il puntatore viene acquisito in modo implicito nella finestra su cui il puntatore ha effettuato il contatto e tale finestra continua a ricevere l'input per il puntatore finché non interrompe il contatto. <br/>
<blockquote>
[!Important]<br />
Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERWHEEL</strong>] (wm-pointerwheel.md)<br/></td>
<td>Inserito nella finestra con lo stato attivo della tastiera in primo piano quando viene ruotata una rotellina di scorrimento. <br/> Una finestra riceve questo messaggio tramite la relativa funzione [<strong>WindowProc</strong>] (/Previous-Versions/Windows/desktop/legacy/ms633573 (v = vs. 85)).<br/>
<blockquote>
[!Important]<br />
Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERHWHEEL</strong>] (wm-pointerhwheel.md)<br/></td>
<td>Inserito nella finestra con lo stato attivo della tastiera in primo piano quando viene ruotata una rotellina di scorrimento orizzontale. <br/> Una finestra riceve questo messaggio tramite la relativa funzione [<strong>WindowProc</strong>] (/Previous-Versions/Windows/desktop/legacy/ms633573 (v = vs. 85)).<br/>
<blockquote>
[!Important]<br />
Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_TOUCHHITTESTING</strong>] (wm-touchhittesting.md)<br/></td>
<td>Inviato a una finestra in un tocco per determinare la destinazione del tocco più probabile. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al messaggio di input del puntatore](wmpointer-reference.md)
</dt> </dl>

 

